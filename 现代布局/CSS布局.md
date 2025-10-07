# CSS布局

- 内容

  ![image-20251005140834177](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251005140834177.png)

- 布局类别

  ![image-20251005140923323](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251005140923323.png)

## 一. CSS正常布局流

1. 定义：

   - 正常布局流(normalflow)是指在不对页面进行任何布局控制时，浏览器默认的 HTML 布局方式。也称为标准流。
   - 正常布局流是 CSS 布局的基石，页面大的布局基本就是利用区块元素上下罗列而成。

2. 元素布局特点：

   - 区块元素：

     ![image-20251005141152498](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251005141152498.png)

   - 行内元素：

     ![image-20251005141215181](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251005141215181.png)

   - 文档流方向：

     ![image-20251005141239058](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251005141239058.png)

## 二. display显示属性

1. 前提：需要块级元素一行排列或者行内元素设置大小

2. display属性概述：

   ![image-20251005141423539](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251005141423539.png)

### 2.1 display转换

![image-20251005144855175](D:\桌面\前端\现代布局\assets\image-20251005144855175.png)

### 2.2 display属性

![image-20251005145005940](D:\桌面\前端\现代布局\assets\image-20251005145005940.png)

## 三. 被放弃的浮动 float

### 3.1 概述

![image-20251005150807812](D:\桌面\前端\现代布局\assets\image-20251005150807812.png)

`当子元素超过父容器的边缘时会换行`

### 3.2 浮动的bug

设置float的元素会覆盖没有设置float的元素

![image-20251005152601156](D:\桌面\前端\现代布局\assets\image-20251005152601156.png)

### 3.3 清除浮动的4种方式

![image-20251005152617293](D:\桌面\前端\现代布局\assets\image-20251005152617293.png)

## 四. 弹性盒子布局 display:flex

### 4.1 flexbox的概述

![image-20251005154034868](D:\桌面\前端\现代布局\assets\image-20251005154034868.png)

### 4.2 flexbox的使用核心

- 父控子

- 主轴与交叉轴

  ![image-20251005154154978](D:\桌面\前端\现代布局\assets\image-20251005154154978.png)

### 4.3 属性

#### 4.3.1 容器的属性

![image-20251005154216750](D:\桌面\前端\现代布局\assets\image-20251005154216750.png)

#### 4.3.2 项目的属性

![image-20251005154240570](D:\桌面\前端\现代布局\assets\image-20251005154240570.png)

### 4.4 flexbox的特性

![image-20251005154305814](D:\桌面\前端\现代布局\assets\image-20251005154305814.png)

### 4.5 主轴的对齐方式

#### 4.5.1 概述

![image-20251005155503911](D:\桌面\前端\现代布局\assets\image-20251005155503911.png)

#### 4.5.2 属性

![image-20251005155516263](D:\桌面\前端\现代布局\assets\image-20251005155516263.png)

### 4.6 交叉轴对齐方式

#### 4.6.1 属性

`只对单行有效`

![image-20251005160524842](D:\桌面\前端\现代布局\assets\image-20251005160524842.png)

### 4.7 改变主轴方向

![image-20251007170020149](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251007170020149.png)

### 4.8 换行warp以及多行交叉轴对齐

#### 4.8.1 换行warp

![image-20251007172221881](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251007172221881.png)

#### 4.8.2 多行交叉轴对齐（align-content）

![image-20251007173802088](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251007173802088.png)

### 4.9 子项目flex伸缩以及gap间隙

#### 4.9.1 子项目flex伸缩尺寸

![image-20251007175622466](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251007175622466.png)

`flex要写在“孩子”身上`

#### 4.9.2 gap间距

![image-20251007180551347](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20251007180551347.png)

### 4.10 京东淘宝多行伸缩布局

1. 淘宝：
   - 在多盒嵌套的基础上，使用padding和margin实现上下文的对齐
2. 京东：
   - 在确保flex=1的基础上，通过使用calc函数计算出min-width和max-width来确定每一行所有盒子的数目