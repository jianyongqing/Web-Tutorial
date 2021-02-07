# 一、HTML概述

## 1.1 什么是HTML?

>  HTML是用来描述网页的一种语言.
>
>  - HTML 指的是超文本标记语言 (Hyper Text Markup Language)
>  - HTML 不是一种编程语言，而是一种标记语言 (markup language)
>  - 标记语言是一套标记标签 (markup tag)
>  - HTML 使用标记标签来描述网页

## 1.2 web2.0简述

> Web2.0是目前主流的Web页面开发标准

Web2.0对Web页面构成的描述：

- `结构`：数据的组织形式，实现方式：HTML 超文本标记语言
- `表现`：数据的表现形式，实现方式：CSS 层叠样式表
- `行为`：用户交互动作，实现方式： JavaScript 脚本文件

## 1.3 HTML 文档的构成 

```html
<!DOCTYPE html> <!--文档类型声明-->
<html lang="en">
    <head>
	      <meta charset="UTF-8"> <!--元信息-->
	      <title>页面标题</title> <!--页面标题-->
    </head>
    <body>
	      <!--body主体内容-->
    </body>
</html>
```

## 1.4 HTML 注释 

定义注释:

```html
<!--HTML注释内容-->
```

## 1.5 HTML文档规范

# 二、HTML基本语法

## 2.1 HTML基本标签

1. **标题**

HTML标题（Heading）是通过 `<h1>` - `<h6>`等标签进行定义的.

```html
<h1>...</h1>
<h2>...</h2>
    ...
<h6>...</h6>
```

2. **段落**

`<p>`标签进行定义定义段落.

```html
<p>...</p>
```

3. **超链接**

`<a>`标签定义链接.

```html
<a href="http://www.w3school.com.cn">This is a link</a>
```

4. **图像**

`<img>`标签定义图像.

```html
<img src="w3school.jpg" width="104" height="142" />
```

## 2.2 HTML元素、属性和格式化

1. **HTML元素**

- HTML 元素指的是从开始标签（start tag）到结束标签（end tag）的所有代码。

| 开始标签 |      元素内容       | 结束标签 |
| :------: | :-----------------: | :------: |
|  `<p>`   | This is a paragraph |  `</p>`  |
| `<br />` |                     |          |

> 注释：开始标签常被称为开放标签（opening tag），结束标签常称为闭合标签（closing tag）。

- HTML元素语法

  > 元素的内容是开始标签与结束标签之间的内容
  > 空元素在开始标签中进行关闭（以开始标签的结束而结束）
  > 大多数 HTML 元素可拥有属性

- 嵌套的 HTML 元素

大多数 HTML 元素可以嵌套（可以包含其他 HTML 元素）。

2. **HTML属性**

- 标签可以拥有属性。属性提供了有关 HTML 元素的更多的信息。

- 属性总是以名称/值对的形式出现   如：name="value"。

- 常用标签属性

  ```html
  <h1>:alignd对齐方式
  <body>:bgcolor背景颜色
  <a>:target规定在何处打开链接
  ```

- 通用属性

  ```html
  class:规定元素的类名
  id:规定元素唯一ID
  style:规定元素的样式
  title:规定元素的额外信息
  ```

3. **HTML格式化**

- 文本格式化标签

|    标签    |     描述     |
| :--------: | :----------: |
|   `<b>`    | 定义粗体文本 |
|  `<big>`   |  定义大号字  |
|   `<em>`   | 定义着重文字 |
|   `<i>`    |  定义斜体字  |
| `<small>`  |  定义小号字  |
| `<strong>` | 定义加重语气 |
|  `<sub>`   |  定义下标字  |
|  `<sup>`   |  定义上标字  |
|  `<ins>`   |  定义插入字  |
|  `<del>`   |  定义删除字  |

## 2.3 HTML样式、链接和表格

1. **HTML样式**

   ```html
   1.标签
   <style>:样式定义
   <link>:资源引用
   2.属性
   rel="stylesheet":外部样式表
   type="text/css":引入文档的类型
   margin-left:边距
   
   ```

2. **HTML链接**

   ```html
   1.链接数据:
       文本链接
   	图片链接
   2.属性:
   	href属性:指向另一个文档的链接
   	name属性:创建文档内的链接
   3.img标签属性:
   	alt:替换文本属性
   
   ```

```html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>链接</title>
</head>
<body>
    <!--文本链接-->
    <a href="http://baidu.com">点击我</a>

    <br/>

    <!--图片链接-->
    <a href="http://baidu.com"><img src="00.png" width="200px" height="200px" alt="logo"></a>
    
    <br/>

    <!--文档内链接-->
    <a name="tips">hello</a>
    <a href="#tips">跳转到hello</a>
</body>
</html>

```

3. **HTML表格**

表格标签:

|     表格     |         描述         |
| :----------: | :------------------: |
|  `<table>`   |       定义表格       |
| `<caption>`  |     定义表格标题     |
|    `<th>`    |    定义表格的表头    |
|    `<tr>`    |     定义表格的行     |
|    `<td>`    |     定义表格单元     |
|  `<thead>`   |    定义表格的页眉    |
|  `<tbody>`   |    定义表格的主体    |
|  `<tfoot>`   |    定义表格的页脚    |
|   `<col>`    | 定义用于表格列的属性 |
| `<colgroup>` |    定义表格列的组    |

```html
<!DOctype html>
<html>
    <head>
        <meta http-equiv="Content-Type" content="text/html;charser=UTF-8">
        <title>表格制作</title>
    </head>
    <body>
        <style type="text/css">
            table {
                background-color: red;
                border-spacing:1px;
            }
            th,td{
                background-color: white;
            }
        </style>
        <table>
            <caption>学生成绩</caption>
            <tr>
                <th>学号</th><th>姓名</th><th>科目</th><th>成绩</th>
            </tr>
            <tr>
                <td>001</td><td>王明</td><td>高数</td><td rowspan="2">97</td>
            </tr>
            <tr>
                <td>002</td><td>徐华</td><td>C++</td>
            </tr>
            <tr>
                <td>003</td><td>赵菊</td><td colspan="2">高数</td>
            </tr>
        </table>

        <br/>

        <table cellpadding="10">
            <caption>表格内的标签</caption>
            <tr>
                <td>表格1</td>
                <td>表格2</td>
            </tr>
            <tr>
                <td>
                    <ul>
                        <li>苹果</li>
                        <li>菠萝</li>
                        <li>香蕉</li>
                    </ul>
                </td>
                <td>
                    你想吃啥?
                </td>
            </tr>
        </table>
    </body>
</html>

```

## 2.4 HTML列表、块和布局

1. **列表**

- 无序列表
               

      使用标签:<ul>、<li>
      属性:disc、circle、square
      

- 有序列表

      使用标签:<ol>、<li>
      属性:A、a、I、i、start
      

- 嵌套列表

      使用标签:<ul>、<ol>、<li>
      

- 定义列表

      使用标签:<dl>、<dt>、<dd>
      

```html
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>列表</title>
</head>
<body>
    <!--无序列表-->
    <ul type="square">
        <li>ios</li>
        <li>android</li>
        <li>html5</li>
        <li>swift</li>
    </ul>
    
    <!--有序列表-->
    <ol start="10">
        <li>ios</li>
        <li>android</li>
        <li>html5</li>
        <li>swift</li>
    </ol>

    <!--嵌套列表-->
    <ul>
        <li>宠物</li>
            <ol>
                <li>猫咪</li>
                <li>小狗</li>
            </ol>
        <li>人类</li>
            <ol>
                <li>英国人</li>
                <li>法国人</li>
            </ol>
    </ul>

    <!--自定义列表-->
    <dl>
        <dt>helloworld</dt>
            <dd>每一门新的语言都会打印helloworld</dd>
        <dt>helloworld</dt>
            <dd>每一门新的语言都会打印helloworld</dd>
        <dt>helloworld</dt>
            <dd>每一门新的语言都会打印helloworld</dd>
    </dl>
</body>
</html>

```

2. **块**

3. **布局**

## 2.5 HTML表单提交

`<form>`...`</form>`标签定义表单.

## 2.6 HTML框架、背景和实体

# 三、HTML5基本操作
