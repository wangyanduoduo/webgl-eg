<!--
 * @Author: wy
 * @Date: 2023-12-06 15:36:01
 * @LastEditors: wy
 * @LastEditTime: 2023-12-11 17:39:06
 * @FilePath: /笔记/webgl-eg/read.md
 * @Description:
-->

## webgl 知识点

### webgl 变量

- attribute 顶点属性
- uniform 类似全局属性，和所有的顶点相关
- varying 片元着色器和顶点着色器之前数据传递
- textures 纹理

### webgl 数据类型

1. vec2
2. vec3
3. vec4
4. precision 片元着色器精度
5. highp: 高精度
6. mediump: 中精度
7. lowp: 低精度

- 矢量
- 矩阵

### 顶点着色器

内置类型和变量
顶点位置：vec4 gl_Position(必须被赋值)
顶点尺寸：float gl_PointSize

顶点坐标有 4 个值： （1， 2， 4， 4） 最后一位代表齐次坐标信息（透视分量），在 webgl 坐标系统里，会自动用，x,y,z 的信息 除以最后一个数(w)，然后最后一个数字被变成 1，这是因为 webgl 坐标系的坐标都是-1 ～ 1 之间的，所以前 3 个数，必须不能设置大于最后一个数。这个坐标就会变成（0.25， 0.5， 1， 1）

### 片元着色器

内置类型和变量
vec4 gl_FragColor(必须被赋值)

### 纹理

纹理的加载需要打开服务器

### 坐标系

#### webgl 坐标

以 0，0 为中心点，上下左右为 1， -1， -1， 1

- x 水平方向（从左到右 -1 ～ 1）
- y 竖直方向（从下到上 -1 ～ 1）
- z 垂直页面（从外到里 -1 ～ 1 ）

#### canvas 坐标

以 canvas 的左上角 为中心点

- x 水平方向（从左到右 右为正）
- y 竖直方向（从上到下 下为正）

#### 纹理坐标

以图片的左下角为坐标轴中心点
