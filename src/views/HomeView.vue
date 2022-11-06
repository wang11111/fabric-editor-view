<template>
  <div class="home">
    <Layout>
      <Header v-show="show">
        <!-- 导入 -->
        <import-JSON></import-JSON>
        &nbsp;
        <import-svg></import-svg>
        &nbsp;
        <import-img style="display:none"></import-img>
        &nbsp;
        <!-- 对齐方式 -->
        <align></align>
        &nbsp;
        <flip></flip>
        &nbsp;
        <center-align></center-align>
        &nbsp;
        <group></group>
        &nbsp;
        <zoom></zoom>
        &nbsp;
        <preset></preset>
        &nbsp;
        <lock></lock>
        &nbsp;
        <dele></dele>
        &nbsp;
        <clone></clone>

        <div style="float:right">
          <save></save>
        </div>
      </Header>
      <Content style=" display: flex; height: calc(100vh - 64px);">
        <div v-if="show" style="width: 380px; height: 100%; background:#fff; display: flex">
          <Menu :active-name="menuActive" accordion @on-select="activeIndex => menuActive = activeIndex" width="80px">
            <!-- <MenuItem :name="1" style="padding:10px"><Icon type="md-book" />模板</MenuItem> -->
            <MenuItem :name="2" style="padding:10px">
            <Icon type="md-create" />元素</MenuItem>
            <MenuItem :name="3" style="padding:10px">
            <Icon type="ios-build" />背景</MenuItem>
          </Menu>
          <div class="content">
            <!-- 生成模板 -->
            <div v-show="menuActive === 1" class="left-panel">
              <import-tmpl></import-tmpl>
            </div>
            <!-- 常用元素 -->
            <div v-show="menuActive === 2" class="left-panel">
              <tools :canvasObj="canvas" @rigthCilck="rigthCilck" @setDrawType="setDrawType"></tools>
              <!-- <svgEl></svgEl> -->
            </div>
            <!-- 背景设置 -->
            <div v-show="menuActive === 3" class="left-panel">
              <set-size></set-size>
              <bg-bar></bg-bar>
            </div>

          </div>
        </div>
        <!-- 画布区域 -->
        <div style="width: 100%;position: relative; background:#F1F1F1;">
          <div class="canvas-box">
            <canvas id="canvas"></canvas>
            <!-- <canvas id="mycanvas"></canvas> -->
            <ContextMenu ref="contextMenu"></ContextMenu>
          </div>
        </div>
        <!-- 属性区域 -->
        <div style="width: 380px; height: 100%; padding:10px; overflow-y: auto; background:#fff">
          <history v-if="show"></history>
          <layer v-if="show"></layer>
          <attribute v-if="show"></attribute>
        </div>
      </Content>
    </Layout>
  </div>
</template>

<script>

// 导入元素
import importJSON from '@/components/importJSON.vue'
import importSvg from '@/components/importSvg.vue'
import importImg from '@/components/importImg.vue'

// 顶部组件
import align from '@/components/align.vue'
import centerAlign from '@/components/centerAlign.vue'
import flip from '@/components/flip.vue'
import save from '@/components/save.vue'
import clone from '@/components/clone.vue'
import group from '@/components/group.vue'
import zoom from '@/components/zoom.vue'
import lock from '@/components/lock.vue'
import dele from '@/components/del.vue'
import preset from '@/components/preset.vue'

// 左侧组件
import importTmpl from '@/components/importTmpl.vue'
import tools from '@/components/tools.vue'
import svgEl from '@/components/svgEl.vue'
import bgBar from '@/components/bgBar.vue'
import setSize from '@/components/setSize.vue'

// 右侧组件
import history from '@/components/history.vue'
import layer from '@/components/layer.vue'
import attribute from '@/components/attribute.vue'

// 功能组件
import EventHandle from '@/utils/eventHandler'
import hotkeys from '@/plugin/hotkeys'
import initAligningGuidelines from '@/plugin/initAligningGuidelines'
import initCenteringGuidelines from '@/plugin/initCenteringGuidelines'
import ContextMenu from '@/components/ContextMenu.vue'
import { fabric } from 'fabric';

const event = new EventHandle()
const canvas = {}
export default {
  name: 'HomeView',
  provide: {
    canvas,
    fabric,
    event
  },
  data() {
    return {
      menuActive: 2,
      show: false,
      select: null,
      isLock: false,
    };
  },
  components: {
    setSize, tools, bgBar, lock, layer, align, attribute, dele, importSvg, save, importJSON, clone, flip, importImg, importTmpl, centerAlign, group, zoom, history, preset, ContextMenu
  },
  created() {
    this.$Spin.show();
  },
  mounted() {
    this.canvas = canvas.c = new fabric.Canvas('canvas', {
      fireRightClick: true,
      fireMiddleClick: true,
      selectionFullyContained: false,
      selectionKey: 'ctrlKey',
      targetFindTolerance: 10
    });
    this.canvas.set('selectionFullyContained', true)
    initAligningGuidelines(this.canvas)
    initCenteringGuidelines(this.canvas)

    this.canvas.set('backgroundColor', '#fff')
    this.show = true
    this.$Spin.hide();
    event.init(this.canvas)
    hotkeys(this.canvas)
    this.setControlsStyle(fabric)
  },
  methods: {
    setControlsStyle(fabric) {
      fabric.Object.prototype.transparentCorners = false;
      fabric.Object.prototype.cornerSize = 10;
      fabric.Object.prototype.cornerStrokeColor = '#C2C2C2';
      fabric.Object.prototype.cornerColor = '#ffffff';
      fabric.Object.prototype.cornerStyle = 'circle';
      fabric.Object.prototype.borderColor = '#85CCF9';

      fabric.Intersection.intersectLinePolygon = function (a1, a2, points, infinite = true) {
        var result = new fabric.Intersection(),
          length = points.length,
          b1, b2, inter, i;

        for (i = 0; i < length; i++) {
          b1 = points[i];
          b2 = points[(i + 1) % length];
          inter = fabric.Intersection.intersectLineLine(a1, a2, b1, b2);

          result.appendPoints(inter.points);
        }
        if (result.points.length > 0) {
          result.status = 'Intersection';
        }
        return result;
      }
      fabric.Canvas.prototype.setCursor = function (value) {
        this.upperCanvasEl.style.cursor = value;
      }

      fabric.Canvas.prototype._setCursorFromEvent = function (e, target) {
        console.log(target);
        if (!target) {
          this.setCursor(this.defaultCursor);
          return false;
        }
        var hoverCursor = target.hoverCursor || this.hoverCursor,
          activeSelection = this._activeObject && this._activeObject.type === 'activeSelection' ?
            this._activeObject : null,
          // only show proper corner when group selection is not active
          corner = (!activeSelection || !activeSelection.contains(target))
            // here we call findTargetCorner always with undefined for the touch parameter.
            // we assume that if you are using a cursor you do not need to interact with
            // the bigger touch area.
            && target._findTargetCorner(this.getPointer(e, true));

        if (!corner) {
          if (target.subTargetCheck) {
            // hoverCursor should come from top-most subTarget,
            // so we walk the array backwards
            this.targets.concat().reverse().map(function (_target) {
              hoverCursor = _target.hoverCursor || hoverCursor;
            });
          }
          this.setCursor(hoverCursor);
        }
        else {
          this.setCursor(this.getCornerCursor(corner, target, e));
        }
      },

        fabric.Intersection.intersectLineLine = function (a1, a2, b1, b2) {
          var result,
            uaT = (b2.x - b1.x) * (a1.y - b1.y) - (b2.y - b1.y) * (a1.x - b1.x),
            ubT = (a2.x - a1.x) * (a1.y - b1.y) - (a2.y - a1.y) * (a1.x - b1.x),
            uB = (b2.y - b1.y) * (a2.x - a1.x) - (b2.x - b1.x) * (a2.y - a1.y);
          if (uB !== 0) {
            var ua = uaT / uB,
              ub = ubT / uB;
            if (0 <= ua && ua <= 1 && 0 <= ub && ub <= 1) {
              result = new fabric.Intersection('Intersection');
              result.appendPoint(new fabric.Point(a1.x + ua * (a2.x - a1.x), a1.y + ua * (a2.y - a1.y)));
            }
            else {
              result = new fabric.Intersection();
            }
          }
          else {
            if (uaT === 0 || ubT === 0) {
              result = new fabric.Intersection('Coincident');
            }
            else {
              result = new fabric.Intersection('Parallel');
            }
          }
          return result;
        };
      // fabric.Canvas.prototype.getActiveObjects = function () {
      //   var active = this._activeObject;
      //   if (active) {
      //     if (active.type === 'activeSelection' && active._objects) {
      //       return active._objects.slice(0);
      //     }
      //     else {
      //       return [active];
      //     }
      //   }
      //   return [];
      // }

    },
    rigthCilck(e) {
      this.$refs.contextMenu.canvasOnMouseDown(e);
    },
    setDrawType(dType) {
      this.$refs.contextMenu.drawType = dType;
    }
  }
};
</script>
<style lang="less" scoped>
/deep/ .ivu-layout-header {
  padding: 0 10px;
}

.home,
.ivu-layout {
  height: 100vh;
}

.icon {
  display: block;
}

.canvas-box {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

#canvas {
  width: 300px;
  height: 300px;
  margin: 0 auto;
}

.content {
  flex: 1;
  width: 200px;
  padding: 10px;
  padding-top: 0;
  height: 100%;
  overflow-y: auto;
}
</style>
