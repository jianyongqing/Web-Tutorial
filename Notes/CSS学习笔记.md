## 一、CSS基础知识

### 1.1 CSS介绍及语法

> CSS：Cascading Style Sheet，层叠样式表. CSS的作用就是给HTML页面标签添加各种样式，**定义网页的显示效果**. 简单一句话：CSS将网页**内容和显示样式进行分离**，提高了显示功能。

```css
/*这是个注释*/
selector{
    property:value
}

/* 实例 */
body{
    color:red;
    font-size:14px;
}
/* 选择器分组|继承 */
h1,h2,h3{
    color:green;
}
```

### 1.2 选择器

- **标签选择器**

1. **派生选择器**

   通过依据元素在其位置的上下文关系来定义样式

   ```css
   /* 将列表中的 strong 元素变为斜体字，而不是通常的粗体字*/
   li strong {
       font-style: italic;
       font-weight: normal;
   }
   ```

2. **id选择器**

   id选择器可以为标有id的HTML元素指定特定的样式

   id选择器以"#"来定义

   ```css
   #red {color:red;}
   #green {color:green;}
   ```

   id 选择器和派生选择器

    在现代布局中，id 选择器常常用于建立派生选择器

   ```css
   #sidebar p {
   	font-style: italic;
   	text-align: right;
   	margin-top: 0.5em;
   }
   ```

   

3. **类选择器**

   类选择器以一个点''.''显示

   ```css
   .center {
       text-align: center
   }
   ```

   

4. **属性选择器**

   对带有指定属性的HTML元素设置样式

   ```css
   /* 为带有 title 属性的所有元素设置样式 */
   [title]{
       color:red;
   }
   ```

### 1.3 如何插入样式表

1. **外部样式表**

   ```html
   <head>
   <link rel="stylesheet" type="text/css" href="mystyle.css" />
   </head>
   ```

2. **内部样式表**

   ```html
   <head>
       <style type="text/css">
           hr {color: sienna;}
           p {margin-left: 20px;}
           body {background-image: url("images/back40.gif");}
       </style>
   </head>
   ```

3. **内联样式-不推荐**

   ```html
   <p style="color: sienna; margin-left: 20px">
   This is a paragraph
   </p>
   
   ```

4. **多重样式**

   如果某些属性在不同的样式表中被同样的选择器定义，那么属性值将从更具体的样式表中被继承过来.

   同时`内部样式表 `>`外部样式表`

## 二、CSS基本样式

### 2.1 CSS样式-背景

| 属性                  | 描述                                       |
| :-------------------- | :----------------------------------------- |
| background            | 简写属性，作用是将背景属性设置在一个声明中 |
| background-color      | 设置元素的背景颜色                         |
| background-image      | 把图像设置为背景                           |
| background-repeat     | 设置背景图像是否及如何重复                 |
| background-attachment | 背景图像是否固定或者随着页面的其余部分滚动 |
| background-position   | 设置背景图像的起始位置。                   |

1. **[background] 属性**

   ```css
   body{ 
       background: #00ff00 url('smiley.gif') no-repeat fixed center; 
   }
   
   ```

2. **背景颜色-[background-color]**

   ```css
   body{
       background-color:yellow;
   }
   h1{
       background-color:#00ff00;
   }
   p{
       background-color:rgb(255,0,255);
   }
   
   ```

   > CSS中，颜色值通常以以下方式定义:
   >
   > - 十六进制 - 如："#ff0000"
   > - RGB - 如："rgb(255,0,0)"
   > - 颜色名称 - 如："red"

3. **背景图像-[background-image]**

   ```css
   body {
       background-image:url('bgdesert.jpg');
   }
   
   ```

4. **背景图像 - 水平或垂直平铺-[background-repeat]**

   默认情况下 background-image 属性会在页面的水平或者垂直方向平铺.

   ```css
   /* 如果图像只在水平方向平铺 (repeat-x), 页面背景会更好些 */
   body{
       background-image:url('gradient2.png');
       background-repeat:repeat-x;
   }
   
   ```

   ```css
   /* 背景图像- 设置定位与不平铺 */
   body{
       background-image:url('img_tree.png');
       background-repeat:no-repeat;
   }
   
   ```

### 2.2 CSS样式-文本

| 属性            | 描述                     |
| :-------------- | :----------------------- |
| color           | 设置文本颜色             |
| direction       | 设置文本方向             |
| letter-spacing  | 设置字符间距             |
| line-height     | 设置行高                 |
| text-align      | 对齐元素中的文本         |
| text-decoration | 向文本添加修饰           |
| text-indent     | 缩进元素中文本的首行     |
| text-shadow     | 设置文本阴影             |
| text-transform  | 控制元素中的字母         |
| unicode-bidi    | 设置或返回文本是否被重写 |
| vertical-align  | 设置元素的垂直对齐       |
| white-space     | 设置元素中空白的处理方式 |
| word-spacing    | 设置字间距               |

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
<style>
h1{
text-align: center;
text-transform: uppercase;
color: #A7C942;
}
p
{
text-indent: 50px;
text-align:justify;
letter-spacing:3px;
}
a
{
text-decoration:none;
}
</style>
</head>

<body>
<h1>text formatting</h1>
<p>This text is styled with some of the text formatting properties. The heading uses the text-align, text-transform, and color properties.
The paragraph is indented, aligned, and the space between characters is specified. The underline is removed from the
<a target="_blank" href="#">&quot;尝试一下&quot;</a> link.</p>
</body>
</html>

```

### 2.3 CSS样式-字体

| 属性         | 描述                               |
| :----------- | :--------------------------------- |
| font         | 在一个声明中设置所有的字体属性     |
| font-family  | 指定文本的字体系列                 |
| font-size    | 指定文本的字体大小                 |
| font-style   | 指定文本的字体样式                 |
| font-variant | 以小型大写字体或者正常字体显示文本 |
| font-weight  | 指定字体的粗细                     |

### 2.4 CSS样式-链接

链接的样式，可以用任何CSS属性（如颜色，字体，背景等） 

### 2.5 CSS样式-列表

> CSS列表属性作用如下：
>
> - 设置不同的列表项标记为有序列表
> - 设置不同的列表项标记为无序列表
> - 设置列表项标记为图像

| 属性                | 描述                                               |
| :------------------ | :------------------------------------------------- |
| list-style          | 简写属性, 用于把所有用于列表的属性设置于一个声明中 |
| list-style-image    | 将图像设置为列表项标志                             |
| list-style-position | 设置列表中列表项标志的位置                         |
| list-style-type     | 设置列表项标志的类型                               |

```css
ul
{
    list-style-type: none;
    padding: 0px;
    margin: 0px;
}
ul li
{
    background-image: url(sqpurple.gif);
    background-repeat: no-repeat;
    background-position: 0px 5px; 
    padding-left: 14px; 
}

```

### 2.6 CSS样式-表格

- 表格边框

  ```css
  /* 指定了一个表格的Th和TD元素的黑色边框 */
  table, th, td {
      border: 1px solid black;
  }
  
  ```

- 折叠边框

  ```css
  /* 因为表和th/ td元素有独立的边界, 为了显示一个表的单个边框，使用 border-collapse属性 */
  table{
      border-collapse:collapse;
  }
  table,th, td{
      border: 1px solid black;
  }
  
  ```

- 表格宽度和高度

  ```css
  table {
      width:100%;
  }
  th{
      height:50px;
  }
  
  ```

- 表格文字对齐

  ```css
  /* 表格中的文本对齐和垂直对齐属性, text-align属性设置水平对齐方式，向左，右，或中心 */
  td{
      text-align:right;
  }
  
  ```

- 表格填充

  ```css
  /* 表的内容中控制空格之间的边框，应使用td和th元素的填充属性 */
  td{
      padding:15px;
  }
  
  ```

- 表格颜色

  ```css
  /* 指定边框的颜色，和th元素的文本和背景颜色 */
  table, td, th{
      border:1px solid green;
  }
  th{
      background-color:green;
      color:white;
  }
  
  ```

### 2.7 CSS样式-轮廓

轮廓（outline）是绘制于元素周围的一条线，位于边框边缘的外围，可起到突出元素的作用。

CSS outline 属性规定元素轮廓的样式、颜色和宽度。

| 属性          | 描述                           |
| :------------ | :----------------------------- |
| outline       | 在一个声明中设置所有的轮廓属性 |
| outline-color | 设置轮廓的颜色                 |
| outline-style | 设置轮廓的样式                 |
| outline-width | 设置轮廓的宽度                 |

## 三、 CSS定位

> 一切皆为框

 CSS 定位 (Positioning) 属性允许你对元素进行定位 

### 3.1 CSS定位-定位

### 3.2 CSS定位-浮动

## 四、CSS盒子模型

### 4.1 盒子模型详解

​		在 CSS 盒子模型中，每个的 HTML 元素都会被当作是一个矩形的盒子，然后对它们进行从上到下，从左到右的布局。 一个盒子通常包括四个区域，从里到外分别是：

- 内容区域 - 代表盒子的实际内容部分，它是由 width 宽度和 height 高度来确定的
- 内间距区域 - 代表盒子与实际内容之间的空白区域，由 padding 属性设置
- 边框区域 - 代表盒子的边框，是内间距区域和外边距区域的边界，由 border 属性设置
- 外边距区域 - 代表此盒子的边框与相邻的其他盒子边框之间的距离，由 margin 属性设置

![](https://gitee.com/minimalism_jyq/image-hosting-service/raw/master/CSS%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0/%E7%9B%92%E5%AD%90%E6%A8%A1%E5%9E%8B.png) 

### 4.2 盒子的类型

CSS 中的盒子模型有两种类型，一种是 content-box，内容盒子，一种是 border-box 边框盒子，通过 css 属性 box-sizing 来设置. 这两种盒子计算宽高的方式是不同的.

1. **content-box**

   > content-box 是 box-sizing 的默认值，也就是说所有的盒子默认都是内容盒子，那么这里 css 属性中的 width 和 height 设置的是它内容区域的宽高，而盒子的宽高需要加上内间距和边框，外边距不算在内。

   *宽度的计算方式是：内容的宽度+左右内间距+左右边框的宽度*

   *高度的计算方式则是：内容的高度+上下内间距+上下边框的宽度*

   ```html
   <div class="box"></div>
   ```

   ```css
   <!-- 盒子的宽高需要加上内间距和边框，外边距不算在内 -->
   .box {
       <!-- width 和 height 设置的是它内容区域的宽高 -->
       width:300px;
       height:200px;
       padding:10px;
       border:5px solid lightblue;
       margin:20px;
   }
   
   ```
2. **border-box**

   > 如果把 box-sizing 的值改成 border-box，那么 width 和 height 属性就是分别设置盒子的最终宽度和高度 

   ```css
   .box {
     box-sizing: border-box; /* ... */
   }
   ```

### 4.3 CSS盒子模型-盒子模型应用

## 五、CSS选择器详解

## 六、CSS常用操作

## 七、CSS3基本操作

