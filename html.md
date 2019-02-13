# 前端学习基础

**注：** *以下仅为作者学习前端过程的一些基础笔记*
--------
## HTML的学习

- HTML的标签
   - `<!DOCTYPE html>` 声明为 HTML5 文档
   - `<html>` 元素是 HTML 页面的根元素
   -  `<head>` 元素包含了文档的元（meta）数据，如 <meta
   charset="utf-8"> 定义网页编码格式为 utf-8。
   - `<title>` 元素描述了文档的标题
   - `<body>` 元素包含了可见的页面内容
- 基本的HTML文档格式
 ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>这是标题</title>
    </head>
    <body>
            这是内容
    </body>
    </html>
  ```
- **`<head>`标签**

  `<head>` 元素包含了所有的头部标签元素。在 `<head>`元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息。可以添加在头部区域的元素标签为: `<title>`, `<style>`, `<meta>`, `<link>`, `<script>`,` <noscript>`, and `<base>`.
- **`<title>`标签**
   
   `<title>` 标签定义了不同文档的标题, 在 HTML/XHTML 文档中是必须的。
   
   `<title>`元素：
   - 定义了浏览器工具栏的标题
   - 当网页添加到收藏夹时，显示在收藏夹中的标题
   - 显示在搜索引擎结果页面的标题
 - **`<body>`标签里的元素简介**
    - 标题

      - HTML 标题（Heading）是通过`<h1> - <h6>` 标签来定义的.

      实例：
      ```html
      <h1>一级标题</h1>
      <h2>二级标题</h2>
      <h3>三级标题</h3>
      <h4>四级标题</h4>
      <h5>五级标题</h5>
      <h6>六级标题</h6>
      ```
      ![图片展示](https://i.loli.net/2019/01/26/5c4c66076b582.png)
      **注：** *标题是黑体，按照1-6依次减小，且浏览器会自动地在标题的前后添加空行。*
    - 段落
       - HTML 段落是通过标签` <p>` 来定义的.

       实例：
       ```html
      <p>这是一个段落。</p>
      <p>这是另外一个段落。</p>
      ```
      ![2.png](https://i.loli.net/2019/01/26/5c4c665051c71.png)
      **注：** *HTML输出格式问题：当显示页面时，浏览器会移除源代码中多余的空格和空行。所有连续的空格或空行都会被算作一个空格。需要注意的是，HTML 代码中的所有连续的空行（换行）也被显示为一个空格。*
    - 超链接
       - HTML 超链接是通过标签 `<a>` 来定义的
      
         语法：`<a href="url">链接文本</a>`

         实例：
       ```html
       <a href="http://www.runoob.com">这是一个链接</a>
       ```
       ![3.png](https://i.loli.net/2019/01/26/5c4c66f4b7e8c.png)
       - 超链接 —— target属性：使用 target 属性，你可以定义被链接的文档在何处显示。

         实例：
       ```html
       <a href="https://Anna521.github.io/" target="_blank">访问博客</a>
       ```
       - 超链接 —— id属性：id属性可用于创建在一个HTML文档书签标记。
         
         实例：
           
         在html文档中插入id
         ```html
         <a id="tips">有用的提示部分</a>
         ```
         在HTML文档中创建一个链接到"有用的提示部分(id="tips"）"：
         ```html
         <a href="#tips">访问有用的提示部分</a>
         ```
         或者，从另一个页面创建一个链接到"有用的提示部分(id="tips"）"：
         ```html
         <a href="http://www.runoob.com/html/html-links.html#tips">
         访问有用的提示部分</a>
         ```
         **注**: *书签是不以任何特殊的方式显示，在HTML文档中是不显示的，所以对于读者来说是隐藏的。*

    - 换行
       - HTML 换行是通过标签`<br>`来定义的。在写完一个内容想要进行换行的话，因为浏览器会把空行当作一个空格，所以打回车是不能进行换行的，所以这时需要`<br>`进行换行的操作，并且这个标签也可以在想不产生一个新段落的情况下进行换行（新行）时使用
       ```html
       <p>这个<br>段落<br>演示了分行的效果</p>
       ```
       ![4.png](https://i.loli.net/2019/01/26/5c4c675325272.png)
       **注：** *`<br\>`元素是一个空的 HTML 元素。由于关闭标签没有任何意义，因此它没有结束标签。*
    - 图像
       - HTML 图像是通过标签 `<img>` 来定义的

         语法：
         ```html
         <img src="url" alt="some_text">
         ```
         实例：
         ```html
         <img src="https://i.loli.net/2019/01/30/5c515c51ee2a2.jpg" alt="4_94241_8.jpg" title="4_94241_8.jpg" />
         ```
         ![13.png](https://i.loli.net/2019/01/30/5c515d02569a7.png)
       **注:** *图像的名称和尺寸是以属性的形式提供的。*

       - 图像 —— src属性：要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址。
       - 图像 —— alt属性：alt 属性用来为图像定义一串预备的可替换的文本。替换文本属性的值是用户定义的。在浏览器无法载入图像时，替换文本属性告诉读者她们失去的信息。此时，浏览器将显示这个替代性的文本而不是图像。为页面上的图像都加上替换文本属性是个好习惯，这样有助于更好的显示信息，并且对于那些使用纯文本浏览器的人来说是非常有用的。
       - 图像 —— width与height属性：height（高度） 与 width（宽度）属性用于设置图像的高度与宽度。指定图像的高度和宽度是一个很好的习惯。如果图像指定了高度宽度，页面加载时就会保留指定的尺寸。如果没有指定图片的大小，加载页面时有可能会破坏HTML页面的整体布局。
   - 注释
      - HTML 注释是通过标签`<!-- -->`来定义的，注释可以增强文章的可读性
      ```html
      <!--我是注释-->
      ```
   - 水平线
      - HTML 水平线是通过`<hr>`来定义的,水平线可以分割内容，使所写文章具有层次感
      ```html
      <p>这是一个段落。</p>
      <hr>
      <p>这是一个段落。</p>
      <hr>
      <p>这是一个段落。</p>
      ```
      ![6.png](https://i.loli.net/2019/01/26/5c4c694fce3fb.png)
   - 文本格式化
      - 粗体：粗体是通过`<b>`来定义的
      ```html
      <b>粗体</b>
      ```
      - 斜体：斜体是通过`<i>`来定义的
      ```html
      <i>斜体</i>
      ```
      **注：** *通常标签` <strong>` 替换加粗标签` <b> `来使用, `<em> `替换 `<i>`标签使用。然而，这些标签的含义是不同的：`<b>` 与`<i> `定义粗体或斜体文本,而`<strong>` 或者`<em>`意味着你要呈现的文本是重要的，所以要突出显示。现今所有主要浏览器都能渲染各种效果的字体。不过，未来浏览器可能会支持更好的渲染效果。*
      - 小号字：小号字是通过`<small>`来定义的
      ```html
      <small>小号字</small>
      ```
      - 下标字：下标字是通过`<sub>`来定义的
      ```html
      <sub>下标字</sub>
      ```
      - 上标字：上标字是通过`<sup>`来定义的
      ```html
      <sup>上标字</sup>
      ```
      - 插入字与删除字：插入字是用`<ins>`,删除字是用`<del>`来定义的,一般插入字与删除字是一起连用的
      ```html
      <p>My favorite color is <del>blue</del> <ins>red</ins>!</p>
      ```
      ![7.png](https://i.loli.net/2019/01/26/5c4c6a7ac92f2.png)
      - 计算机输出标签
         - 计算机代码：`<code> `标签是一个短语标签，用来定义计算机代码文本。
         - 键盘码：`<kbd>` 标签定义键盘文本,但` <kbd>` 标签已废弃，不推荐使用，但是可以通过CSS实现丰富的效果。
         - 计算机程序样本文本：`<samp>` 标签是一个短语标签，用来定义计算机程序的样本文本.
         - 变量：变量是用`var`定义的
         - 预格式文本：预格式文本是用`pre`来定义的，被包围在 `<pre>` 标签,元素中的文本通常会保留空格和换行符。而文本也会呈现为等宽字体。
      - 缩写：缩写是用`<abbr>`来定义的，`<abbr> `标签用来表示一个缩写词或者首字母缩略词，如"WWW"或者"NATO"。
      ```html
      The<abbr title="World Health Organization">WHO</abbr> was founded in 1948.
      ```
      ![8.png](https://i.loli.net/2019/01/26/5c4c6b7f6432b.png)
      - 地址：地址是用`address`来定义的，`<address> `标签定义文档作者/所有者的联系信息。
      ```html
      <address>
      Written by <a href="mailto:webmaster@example.com">Jon Doe</a>.<br>
      Visit us at:<br>
      Example.com<br>
      Box 564, Disneyland<br>
      USA
      </address>
      ```
      ![9.png](https://i.loli.net/2019/01/26/5c4c6be329ad1.png)
      **注：** *如果 `<address>` 元素位于 `<body>` 元素内部，则它表示该文档作者/所有者的联系信息。如果 `<address>` 元素位于`<article>` 元素内部，则它表示该文章作者/所有者的联系信息。`<address>` 元素的文本通常呈现为斜体。大多数浏览器会在该元素的前后添加换行。不应该使用` <address> `标签来描述邮政地址，除非这些信息是联系信息的组成部分。*
      - 文本方向：文本方向是用`bdo`来定义的，`<bdo>` 标签用来覆盖默认的文本方向。
      ```html
      <p>该段落文字从左到右显示。</p>
      <p><bdo dir="rtl">该段落文字从右到左显示。</bdo></p>
      ```
      ![5.png](https://i.loli.net/2019/01/26/5c4c68f0aeea8.png)
      - 长引用：长引用是用`<blockquote>`来定义的
      ```html
      <blockquote cite="http://www.worldwildlife.org/who/index.html">
      For 50 years, WWF has been protecting the future of nature. The world's leading conservation organization, WWF works in 100 countries and is supported by 1.2 million members in the United States and close to 5 million globally.
      </blockquote>
      ```
      ![10.png](https://i.loli.net/2019/01/26/5c4c6fa78d4bc.png)
      **注：** *`<blockquote>` 标签定义摘自另一个源的块引用。浏览器通常会对 `<blockquote>` 元素进行缩进。*
      - 短引用：短引用是用`<q>`来定义的
      ```html
      <p>WWF's goal is to: 
     <q>Build a future where people live in harmony with nature.</q>
     We hope they succeed.</p>
     ```
     ![11.png](https://i.loli.net/2019/01/26/5c4c7155c34a1.png)
    
     **注：** *`<q> `标签定义一个短的引用。浏览器经常会在这种引用的周围插入引号。*
     - 引用、引证：引用与引证是用`<cite>`来定义的`<cite> `标签定义作品（比如书籍、歌曲、电影、电视节目、绘画、雕塑等等）的标题。
     ```html
     <p><cite>The Scream</cite> by Edward Munch. Painted in 1893.</p>
     ```
     ![12.png](https://i.loli.net/2019/01/26/5c4c72f88d4d4.png)
     - 定义项目：定义项目是用`<dfn>`来定义的
   - 表格
      - 表格由 `<table>` 标签来定义。每个表格均有若干行（由 `<tr>` 标签定义），每行被分割为若干单元格（由 `<td>` 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。表格的表头（由`<th>`定义）大多数浏览器会把表头显示为粗体居中的文本。表格的标题可用`<caption>`标签来定义。
      ```html
      <table border="1">
      <tr>
      <th>Header 1</th>
      <th>Header 2</th>
      </tr>
      <tr>
      <td>row 1, cell 1</td>
      <td>row 1, cell 2</td>
      </tr>
      <tr>
      <td>row 2, cell 1</td>
      <td>row 2, cell 2</td>
      </tr>
      </table>
      ```
      ![15.png](https://i.loli.net/2019/01/30/5c5174f1795bd.png)
      - 表格 —— border属性：border是边框属性，很有用，可用它来产生边框
      - 表格 —— colspan属性：定义单元格跨行，放在所要跨行那个表格的标签里，并要指明跨行个数
      - 表格 —— rowspan属性：定义单元格跨列，放在所要跨列那个表格的标签里，并要指明跨列个数
      - 表格 —— cellpadding属性：定义单元格边距
      ```html
      <h4>没有单元格边距:</h4>
      <table border="1">
      <tr>
        <td>First</td>
        <td>Row</td>
      </tr>   
      <tr>
        <td>Second</td>
        <td>Row</td>
      </tr>
      </table>

      <h4>有单元格边距:</h4>
      <table border="1" 
      cellpadding="10">
      <tr>
        <td>First</td>
        <td>Row</td>
      </tr>   
      <tr>
        <td>Second</td>
        <td>Row</td>
     </tr>
     </table>
     ```
     ![17.png](https://i.loli.net/2019/01/30/5c5179d6d0ff0.png)
      - 表格 —— cellspacing属性：定义单元格间距
      ```html
      <h4>没有单元格间距:</h4>
      <table border="1">
      <tr>
      <td>First</td>
      <td>Row</td>
      </tr>
      <tr>
      <td>Second</td>
      <td>Row</td>
      </tr>
      </table>
      ```
      ![16.png](https://i.loli.net/2019/01/30/5c5178c251a97.png)
   - 列表
    
     列表由`<li>`标签定义，分为无序列表,有序列表与自定义列表三种：
      - 无序列表：无序列表是一个项目的列表，此列项目使用粗体圆点（典型的小黑圆圈）进行标记。无序列表使用 `<ul>` 标签
      ```html
      <ul>
      <li>Coffee</li>
      <li>Milk</li>
      </ul>
      ```
      ![18.png](https://i.loli.net/2019/01/30/5c517b586cabf.png)
      - 有序列表：同样，有序列表也是一列项目，列表项目使用数字进行标记。 有序列表使用` <ol>` 标签。
      ```html
      <ol>
      <li>Coffee</li>
      <li>Milk</li>
      </ol>
      ```
     ![19.png](https://i.loli.net/2019/01/30/5c517bfe9cb03.png) 
     - 自定义列表：不同于有序和无序列表是由`<li>`标签开始与结束，自定义列表以 `<dl>` 标签开始与结束。每个自定义列表项以` <dt`> 开始。每个自定义列表项的定义以 `<dd>` 开始。
     ```html
     <dl>
     <dt>Coffee</dt>
     <dd>- black hot drink</dd>
     <dt>Milk</dt>
     <dd>- white cold drink</dd>
     </dl>
     ```
     ![20.png](https://i.loli.net/2019/01/30/5c517d8303d3d.png)
     
     **注：** *自定义列表不仅仅是一列项目，而是项目及其注释的组合。*
     - 列表 —— type属性：在有序列表`<ol>`标签中可增加type属性，可使标记符号由数字变为诸如大写字母等其他的符号
        ```html
        <h4>大写字母列表：</h4>
        <ol type="A">
        <li>Apples</li>
        <li>Bananas</li>
        <li>Lemons</li>
        <li>Oranges</li>
        </ol>
        ```
        ![21.png](https://i.loli.net/2019/01/30/5c517f354f9c6.png)
      - 列表 —— style属性：同样的，在无序列表`<ul>`标签中可用style属性来改变标记符号，例如：
      ```html
      圆点列表：<ul style="list-style-type:disc">
      圆圈列表：<ul style="list-style-type:circle">
      正方形列表：<ul style="list-style-type:square">
      ```
- **html头部**
   - **`<base>`标签：**`<base>` 标签描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的默认链接。
   ```html
   <head>
   <base href="http://www.runoob.com/images/" target="_blank">
   </head>
   ```
   - **`<link>`标签:**`<link> `标签定义了文档与外部资源之间的关系，`<link>` 标签通常用于链接到样式表:
   ```html
   <head>
   <link rel="stylesheet" type="text/css" href="mystyle.css">
   </head>
   ```
   - **`<style>`标签：**`<style>` 标签定义了HTML文档的样式文件引用地址,在`<style>` 元素中你也可以直接添加样式来渲染 HTML 文档:

     语法：
   ```html
   <head>
   <style type="text/css">
   body {background-color:yellow}
   p {color:blue}
   </style>
   </head>
   ```
     实例：
     ```html
     <!DOCTYPE html>
     <html>
     <head>
     <meta charset="utf-8"> 
     <title>菜鸟教程(runoob.com)</title>
     <style type="text/css">
     h1 {color:red;}
     p {color:blue;}
     </style>
     </head>

     <body>
     <h1>这是一个标题</h1>
     <p>这是一个段落。</p>
     </body>

     </html>
     ```
     ![14.png](https://i.loli.net/2019/01/30/5c5169f4eeacb.png)

   - **`<meta>`标签：**`<meta>`标签描述了一些基本的元数据。`<meta>` 标签提供了元数据.元数据也不显示在页面上，但会被浏览器解析。META 元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。元数据可以使用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他Web服务。`<meta>` 一般放置于 `<head>` 区域。实例如下：
      - 为搜索引擎定义关键词:
      ```html
      <meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">
      ```
      - 为网页定义描述内容
      ```html
      <meta name="description" content="免费 Web & 编程 教程">
      ```
      - 定义网页作者:
      ```html
      <meta name="author" content="Runoob">
      ```
      - 每30秒钟刷新当前页面:
      ```html
      <meta http-equiv="refresh" content="30">
      ```
- html区块
   
   大多数 HTML 元素被定义为块级元素或内联元素。

   块级元素在浏览器显示时，通常会以新行来开始（和结束）。比如: `<h1>`,`<p>`, `<ul>`, `<table>`

   内联元素在显示时通常不会以新行开始。比如: `<b>`,`<td>`, `<a>`, `<img>`
   - **`<div>`标签：**`<div>` 标签定义 HTML 文档中的一个分隔区块或者一个区域部分。`<div>`标签常用于组合块级元素，以便通过 CSS 来对这些元素进行格式化。
   ```html
   <div style="color:#0000FF">
   <h3>这是一个在 div 元素中的标题。</h3>
   <p>这是一个在 div 元素中的文本。</p>
   </div>
   ```
   ![22.png](https://i.loli.net/2019/01/30/5c51861446658.png)
   
   提示：`<div>` 元素经常与 CSS 一起使用，用来布局网页。
   
   注释：默认情况下，浏览器通常会在 `<div>` 元素前后放置一个换行符。然而，您可以通过使用 CSS 改变这种情况。
   - **`<span>`标签：** HTML` <span> `元素是内联元素，可用作文本的容器。`<span> `元素也没有特定的含义。当与 CSS 一同使用时，`<span>` 元素可用于为部分文本设置样式属性。`<span>` 标签提供了一种将文本的一部分或者文档的一部分独立出来的方式。
   ```html
   <p>我的母亲有 <span style="color:blue">蓝色</span> 的眼睛。</p>
   ```
   ![2.png](https://i.loli.net/2019/01/30/5c5187f5c5d23.png)
- 布局
  - 使用`<div>`元素
  ```html
  <!DOCTYPE html>
  <html>
  <head> 
  <meta charset="utf-8"> 
  <title>菜鸟教程(runoob.com)</title> 
  </head>
  <body>
  <div id="container" style="width:500px">
  <div id="header" style="background-color:#FFA500;">
  <h1 style="margin-bottom:0;">主要的网页标题</h1></div>
  <div id="menu" style="background-color:#FFD700;height:200px;width:100px;float:left;">
  <b>菜单</b><br>
  HTML<br>
  CSS<br>
  JavaScript</div>
  <div id="content" style="background-color:#EEEEEE;height:200px;width:400px;float:left;">
  内容在这里</div>
  <div id="footer" style="background-color:#FFA500;clear:both;text-align:center;">
  版权 © runoob.com</div>
  </div>
  </body>
  </html>
  ```
  <img src="https://i.loli.net/2019/02/13/5c63b578c65fe.png" alt="23.png" title="23.png" />

  - 使用`<table>`元素
  ```html
  <!DOCTYPE html>
  <html>
  <head> 
  <meta charset="utf-8"> 
  <title>菜鸟教程(runoob.com)</title> 
  </head>
  <body>
  <table width="500" border="0">
  <tr>
  <td colspan="2" style="background-color:#FFA500;">
  <h1>主要的网页标题</h1>
  </td>
  </tr>
  <tr>
  <td style="background-color:#FFD700;width:100px;">
  <b>菜单</b><br>
  HTML<br>
  CSS<br>
  JavaScript
  </td>
  <td style="background-color:#eeeeee;height:200px;width:400px;">
  内容在这里</td>
  </tr>
  <tr>
  <td colspan="2" style="background-color:#FFA500;text-align:center;">
  版权 © runoob.com</td>
  </tr>
  </table>
  </body>
  </html>
  ```
  <img src="https://i.loli.net/2019/02/13/5c63b578c65fe.png" alt="23.png" title="23.png" />
  
  **注：** *虽然我们可以使用HTML table标签来设计出漂亮的布局，但是table标签是不建议作为布局工具使用的 - 表格不是布局工具。*
  
  **提示：** *HTML布局一般使用CSS， 使用 CSS 最大的好处是，如果把 CSS 代码存放到外部样式表中，那么站点会更易于维护。通过编辑单一的文件，就可以改变所有页面的布局。*
- 表单
  
  - 表单是使用表单标签 `<form>` 来设置的：表单是一个包含表单元素的区域。表单元素是允许用户在表单中输入内容,比如：文本域(textarea)、下拉列表、单选框(radio-buttons)、复选框(checkboxes)等等。
    
    语法：
    ```html
    <form>
    .
    input 元素
    .
    </form>
    ```
  - 文本域：文本域通过`<input type="text">` 标签来设定，当用户要在表单中键入字母、数字等内容时，就会用到文本域。
  ```html
  <form>
  First name: <input type="text" name="firstname"><br>
  Last name: <input type="text" name="lastname">
  </form>
  ```
  <img src="https://i.loli.net/2019/02/13/5c63bdd4b5faf.png" alt="24.png" title="24.png" />

    另；多行文本输入控件
    ```html
    <textarea rows="10" cols="30">
    我是一个文本框。
    </textarea>
    ```
  <img src="https://i.loli.net/2019/02/13/5c63d62875bfa.png" alt="29.png" title="29.png" />

  - 密码字段：密码字段通过标签`<input type="password"> `来定义:
   ```html
    <form>
    Password: <input type="password" name="pwd">
    </form>
    ```
  <img src="https://i.loli.net/2019/02/13/5c63c25d0b097.png" alt="24.png" title="24.png" />

  - 单选按钮：`<input type="radio">` 标签定义了表单单选框选项
  ```html
  <form>
  <input type="radio" name="sex" value="male">Male<br>
  <input type="radio" name="sex" value="female">Female
  </form>
  ```
  <img src="https://i.loli.net/2019/02/13/5c63c3a9d236f.png" alt="25.png" title="25.png" />

  - 复选框：`<input type="checkbox">` 定义了复选框. 用户需要从若干给定的选择中选取一个或若干选项。
  ```html
  <form>
  <input type="checkbox" name="vehicle" value="Bike">I have a bike<br>
  <input type="checkbox" name="vehicle" value="Car">I have a car 
  </form>
  ```
  <img src="https://i.loli.net/2019/02/13/5c63c46df2b80.png" alt="26.png" title="26.png" />

  - 提交按钮：`<input type="submit">` 定义了提交按钮：当用户单击确认按钮时，表单的内容会被传送到另一个文件。表单的动作属性定义了目的文件的文件名。由动作属性定义的这个文件通常会对接收到的输入数据进行相关的处理。
  ```html
  <form name="input" action="html_form_action.php" method="get">
  Username: <input type="text" name="user">
  <input type="submit" value="Submit">
  </form> 
  ```
  <img src="https://i.loli.net/2019/02/13/5c63c8b9bb7f0.png" alt="27.png" title="27.png" />

  - 下拉列表：`<select>`与`<option value = option>`定义了下拉列表
  ```html
  <form action="">
  <select name="cars">
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="fiat" selected>Fiat</option>
  <option value="audi">Audi</option>
  </select>
  </form>
  ```
  <img src="https://i.loli.net/2019/02/13/5c63d47617c4c.png" alt="28.png" title="28.png" />

  - 创建按钮：`<input type="button" value="xx">`定义了按钮
  ```html
  <form action="">
  <input type="button" value="Hello world!">
  </form>
  ```
- 框架
  - 框架是通过`<iframe>`来定义的
    
    语法：
    ```html
    <iframe src="URL"></iframe>
    ```
  - Iframe——设置高度与宽度：height 和 width 属性用来定义iframe标签的高度与宽度。
  ```html
  <iframe src="demo_iframe.htm" width="200" height="200"></iframe>
  ```
  - Iframe——移除边框：frameborder 属性用于定义iframe表示是否显示边框。
  ```html
  <iframe src="demo_iframe.htm" frameborder="0"></iframe>
  ```
  - 使用iframe来显示目标链接页面:iframe可以显示一个目标链接的页面
  ```html
  <iframe src="demo_iframe.htm" name="iframe_a"></iframe>
  <p><a href="http://www.runoob.com" target="iframe_a">RUNOOB.COM</a></p>
  ```














   


