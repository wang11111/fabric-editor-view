<template>
  <div>
    <Divider plain orientation="left">常用元素</Divider>
    <div class="tool-box">
      <span @click="drawTypeChange('itext')">
        <svg t="1650875455324" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
          p-id="5401" width="26" height="26">
          <path
            d="M213.333333 209.92v128h85.333334v-42.666667h170.666666v433.493334H384.853333v85.333333h256v-85.333333H554.666667V295.253333h170.666666v42.666667h85.333334v-128H213.333333z"
            p-id="5402"></path>
        </svg>
      </span>
      <span @click="drawPolygon">
        <svg t="1650854954008" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
          p-id="14038" width="26" height="26">
          <path
            d="M720.832 692.352h-12.64L530.208 260.448a19.968 19.968 0 0 0-36.416 0L316.608 692.352h-13.44c-7.904 0-15.04 3.968-17.408 11.072a19.872 19.872 0 0 0 18.208 27.68h56.96c9.504 0 18.208-6.336 19.776-15.808a18.752 18.752 0 0 0-15.808-21.344l36.384-87.808h159.776l34.816 87.808a18.88 18.88 0 0 0-15.808 21.344c1.568 9.504 10.272 15.808 19.776 15.808h121.024c7.904 0 15.04-3.968 17.408-11.072a19.2 19.2 0 0 0-17.408-27.68z m-306.112-125.76l64.864-158.208 64.864 158.208H414.72z m-246.816-80.704c0 6.336 5.536 11.872 11.872 11.872s11.872-5.536 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744z m0-75.936c0 6.336 5.536 11.872 11.872 11.872s11.872-5.536 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744z m0 151.872c0 6.336 5.536 11.872 11.872 11.872s11.872-5.536 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744z m11.872-216.736a12.16 12.16 0 0 0 11.872-11.872v-23.744c-0.8-6.336-5.536-11.072-11.872-11.072s-11.872 5.536-11.872 11.872v23.744c0 6.336 4.736 11.072 11.872 11.072z m-11.872 292.672c0 6.336 5.536 11.872 11.872 11.872s11.872-5.536 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744z m0 75.936c0 7.104 4.736 11.872 11.872 11.872a12.16 12.16 0 0 0 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744z m665.248-227.808c0 6.336 5.536 11.872 11.872 11.872s11.872-5.536 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744z m0-75.936c0 6.336 5.536 11.872 11.872 11.872s11.872-5.536 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744z m0 151.872c0 6.336 5.536 11.872 11.872 11.872s11.872-5.536 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744z m11.072-216.736a12.16 12.16 0 0 0 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744c0.8 7.104 5.536 11.872 11.872 11.872z m-11.072 292.672c0 6.336 5.536 11.872 11.872 11.872s11.872-5.536 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744z m0 75.936c0 6.336 5.536 11.872 11.872 11.872s11.872-5.536 11.872-11.872v-23.744c0-6.336-5.536-11.872-11.872-11.872s-11.872 5.536-11.872 11.872v23.744z m-347.264 119.456h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872h23.744c6.336 0 11.872-5.536 11.872-11.872s-5.536-11.872-11.872-11.872z m-75.936 0h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872h23.744c6.336 0 11.872-5.536 11.872-11.872s-5.536-11.872-11.872-11.872z m151.872 0h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872h23.744c6.336 0 11.872-5.536 11.872-11.872s-5.536-11.872-11.872-11.872z m-228.608 0h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872h23.744c6.336 0 11.872-5.536 11.872-11.872s-4.736-11.872-11.872-11.872z m-75.136-7.904H222.496v-11.072a12.48 12.48 0 0 0-12.672-12.64h-18.976v-37.984c0-7.104-5.536-12.64-11.872-12.64s-11.872 5.536-11.872 12.64v37.984h-10.272a12.512 12.512 0 0 0-12.672 12.64v52.992a12.48 12.48 0 0 0 12.672 12.64h52.992a12.512 12.512 0 0 0 12.672-12.64v-11.072h35.584c7.104-1.568 12.672-7.904 12.672-14.24 0-7.104-12.672-16.608-12.672-16.608z m379.68 7.904h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872h23.744c6.336 0 11.872-5.536 11.872-11.872s-5.536-11.872-11.872-11.872z m75.936 0h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872h23.744c6.336 0 11.872-5.536 11.872-11.872s-4.736-11.872-11.872-11.872z m-251.52-642.304h23.744c6.336 0 11.872-5.536 11.872-11.872s-5.536-11.872-11.872-11.872h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872z m-75.936 0h23.744c6.336 0 11.872-5.536 11.872-11.872s-5.536-11.872-11.872-11.872h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872z m151.872 0h23.744c6.336 0 11.872-5.536 11.872-11.872s-5.536-11.872-11.872-11.872h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872z m-227.808 0h23.744c6.336 0 11.872-5.536 11.872-11.872s-5.536-11.872-11.872-11.872h-23.744c-7.104 0.8-11.872 5.536-11.872 12.672s4.736 11.072 11.872 11.072zM257.28 167.904H221.696v-11.072a12.512 12.512 0 0 0-12.672-12.672H156.832a12.512 12.512 0 0 0-12.672 12.672v52.992c0 7.104 5.536 12.672 12.672 12.672h11.072v35.584c1.568 7.104 7.904 12.672 14.24 12.672s16.608-12.672 16.608-12.672V222.496h11.072a12.512 12.512 0 0 0 12.672-12.672v-18.976h35.584a12.16 12.16 0 0 0 11.872-11.872 12.224 12.224 0 0 0-12.672-11.072z m356.768 22.944h23.744c6.336 0 11.872-5.536 11.872-11.872s-5.536-11.872-11.872-11.872h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872z m76.736 0h23.744c6.336 0 11.072-4.736 11.072-11.072s-5.536-11.872-11.872-11.872h-23.744c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.072 12.64 11.072z m176.384-46.656h-52.992a12.48 12.48 0 0 0-12.64 12.672v11.072h-35.584c-7.104 1.568-12.64 7.904-12.64 14.24s12.64 16.608 12.64 16.608h35.584v11.072c0 7.104 5.536 12.672 12.64 12.672h18.976v37.984c0 7.104 5.536 12.672 11.872 12.672s11.872-5.536 11.872-12.672V222.528h11.072a12.48 12.48 0 0 0 12.64-12.672V156.864a13.76 13.76 0 0 0-13.44-12.672z m0 657.312h-11.072v-35.584c-1.568-7.104-7.904-12.64-14.24-12.64-7.104 0-16.608 12.64-16.608 12.64v35.584h-11.072a12.48 12.48 0 0 0-12.64 12.64v18.976h-35.584c-6.336 0-11.872 5.536-11.872 11.872s5.536 11.872 11.872 11.872h35.584v11.072a12.48 12.48 0 0 0 12.64 12.64h52.992a12.48 12.48 0 0 0 12.64-12.64v-52.992c0-7.904-5.536-13.44-12.64-13.44z"
            p-id="14039"></path>
        </svg>
      </span>
      <span @click="drawTypeChange('rectangle')">
        <svg t="1650855811131" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
          p-id="18499" width="26" height="26">
          <path
            d="M864 896H160a32 32 0 0 1-32-32V160a32 32 0 0 1 32-32h704a32 32 0 0 1 32 32v704a32 32 0 0 1-32 32zM192 832h640V192H192v640z"
            p-id="18500"></path>
        </svg>
      </span>
      <span @click="drawTypeChange('ellipse')">
        <svg t="1650855860236" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
          p-id="19440" width="26" height="26">
          <path
            d="M512 928C282.624 928 96 741.376 96 512S282.624 96 512 96s416 186.624 416 416-186.624 416-416 416z m0-768C317.92 160 160 317.92 160 512s157.92 352 352 352 352-157.92 352-352S706.08 160 512 160z"
            p-id="19441"></path>
        </svg>
      </span>
      <span @click="drawTypeChange('semicircle')">
        <svg t="1650855860236" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
          p-id="19440" width="26" height="26">
          <path
            d="M512 928C282.624 928 96 741.376 96 512S282.624 96 512 96s416 186.624 416 416-186.624 416-416 416z m0-768C317.92 160 160 317.92 160 512s157.92 352 352 352 352-157.92 352-352S706.08 160 512 160z"
            p-id="19441"></path>
        </svg>
      </span>
      <span @click="drawTypeChange('triangle')">
        <svg t="1650874633978" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
          p-id="2032" width="26" height="26">
          <path
            d="M928.64 896a2.144 2.144 0 0 1-0.64 0H96a32.032 32.032 0 0 1-27.552-48.288l416-704c11.488-19.456 43.552-19.456 55.104 0l413.152 699.2A31.936 31.936 0 0 1 928.64 896zM152.064 832h719.84L512 222.912 152.064 832z"
            p-id="2033"></path>
        </svg>
      </span>
      <span @click="drawTypeChange('gridentRectangle')">
        <svg t="1650855811131" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
          p-id="18499" width="26" height="26">
          <path
            d="M864 896H160a32 32 0 0 1-32-32V160a32 32 0 0 1 32-32h704a32 32 0 0 1 32 32v704a32 32 0 0 1-32 32zM192 832h640V192H192v640z"
            p-id="18500"></path>
        </svg>
      </span>
      <span @click="drawTypeChange('clippath')">
        <svg t="1650855811131" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg"
          p-id="18499" width="26" height="26">
          <path
            d="M864 896H160a32 32 0 0 1-32-32V160a32 32 0 0 1 32-32h704a32 32 0 0 1 32 32v704a32 32 0 0 1-32 32zM192 832h640V192H192v640z"
            p-id="18500"></path>
        </svg>
      </span>
    </div>
    <!-- <Divider plain orientation="left">快捷导航</Divider>
    <div>
      <a href="https://color.uisdc.com/pick.html" target="_blank">配色</a>
      <Divider type="vertical" />
      <a href="https://www.svgrepo.com/" target="_blank">素材</a>
      <Divider type="vertical" />
      <a href="https://unsplash.com/" target="_blank">图片</a>
      <Divider type="vertical" />
      <a href="https://www.pexels.com/zh-cn/search/%E8%83%8C%E6%99%AF/" target="_blank">背景</a>
    </div> -->
  </div>
</template>

<script>
import { v4 as uuid } from 'uuid';
import options from '../plugin/options'
import $ from 'jquery'
import semicircle from '@/custom/semicircle'

const defaultPosition = {
  left: 100, top: 100, shadow: '', fontFamily: 'arial'
}
export default {
  name: 'ToolBar',
  inject: ['canvas', 'fabric'],
  data() {
    return {
      options,
      rect: [],
      showMenu: false,
      mouseFrom: {},
      mouseTo: {},
      drawType: null,  //当前绘制图像的种类
      drawWidth: 2, //笔触宽度
      color: "#E34F51", //画笔颜色
      drawingObject: null, //当前绘制对象
      moveCount: 1, //绘制移动计数器
      doDrawing: false, // 绘制状态

      //polygon 相关参数
      polygonMode: false,
      pointArray: [],
      lineArray: [],
      activeShape: false,
      activeLine: "",
      line: {},
      semicircle: {}
    };
  },
  mounted() {
    //  this.canvas.selectionColor = "rgba(0,0,0,0.05)";
    this.canvas.c.on("mouse:down", this.mousedown);
    this.canvas.c.on("mouse:move", this.mousemove);
    this.canvas.c.on("mouse:up", this.mouseup);
    this.canvas.c.on("mouse:over", this.mouseover);

    $(document).contextmenu(function (e) {
      e.preventDefault();
    });
    this.semicircle = semicircle();
  },
  methods: {
    // 鼠标点击直线
    mousedown(e) {
      this.$emit('rigthCilck', e);
      // 如果是右键，结束当前绘制
      if (e.button === 3) {
        if (this.drawType === "polygon") {
          this.generatePolygon();
        }

        this.drawTypeChange("");
        return;
      }
      // 记录鼠标按下时的坐标
      var xy = e.absolutePointer || this.transformMouse(e.e.offsetX, e.e.offsetY);
      this.mouseFrom.x = xy.x;
      this.mouseFrom.y = xy.y;
      this.doDrawing = true;
      if (this.drawType == "text") {
        this.drawing();
      }

      // 绘制多边形
      if (this.drawType == "polygon") {
        this.canvas.skipTargetFind = false;
        try {
          // 此段为判断是否闭合多边形，点击红点时闭合多边形
          if (this.pointArray.length > 1) {
            // e.target.id == this.pointArray[0].id 表示点击了初始红点
            if (e.target && e.target.id == this.pointArray[0].id) {
              this.generatePolygon(true);
            }
          }
          //未点击红点则继续作画
          if (this.polygonMode) {
            this.addPoint(e);
          }
        } catch (error) {
          console.log(error);
        }
      }
    },

    // 鼠标松开执行
    mouseup(e) {
      var xy = e.pointer || this.transformMouse(e.e.offsetX, e.e.offsetY);
      this.mouseTo.x = xy.x;
      this.mouseTo.y = xy.y;
      this.drawingObject = null;
      this.moveCount = 1;
      if (this.drawType != "polygon") {
        this.doDrawing = false;
      }
    },

    //鼠标移动过程中已经完成了绘制
    mousemove(e) {
      if (this.moveCount % 2 && !this.doDrawing) {
        //减少绘制频率
        return;
      }
      this.moveCount++;
      var xy = e.absolutePointer || this.transformMouse(e.e.offsetX, e.e.offsetY);
      this.mouseTo.x = xy.x;
      this.mouseTo.y = xy.y;
      // 多边形特殊处理
      if (this.drawType != "polygon") {
        this.drawing(e);
      }
      if (this.drawType == "polygon") {
        var adsortPoint = this.getAdsortPoint(e.absolutePointer.x, e.absolutePointer.y);
        if (this.activeLine && this.activeLine.class == "line") {
          this.activeLine.set({ x2: adsortPoint.x, y2: adsortPoint.y });

          var points = this.activeShape.get("points");
          points[this.pointArray.length] = {
            x: adsortPoint.x,
            y: adsortPoint.y,
            zIndex: 1
          };
          this.activeShape.set({
            points: points
          });
          this.canvas.c.renderAll();
        }
        this.canvas.c.renderAll();
      }
    },

    //鼠标移动过程中已经完成了绘制
    mouseover(e) {
    },
    // 开始绘制时，指定绘画种类
    drawTypeChange(e) {
      this.drawType = e;
      // this.canvas.c.set('skipTargetFind', true)
      // 绘制过程中关闭选中
      this.canvas.c.selection = !e;
      this.$emit('setDrawType', this.drawType);
      this.canvas.c.skipTargetFind = !!e

    },

    deleteObj() {
      this.canvas.getActiveObjects().map(item => {
        this.canvas.c.remove(item);
      });
    },
    transformMouse(mouseX, mouseY) {
      return { x: mouseX / 1, y: mouseY / 1 };
    },
    // 绘制多边形开始，绘制多边形和其他图形不一样，需要单独处理
    drawPolygon() {
      this.drawType = "polygon";
      this.$emit('setDrawType', this.drawType);
      this.polygonMode = true;
      //这里画的多边形，由顶点与线组成
      this.pointArray = new Array();  // 顶点集合
      this.lineArray = new Array();  //线集合
    },
    addPoint(e) {
      //var point = this.canvas.getPointer(e.e)
      var adsortPoint = this.getAdsortPoint(e.absolutePointer.x, e.absolutePointer.y);
      var random = Math.floor(Math.random() * 10000);
      var id = new Date().getTime() + random;
      var circle = new fabric.Circle({
        radius: 5,
        fill: "#ffffff",
        stroke: "#333333",
        strokeWidth: 0.5,
        left: (adsortPoint.x || e.e.layerX),
        top: (adsortPoint.y || e.e.layerY),
        selectable: false,
        hasBorders: false,
        hasControls: false,
        originX: "center",
        originY: "center",
        id: id,
        objectCaching: false
      });
      if (this.pointArray.length == 0) {
        circle.set({
          fill: "red"
        });
      }
      var points = [
        (adsortPoint.x),
        (adsortPoint.y),
        (adsortPoint.x),
        (adsortPoint.y)
      ];

      this.line = new fabric.Line(points, {
        strokeWidth: 2,
        fill: "#999999",
        stroke: "#999999",
        class: "line",
        originX: "center",
        originY: "center",
        selectable: false,
        hasBorders: false,
        hasControls: false,
        evented: false,

        objectCaching: false
      });
      if (this.activeShape) {
        //var pos = this.canvas.getPointer(e.e);
        var points = this.activeShape.get("points");
        points.push({
          x: adsortPoint.x,
          y: adsortPoint.y
        });
        var polygon = new fabric.Polyline(points, {
          stroke: "#333333",
          strokeWidth: 1,
          fill: "",
          // opacity: 0.3,

          selectable: false,
          hasBorders: false,
          hasControls: false,
          evented: false,
          objectCaching: false
        });
        this.canvas.c.remove(this.activeShape);
        this.canvas.c.add(polygon);
        this.activeShape = polygon;
        this.canvas.c.renderAll();
      } else {
        var polyPoint = [
          {
            x: (adsortPoint.x),
            y: (adsortPoint.y)
          }
        ];
        var polygon = new fabric.Polyline(polyPoint, {
          stroke: "#333333",
          strokeWidth: 1,
          fill: "#cccccc",
          opacity: 0.3,

          selectable: false,
          hasBorders: false,
          hasControls: false,
          evented: false,
          objectCaching: false
        });
        this.activeShape = polygon;
        this.canvas.c.add(polygon);
      }
      this.activeLine = this.line;

      this.pointArray.push(circle);
      this.lineArray.push(this.line);
      this.canvas.c.add(this.line);
      this.canvas.c.add(circle);
    },
    generatePolygon(isClose) {
      var points = new Array();
      this.pointArray.map((point, index) => {
        points.push({
          x: point.left,
          y: point.top
        });
        this.canvas.c.remove(point);
      });
      this.lineArray.map((line, index) => {
        this.canvas.c.remove(line);
      });
      this.canvas.c.remove(this.activeShape).remove(this.activeLine);
      var polygon = null;
      if (isClose) {
        polygon = new fabric.Polygon(points, {
          stroke: this.options.borderColor,
          strokeWidth: this.drawWidth,
          fill: this.options.fillColor,
          opacity: 1,
          hasBorders: false,
          hasControls: false,
          perPixelTargetFind: true,
          objectCaching: false,
        });
      } else {
        polygon = new fabric.Polyline(points, {
          stroke: this.options.borderColor,
          strokeWidth: this.drawWidth,
          fill: this.options.fillColor,
          opacity: 1,
          hasBorders: false,
          hasControls: false,
          perPixelTargetFind: true,
          objectCaching: false
        });
      }
      this.canvas.c.add(polygon);

      this.activeLine = null;
      this.activeShape = null;
      this.polygonMode = false;
      this.doDrawing = false;
      this.drawType = null;
      this.$emit('setDrawType', this.drawType);
    },
    drawing(e) {
      if (this.drawingObject) {
        this.canvas.c.remove(this.drawingObject);
      }
      var canvasObject = null;
      var left = this.mouseFrom.x;
      var top = this.mouseFrom.y;
      var mouseFrom = this.mouseFrom;
      var mouseTo = this.mouseTo;
      switch (this.drawType) {
        case "arrow": //箭头
          var x1 = mouseFrom.x,
            x2 = mouseTo.x,
            y1 = mouseFrom.y,
            y2 = mouseTo.y;
          var w = x2 - x1,
            h = y2 - y1,
            sh = Math.cos(Math.PI / 4) * 16;
          var sin = h / Math.sqrt(Math.pow(w, 2) + Math.pow(h, 2));
          var cos = w / Math.sqrt(Math.pow(w, 2) + Math.pow(h, 2));
          var w1 = (16 * sin) / 4,
            h1 = (16 * cos) / 4,
            centerx = sh * cos,
            centery = sh * sin;
          /**
           * centerx,centery 表示起始点，终点连线与箭头尖端等边三角形交点相对x，y
           * w1 ，h1用于确定四个点
           */

          var path = " M " + x1 + " " + y1;
          path += " L " + (x2 - centerx + w1) + " " + (y2 - centery - h1);
          path +=
            " L " + (x2 - centerx + w1 * 2) + " " + (y2 - centery - h1 * 2);
          path += " L " + x2 + " " + y2;
          path +=
            " L " + (x2 - centerx - w1 * 2) + " " + (y2 - centery + h1 * 2);
          path += " L " + (x2 - centerx - w1) + " " + (y2 - centery + h1);
          path += " Z";
          canvasObject = new fabric.Path(path, {
            stroke: this.options.borderColor,
            fill: this.options.fillColor,
            strokeWidth: this.drawWidth
          });
          break;
        case "pentagram": //五角星
          var x1 = mouseFrom.x,
            x2 = mouseTo.x,
            y1 = mouseFrom.y,
            y2 = mouseTo.y;
          /**
           * 实现思路  (x1,y1)表示鼠标起始的位置 (x2,y2)表示鼠标抬起的位置
           * r 表示五边形外圈圆的半径，这里建议自己画个图理解
           * 正五边形夹角为36度。计算出cos18°，sin18°备用
           */
          var w = Math.abs(x2 - x1),
            h = Math.abs(y2 - y1),
            r = Math.sqrt(w * w + h * h)
          var cos18 = Math.cos(18 * Math.PI / 180)
          var sin18 = Math.sin(18 * Math.PI / 180)

          /**
           * 算出对应五个点的坐标转化为路径
           */
          var point1 = [x1, y1 + r]
          var point2 = [x1 + 2 * r * (sin18), y1 + r - 2 * r * (cos18)]
          var point3 = [x1 - r * (cos18), y1 + r * (sin18)]
          var point4 = [x1 + r * (cos18), y1 + r * (sin18)]
          var point5 = [x1 - 2 * r * (sin18), y1 + r - 2 * r * (cos18)]

          var path = " M " + point1[0] + " " + point1[1]
          path += " L " + point2[0] + " " + point2[1]
          path += " L " + point3[0] + " " + point3[1]
          path += " L " + point4[0] + " " + point4[1]
          path += " L " + point5[0] + " " + point5[1]
          path += " Z";
          canvasObject = new fabric.Path(path, {
            stroke: this.options.borderColor,
            fill: this.options.fillColor,
            strokeWidth: this.drawWidth,
            // angle:180,  //设置旋转角度
          });
          break;
        case "ellipse": //椭圆
          // 按shift时画正圆，只有在鼠标移动时才执行这个，所以按了shift但是没有拖动鼠标将不会画圆
          if (e.e.shiftKey) {
            mouseTo.x - left > mouseTo.y - top ? mouseTo.y = top + mouseTo.x - left : mouseTo.x = left + mouseTo.y - top
          }
          var radius =
            Math.sqrt(
              (mouseTo.x - left) * (mouseTo.x - left) +
              (mouseTo.y - top) * (mouseTo.y - top)
            ) / 2;
          canvasObject = new fabric.Ellipse({
            id: uuid(),
            left: (mouseTo.x - left) / 2 + left,
            top: (mouseTo.y - top) / 2 + top,
            stroke: this.options.borderColor,
            fill: this.options.fillColor,
            originX: "center",
            originY: "center",
            rx: Math.abs(left - mouseTo.x) / 2,
            ry: Math.abs(top - mouseTo.y) / 2,
            strokeWidth: this.drawWidth
          });
          break;
        case "rectangle": //长方形
          // 按shift时画正方型
          if (e.e.shiftKey) {
            mouseTo.x - left > mouseTo.y - top ? mouseTo.y = top + mouseTo.x - left : mouseTo.x = left + mouseTo.y - top
          }
          canvasObject = new fabric.Rect({
            top: Math.min(mouseFrom.y, mouseTo.y),
            left: Math.min(mouseFrom.x, mouseTo.x),
            width: Math.abs(mouseFrom.x - mouseTo.x),
            height: Math.abs(mouseFrom.y - mouseTo.y),
            stroke: this.options.borderColor,
            fill: this.options.fillColor,
            strokeUniform: true
          })
          break;
        case 'gridentRectangle':
          canvasObject = new fabric.Rect({
            top: Math.min(mouseFrom.y, mouseTo.y),
            left: Math.min(mouseFrom.x, mouseTo.x),
            width: Math.abs(mouseFrom.x - mouseTo.x),
            height: Math.abs(mouseFrom.y - mouseTo.y),
            stroke: this.options.borderColor,
            fill: this.options.fillColor,
          })

          var grident = new fabric.Gradient({
            type: 'linear', // linear or radial
            gradientUnits: 'pixels', // pixels or pencentage 像素 或者 百分比
            coords: { x1: 0, y1: 0, x2: canvasObject.width, y2: 0 },
            colorStops: [ // 定义渐变颜色的数组
              { offset: 0, color: 'gray' },
              { offset: 0.5, color: 'white' },
              { offset: 1, color: 'gray' },
            ]
          })
          canvasObject.set('fill', grident);
          break;
        case 'clippath':
          // 裁剪的图形
          // clipPath从对象的中心开始定位，对象originX和originY不起任何作用，而clipPath originX和originY起作用。定位逻辑与fabric.Group相同
          const clipPath = new fabric.Circle({
            radius: 40,
            left: -40,
            top: -40
          })

          canvasObject = new fabric.Group([
            new fabric.Rect({ width: 100, height: 100, fill: 'red' }),
            new fabric.Rect({ width: 100, height: 100, fill: 'yellow', left: 100 }),
            new fabric.Rect({ width: 100, height: 100, fill: 'blue', top: 100 }),
            new fabric.Rect({
              width: 100,
              height: 100,
              fill: 'green',
              left: 100,
              top: 100
            })
          ])
          // 裁剪一个组
          canvasObject.clipPath = clipPath
          break;
        case 'triangle':
          canvasObject = new this.fabric.Triangle({
            top: Math.min(mouseFrom.y, mouseTo.y),
            left: Math.min(mouseFrom.x, mouseTo.x),
            width: Math.abs(mouseFrom.x - mouseTo.x),
            height: Math.abs(mouseFrom.y - mouseTo.y),
            stroke: this.options.borderColor,
            fill: this.options.fillColor,
          })
          var grident = new fabric.Gradient({
            type: 'linear', // linear or radial
            gradientUnits: 'pixels', // pixels or pencentage 像素 或者 百分比
            coords: { x1: 0, y1: 0, x2: canvasObject.width, y2: 0 },
            colorStops: [ // 定义渐变颜色的数组
              { offset: 0, color: 'gray' },
              { offset: 0.5, color: 'white' },
              { offset: 1, color: 'gray' },
            ]
          })
          canvasObject.set('fill', grident);
          break;
        case "itext": //文本框
          canvasObject = new fabric.IText("Hello world !", {
            top: Math.min(mouseFrom.y, mouseTo.y),
            left: Math.min(mouseFrom.x, mouseTo.x),
            width: Math.abs(mouseFrom.x - mouseTo.x),
            height: Math.abs(mouseFrom.y - mouseTo.y),

            backgroundColor: '#FFFFFF',
            fill: '#000000',
            fontSize: 12,
            lockScalingX: true,
            lockScalingY: true,
            hasRotatingPoint: false,
            transparentCorners: false,
            hasControls: false,
            cornerSize: 7,
          });
          break;
        case "text": //文本框
          canvasObject = new fabric.Textbox("", {
            left: mouseFrom.x,
            top: mouseFrom.y - 10,
            // width: 150,
            fontSize: 16,
            borderColor: this.options.borderColor,
            fill: this.options.borderColor,
          });
          break;
        case "semicircle":
          canvasObject = new this.semicircle({
            top: Math.min(mouseFrom.y, mouseTo.y),
            left: Math.min(mouseFrom.x, mouseTo.x),
            width: Math.abs(mouseFrom.x - mouseTo.x),
            height: Math.abs(mouseFrom.y - mouseTo.y),
            stroke: this.options.borderColor, // 描边色
            fill: this.options.fillColor, // 填充色
            strokeWidth: 1, // 描边宽度
          });
          break;
        default:
          break;
      }

      if (canvasObject) {
        // canvasObject.index = getCanvasObjectIndex();\
        this.canvas.c.add(canvasObject);
        this.canvas.c.setActiveObject(canvasObject)
        this.drawingObject = canvasObject;
      }
    },
    //#region 绘制节点方法

    //#endregion
    // 寻找吸附点
    getAdsortPoint(pointx, pointy) {
      var x = Math.abs(pointx);
      var y = Math.abs(pointy);
      if (!this.options.adsorbPoint) {
        return { x, y }
      }
      const gridSize = this.options.gridSize;//scale
      const resizeX = x % gridSize;
      const resizeY = y % gridSize;
      if (resizeX !== 0) {
        if (resizeX > gridSize / 2) {
          x += gridSize - resizeX;
        } else {
          x -= resizeX;
        }
      }
      if (resizeY !== 0) {
        if (resizeY > gridSize / 2) {
          y += gridSize - resizeY;
        } else {
          y -= resizeY;
        }
      }
      if (pointx < 0) {
        x = -x;
      }
      if (pointy < 0) {
        y = -y;
      }
      return { x, y }
    },
    //---------------------------------------原代码--------------------------------
    addImg(e) {
      const imgEl = e.target.cloneNode(true)
      const imgInstance = new fabric.Image(imgEl, {
        ...defaultPosition,
        id: uuid(),
        name: '图片default'
      });
      this.canvas.c.add(imgInstance)
      this.canvas.c.renderAll()
    },
  }
};
</script>

<style scoped lang="less">
.tool-box {
  display: flex;
  justify-content: space-around;

  span {
    flex: 1;
    text-align: center;
    padding: 5px 0;
    background: #f6f6f6;
    margin-left: 2px;
    cursor: pointer;

    &:hover {
      background: #edf9ff;

      svg {
        fill: #2d8cf0;
      }
    }
  }
}

.img {
  width: 20px;
}
</style>
