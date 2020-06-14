HTML 和CSS





html基本结构

1.不成对出现的标签

 `<br>` `<hr>`  `<meta>` `<img>`  `<input..>`  `<option..>`  `<link>`

2.HTML 基本标签的讲解：

- `<html>` `<head>` `<body>`标签

- `<h1>`----`<h6>`仅仅用于标题文本，不要为了产生粗体文本使用它们

- <p>标签  段落标签

- `<strong><b>`标签

- 都会让文字产生加粗效果

  - `<strong>`用于强调文本，强度更深，表示重要文本--->用于`SEO`优化
  - `<b>`只是视觉加粗效果--->单纯为了产生加粗

`<em>` `<i>`标签

- `em`用于强调文本
- `i`只是视觉斜体效果
- `<strong>`比`<em>`强调更强

特殊符号：

- `&nbsp`; ---->空格
- `&gt`; --->大于号
- `&lt`；--->小于号
- `&quot`；--->引号
- `&copy`;-->版权号 

### HTMl基本标签

`span`标签

- 对被用来组合文档中的行内元素
- 注意：span没有固定的格式表现，当对它应用样式时，才会产生视觉上的变化

`pre`标签

- 文字的格式按源码的排版来显示，我们称之为预处理格式

`a`标签--->他有一个必不可少的属性 href

- `target`属性：
- `_self`(在原来页面打开)
- `_blank`（新窗口打开）
- `_top`（打开时忽略所有的框架）
- `_parent`（在父窗口中打开）

创建锚点和锚链接

- 锚点也是一种超链接，是页面内进行跳转的超链接

  第一步：创建锚点 `<a name="锚点名称"></a>`

  第二步：使用创建好的锚点名称 `<a href="#锚点名称">内容</a>`

`marquee`标签

- 可以创建一个内容滚动效果


```
<marquee direction="down" loop="4" onmouseover=this.stop() onmouseout=this.start()></marquee>
```

- `direction` 表示滚动方向，取值有（left,right,up,down,默认left）

- `loop`表示滚动循环的次数，默认为无限循环

  ```
  onmouseover=this.stop()  onmouseover=this.start()  scrollamout="1"(滚动速度)
  ```

- 表示当鼠标移上区域的时候停止滚动，鼠标移开继续滚动

####  img图片标签与路径

------

- 图片标签与路径：
  - 常见图片格式 `jpg` `png` `gif`
  - `Gif`     （只支持全透明）
  - `Jpeg` /`jpg`
  - `Png` 半/全透明都支持
- 图片标签写法 ：
  - `<img src="" alt="" width="" height="" />`
- 图片四要素：
  - `src=""`        图片路径
  - `alt=""`       图片含义
  - `width=""`     图片宽度 和图片大小保持一致
  - `height=""`     图片高度 和图片大小保持一致
  - `title=""`
- 路径知识：
  - 相对路径、绝对路径：
    - 相对路径：(Relative Path) 相对于该文件的路径；
    - 绝对路径：(Absolute Path) 从磁盘出发的路径；
  - <img src="" …… align="" /> align属性--设置图片与后面文字的位置关系 值--top、bottom、middle、absmiddle、left、right
- 在静态页面中：
  - `/`开头表示根目录；
  - `./`表示当前目录；（斜画线前面一个点）
  - `../`上级目录；（斜画线前面两个点）
  - 直接用文件名不带/也表示同一目录
  - 这些都是相对于当前文件的位置来说的，如果用绝对路径的话就是写全了。

####  三种列表的讲解

三种列表的知识讲解：

- `<ul>`无序列表

 	        无序列表是一个没有顺序项目的列表，此列表项默认粗体圆点进行标识

```xml
<ul>
   <li></li>
   <li></li>
   <li></li>
</ul>
```

- ` <ol>`有序列表

​       有序列表也是一列项目，只是列表项目使用的是数字进行标记。 有序列表始于 `<ol>` 标签。每个列表项始于 `<li>`标签

```xml
<ol>
   <li>内容一</li>
   <li>内容二</li>
   <li>内容三</li>
</ol>
```

- 列表符号
  - 无序列表-列表符号:
    - `type="circle"`  空心圆 `type=“disc”` 实心圆  默认值 `type="square"` 方块符
  - 有序列表-列表符号
    - `type="A"`    A B C D
    - `type="a"`    a b c d
    - `type="1"`    1 2 3 4  默认值type="I"    I II III type="i"    i ii iii
  - 列表嵌套
  - 无序列表-嵌套

```xml
<ul>
 <li>柚子
  <ul>
   <li>沙田柚</li>
   <li>蜜柚</li>
  </ul>
 </li>
 <li>荔枝</li>
 <li>苹果</li></ul>
```

有序列表-嵌套

```xml
<ol>
 <li>茶
  <ul>
   <li>红茶</li>
   <li>绿茶</li>
  </ul>
 </li>
 <li>果汁</li>
 <li>牛奶</li></ol>
```

定义列表

- 定义列表不仅仅是一列项目，而是项目及其注释的组合。定义列表以 `<dl>` 标签开始。每个定义列表项以 `<dt>`开始。每个自定义列表项的定义以 `<dd>` 开始。

```xml
<dl>  
     <dt>pc网页制作</dt>  
     <dd>学习DIV+CSS JS JQ 项目实战</dd>  
     <dt>手机网页制作</dt>  
     <dd>手机网页制作实战</dd>
</dl>
```

`dd`是对`dt`的解释

- `< dl>< /dl>`用来创建一个普通的列表,
- `< dt>< /dt>`用来创建列表中的上层项目，
- `< dd>< /dd>`用来创建列表中最下层项目，
- `< dt>< /dt>`和`< dd>< /dd>`都必须放在`< dl>< /dl>`标志对之间。

```xml
<dl>
    <dt>中国城市</dt>
    <dd>北京 </dd>
    <dd>上海 </dd>
    <dd>广州 </dd>
    <dt>美国城市</dt>
    <dd>华盛顿 </dd>
    <dd>芝加哥 </dd>
    <dd>纽约 </dd>
</dl>
```

- `dl`是d`efinition list`的缩写
- `dt`是`definition title`的缩写
- `dd`是d`efinition description`的缩写

- `list-style`属性具有三个属性分量：
- `list-style-position` ：设置列表项图标的位置，位于文本内或者文本外
- `list-style-type`： 设置列表项图标的类型
- `list-style-image`：使用图像设置列表项图标

####  表单元素(上)

- 表单标签:
  - `<form>`表单标签
    - `<form>`表单是一个包含表单元素的区域，包括起来的都是表单的内容

```xml
<form>
 <input type="text"/>
</form>
```

HTML标签 - `Action`和确认按钮：

- 当用户单击确认按钮时，表单的内容会被传送到另一个文件。表单的动作属性定义了目的文件的文件名。由动作属性定义的这个文件通常会对接收到的输入数据进行相关的处理。

```xml
<form action="html.do" method="get">    
        username:  <input type="text" name="user" />   
        <input type="submit" value="提  交" />
</form>
```

`HTML`标签 - 隐藏域隐藏标签：

​        隐藏域在页面中对于用户是不可见的，在表单中插入隐藏域的目的在于收集或发送信息，以利于被处理表单的程序所使用。浏览者单击发送按钮发送表单的时候，隐藏域的信息也被一起发送到服务器

```xml
<form>        
     <input type="hidden" name="hid" value="value">
</form>
```

`<input>`标签的掌握

- 常用`type`类型：
  - `<input type="" name="" value="" />`
  - `type="text"`       单行文本输入框
  - `type="password"` 密码（`maxlength=""`）
  - `type="radio"`     单项选择（`checked="checked"`）
  - `type="checkbox"`   多项选择
  - `type="button"` 按钮
  - `type="submit"`   提交 `type="image"`图片提交
  - `type="file"` 上传文件
  - `type="reset"`重置
  - `type="hidden"`   隐藏

关于表单中的设置默认值：

```csharp
<input type="text" name="" value="今天心情不错" />
<input type="radio" name="" value="" checked="checked">
<input type="checkbox" name="" value="" checked="checked
```

```xml
<select name="" >
 <option  value=""></option>
 <option  value="" selected="selected"></option>
<select>
```

`textarea`没有默认值

`<label>`标签的使用

- `<label></label>`
  - `label` 元素不会向用户呈现任何特殊效果。
  - 不过，它为鼠标用户改进了可用性。
  - 如果您在 `label` 元素内点击文本，就会触发此控件。
  - 就是说，当用户选择该标签时，浏览器就会自动将焦点转到和标签相关的表单控件上。
  
- `<label>` 标签的`for` 属性应当与相关元素的 `id`属性相同。

  ```xml
  <p>单向选择</p>
  <label for="male">男：</label><input type="radio" name="sex" id="male"/>
  <label for="nv">女：</label><input type="radio" name="sex"checked="check"/>
  ```

#### 表单和表格(下)

表单和表格标签：

- `<textarea>`文本域标签
- `<textarea>`标签：
- `<textarea></textarea>`是文本域标签，可以在其中插入一段文字内容，它有两个常用属性`rows`和`cols`

注意：

- `rows`表示这个文本域有多少行
- `cols`表示这个文本域有多少列

除了这两个属性它还有`readonly`（只读，文本域的内容无法改变，相当于协议）和`title`（鼠标放上提示）

`<select>`标签的掌握

- 注：当提交表单时，浏览器会提交选定的项目，或者收集用逗号分隔的多个选项，将其合成一个单独的参数列表，并且在将 `<select>` 表单数据提交给服务器时包括 `name`属性

```xml
<form>      
    <select name=""  id="">
         <option value="1">1月</option>  
          <option value="2">2月</option>      
</select>
</form>
```

- 常用到的属性：`disabled=“disabled” name="sel" size="2"`

- `<table>`表格标签
- `<table>`表格标签：`<table>`是表格标签，可以用它定义一个表格。

```xml
<table border="1">
    <tr>
    <td>姓名</td>
    <td>性别</td>
    </tr>
</table>
```

- 注意：`<table>`的`border`属性不能少

- `<tr>` `<td>`标签的使用
  - `<tr>`行标签：
    - `<tr>`可以定义表格中的一行，一个<`tr></tr>`表示一行。

```xml
<table border="1">
<tr>
 <td>姓名</td>
 <td>性别</td>
</tr>

<tr>
 <td>姓名</td>
 <td>性别</td>
</tr>
</table>
```

`<td>`单元格标签:

- `<td>`可以定义表格中的一个单元格，`<td></td>`表示一个单元格

```xml
<table border="1">
<tr>
<td >姓名</td>
<td>性别</td>
<td>爱好</td>
</tr>
</table>
```

- `order-collapse` 属性设置是否将表格边框折叠为单一边框：
- `border-collapse:collapse`;

- `colspan`左右合并
- `rowspan`上下合并

总结

- 非可视化标签：`head`  `meta`  `style`  `scrpit.`..

- 可视化标签：`img`  `div` `span` `a` `ul` `li`...

- 只有可视化标签，才能用`css`改变它

- 单标签：`meta`  `link`  `base`  `img`  `input` `br` `hr`

- 双标签：`html` `head` `body`  `div`  `a`  `p`  `span` ..`ul` `li` `ol` `dl` ....


**常用可视化标签**

- div

  - 一般用它来布局
  
- a

    超链接标签

  - `href`*属性：设置跳转的网页地址
  - `target`属性：设置跳转的目标
  - 结论：凡事页面可以点击跳转或者表单提交的文字，都用`a`标签

- `img`

  - `src`*属性用来设置图片的url数据
  - `alt`提供给搜索引擎搜索的
  - `width`
  - `height`
  - 结论 ：显示图片

- ul li

  - 列表
  - 结论：只要将来设计页面中有固定样式的列表，就用ul和li

- `table` `caption` `tr` `td (th)`

  - 慢慢已经被淘汰了 被ul li代替
  - 如果是合并竖排的就是合并行（`rowspan`）
  - 如果是合并横排的就是合并列（`colspan`）



### css基础知识

------

css基础知识：

- `css`样式表的定义
- `css`：（Cascading Style Sheets）层叠样式表；

分类及位置：内部样式-head区域style标签里面

- 外部样式-`link`调用
- 内联样式-标签元素里面

`css`内的注释：/`*`注释内容`*`/

css样式表的语法

- `CSS`规则由两个主要的部分构成：要添加样式的盒子名或者标签名、和要添加的样式。
- 盒子名或者标签名{属性:值;}
- **CSS中几种颜色的表示方法**

用颜色名表示
- 有17个预先确定的颜色，它们是

- `aqua`, `black`, `blue`, `fuchsia`, `gray`, `green`, `lime`, `maroon`, `navy`,
  `olive`, `orange,` `purple`, `red`, `silver`, `teal`, `white`, and `yellow`

**用十六进制的颜色值表示(红、绿、蓝)**

- `#FF0000`或者`#F00`

**用rgb(r,g,b)函数表示**

- 如：`rgb(255,255,0)`

**用hsl(Hue,Saturation,Lightness)函数表示（色调、饱和度、亮度)**
- 如：`hsl(120,100%,100%)`,色调0代表红色，`120`代表绿色，`240`代表蓝色

**用`rgba(r,g,b,a)`函数表示 **

- 其中`a`表示的是改颜色的透明度，取值范围是`0~1`，其中`0`代表完全透明

**用hsla(Hue,Saturation,Lightness,alpha)函数表示**

- 色调、饱和度、亮度、透明度

  ```html
  <div style="position:absolute;top:0px">
          <div style="background-color:gray;">background-color:gray</div>
          <div style="background-color:#F00;">background-color:#F00</div>
          <div style="background-color:#ffff00;">background-color:#ffff00</div>
          <div style="background-color:rgb(255,0,255);">background-color:rgb(255,0,255)</div>
          <div style="background-color:hsl(120,80%,50%);">background-color:hsl(120,80%,50%)</div>
          <div style="background-color:rgba(255,0,255,0.5);">background-color:rgba(255,0,255,0.5)</div>
          <div style="background-color:hsla(120,80%,50%,0.5);">background-color:hsla(120,80%,50%,0.5)</div>
      </div>
  ```

内部样式表

- 当单个页面需要设置样式时，就应该使用内部样式表。
- 使用 `<style></style>`标签在文档`<head></head>`里面定义内部样式表

```xml
<head>
 <style type="text/css" >
  p{color:red;}
 </style>
</head>
```

从外部引入到样式分为两种：（注意写在`head`标签里面）

当样式需要应用于很多页面时，就需要用到外部样式表，首先需要创建一个`css`文件，然后引用到我们的页面中。

`Link`样式表式：  `<link rel=”stylesheet” type=”text/css” href=”my.css”(href表示路径)>`

`Html`式：  `<style type="text/css">@import url("css.css");></style>`

内联样式表（优先级高）
- 写在标签里面的样式
- 如：`<p style="color:red;"></p>`

表示给`p`标签里面的文字颜色设置为红色

区别：外链样式与导入样式
- `link`标签是属于`xhtml`范畴，而`@import`则是`css2.1`中特有的。`link`标签除了可以加载`CSS`外，还可以做很多其它的事情，比如定义`RSS`，定义`rel`连接属性等，`@import`就只能加载`CSS`了。

- 加载的顺序的区别，`link`加载的`css`时，是一种并行(没有尝试是否是这样)加载`CSS`方式，而`@impor`则在整个页面加载完成后才加载。
- 兼容性的区别，因`@import``CSS2.1`才特有的，所以对于不兼容`CSS2.1`的浏览器来说，无效。
- 在样式控制上(比如动态改变网页的布局时,使用`javascript`操作`DOM`)的区别，此时`@import`就无能为力了。



**样式的优先级补充**

- 相同权值情况下，CSS样式的优先级总结来说，就是——就近原则（离被设置元素越近优先级别越高）：

  - `内联样式表（标签内部）` > `嵌入样式表（当前文件中）`> `外部样式表（外部文件中）`

- 权值不同时，浏览器是根据权值来判断使用哪种`css`样式的，哪种样式权值高就使用哪种样式


- 层叠优先级是:

- ```
  浏览器缺省`< `外部样式表` < `内部样式表` < `内联样式
  ```

- 其中样式表又有:`类选择器` < `类派生选择器`<`ID选择器` < `ID派生选择器`

- 派生选择器以前叫上下文选择器，所以完整的层叠优先级是:

- `浏览器缺省` <`外部样式表` < `外部样式表类选择器` < `外部样式表类派生选择器`< `外部样式表ID选择器` < `外部样式表ID派生选择器`< `内部样式表` < `内部样式表类选择器` < `内部样式表类派生选择器` < `内部样式表ID选择器` < `内部样式表ID派生选择器` < `内联样式`...共`12`个优先级

- 另外，如果同一个元素在没有其他样式的作用影响下，其`Class`定义了多个并以空格分开，其优先级顺序为：


- 一个元素同时应用多个`class`，后定义的优先（即近者优先），加上`!important`者最优先！

#### css选择器(上)

- `css`选择器：
- `class`类选择器可以重复利用
  - `id`选择器唯一
  
- 标签选择器

  - 什么是选择器：css选择器就是要改变样式的对象

- 选择器`{属性:值;属性:值;}`

- 标签选择器：页面中所有的标签都是一个选择器  `p{color:red;}`

- `ID`选择器

  - 选择`id`命名的元素 以 `#` 开头   `#p1{color:#0f0;}`

- 类选择器

  - `class`选择器，选择`clas`命名的元素 以`.`开头  `.first{color:#00f;}`

- `css`代码写完后上线前要经过压缩处理

- 本地和服务器分两个`css`版本（备份）

- 压缩后注释都清除，空间体积减少

- 群组选择器

  - 选择多个元素,以逗号隔开 `#main,.first,span,a,h1{color:red;}`

- 包含选择器

  - 选择某元素的后代元素，也称后代选择器，父类与子类间以空格隔开p

    - `span{color:red;}`
  
- 属性选择器

  - 选择包含某一属性的元素
  - `a[title]{color:red;}`  选择包含`title`的`a`标签
  - `a[title][href]{color:red;}` 选择包含`title`和`href`的`a`标签

- `>` `+` 选择器子类选择器：只选择子元素（只选择儿子）（相当于包含元素）

  - `p > span{color:red;}`

- 相邻兄弟选择器：只选择后面的相邻兄弟元素

  - `p + span{color:red;}`



#### css选择器(下)

------

- <a>伪类选择器

- `a:link {color:#FF0000;}`  /* 未访问的链接 */ （只用于a标签）
- `a:visited {color:#00FF00;}`   /* 已访问的链接 */ （只用于a标签）
- `a:hover {color:#FF00FF;}`/* 鼠标移动到链接上
- `*/`（可和其他标签结合一起用）
- `a:active {color:#0000FF;}`    /* 选定的链接 */

**注意**

- 伪类选择器的排序很重要，`a:link` `a:visited` `a:hover` `a:active`，记作`lvha`

- 输入伪类选择器（针对表单）
  - `input:focus{color:red;}`      /* 键盘输入焦点 */
- 其他伪类选择器
  - `p:first-child{color:red;}`     /`* 第一个p *`/
  - `:before` 在元素之前添加内容。
  - `:after` 在元素之后添加内容。
- `css`优先规则
  - 内联样式表-> `ID` 选择器—> `Class` 类选择器->标签选择器

####  背景属性

------

- 背景属性：
  - 背景的添加 ：
  - 背景颜色的添加:
    - `background:red;`
    - `backgronnd-color:red;`
  - 背景图片的添加：
    - `background:url(“images/1.jpg”);`
    - `backgronnd-image:url(“images/1.jpg”);`
  - 背景的平铺
  - 什么是平铺？平铺就是图片是否重复出现
    - 不平铺：`background-repeat:no-repeat;`
    - 水平方向平铺：`background-repeat:repeat-x;`
    - 垂直方向平铺：`background-repeat:repeat-y;`
    - 完全平铺：默认为完全平铺
  - 背景图片的定位
    - 背景图片的定位就是可以设置显示背景图片的位置，通过属性`background-position`来实现
    - `background-position`的取值可为英文单词或者数值和百分值。
    - `background-positon`的英文单词取值
    - `top left`
    - `top center`
    - `top right`
    - `center left`
    - `center center`
    - `center right`
    - `bottom left`
    - `bottom center`
    - `ottom right`
  - `background-positon`的数值取值
    - `background-position:x y;`
  - `positon`的百分值取值
    - `background-position:x% y%;`
  - 背景图片的大小
    - 背景图片的大小可以通过属性`background-size`来设置`background-size`的取值可为数值和百分值。
  - `background-size`的数值取值
    - `background-size:x y;`
  - `background-size`的数值取值
    - `background-size:x% y%;`
  - 背景图片的滚动
    - 背景图片是否随着内容的滚动而滚动由`background-attachment`设置
    - `background-attachment:fixed;`  固定，不随内容的滚动而滚动
    - `background-attachment:scroll;` 滚动，随内容的滚动而滚动

------

####  文字文本属性

------

`css`文字文本属性：
- **文字属性**
  - `color:red;`  文字颜色
  - `font-size:12px`; 文字大小
  - `font-weight:“bold”`  文字粗细(`bold/normal`)
  - `font-family:“宋体”`    文字字体
  - `font-variant:small-caps`小写字母以大写字母显示

**文本属性**

- `text-align:center;`   文本对齐(`right`/`left`/`center`)

- `line-height:10px;` 行间距(可通过它实现文本的垂直居中)

- `text-indent:20px;`  首行缩进

- text-decoration:none;

     文本线(`none`/`underline`/`overline`/`line-through`)

- `letter-spacing`:   字间距

------

####  盒子模型

------

**盒子模型**
- 盒子模型就是一个有高度和宽度的矩形区域
- 所有`html`标签都是盒子模型
- `div`标签自定义盒子模型

所有的标签都是盒子模型

- `class`和`id`的主要差别是：`class`用于元素组（类似的元素，或者可以理解为某一类元素），而`id`用于标识单独的唯一的元素。

**盒子模型的组成**

- 盒子模型组成部分：
  - 自身内容：`width`、h`eight` 宽高
  - 内边距：   `padding`
  - 盒子边框： `border` 边框线
  - 与其他盒子距离：  `margin`外边距
  - 内容+内边距+边框+外边距=面积

`border` 边框

- 常见写法  `border:1px solid #f00;`

单独属性：

`border-width`:

`border-style:`
- `dotted` 点状虚线
- `dashed`（虚线）
- `solid`（实线）
- `double`（双实线）

`border-color` (颜色)

`padding` 内边距
- 值：`像素`/`厘米`等长度单位、百分比
  - `padding:10px;`                      上下左右
  - `padding:10px 10px;`                 上下  左右
  - `padding:10px 10px 10px;`         上 左右 下
  - `padding:10px 10px 10px 10px;` 上 右 下 左（设置4个点-->顺时针方向）

单独属性：
- padding-top:上内边距

- padding-right:右内边距

- padding-bottom:下内边距

- padding-left:左内边距

当设置内边距的时候会把盒子撑大，为了保持盒子原来的大小，应该高度和宽度进行减小，根据`width`和`height`减小

margin 外边距
- 值：与`padding`相同
- 单独属性：与`padding`相同

外边距合并：两个盒子同时设置了外边距，会进行一个外边距合并

#### 外边距实现盒子居中

可以让一个盒子实现水平居中，需要满足一下两个条件：

1. 必须是块级元素。     
2. 盒子必须指定了宽度（width）

然后就给**左右的外边距都设置为auto**，就可使块级元素水平居中。

实际工作中常用这种方式进行网页布局，示例代码如下：

```css
.header{ width:960px; margin:0 auto;}
```



####  块元素、行元素与溢出

------

基本概念
- 块级元素：默认情况下独占一行的元素，可控制宽高、上下边距；
- 行内元素：默认情况下一行可以摆放多个的元素，不可控制宽高和上下边距

行块转换
- `display:none`;  不显示
- `display:block`; 变成块级元素
- `display:inline`; 变成行级元素
- `display:inline-block`; 以块级元素样式展示，以行级元素样式排列

溢出
- `overflow:hidden`;   溢出隐藏
- `overflow:scroll`;   内容会被修剪，浏览器会显示滚动条
- `overflow:auto`;   如果内容被修剪，则产生滚动条

文本不换行：`white-space:nowrap`;

长单词换行：`word-wrap:break-word`;

行内元素和快级元素小结

一、**块级元素**：block element
- 每个块级元素默认占一行高度，一行内添加一个块级元素后无法一般无法添加其他元素（`float`浮动后除外）。两个块级元素连续编辑时，会在页面自动换行显示。块级元素一般可嵌套块级元素或行内元素；
- 块级元素一般作为容器出现，用来组织结构，但并不全是如此。有些块级元素，如只能包含块级元素。
- `DIV` 是最常用的块级元素，元素样式的`display:block`都是块级元素。它们总是以一个块的形式表现出来，并且跟同级的兄弟块依次竖直排列，左右撑满。

二、**行内元素**：inline element

- 也叫内联元素、内嵌元素等；行内元素一般都是基于语义级(semantic)的基本元素，只能容纳文本或其他内联元素，常见内联元素 “a”。比如 `SPAN`元素，`IFRAME`元素和元素样式的`display : inline`的都是行内元素。例如文字这类元素，各个字母 之间横向排列，到最右端自动折行。

三、**block（块）元素的特点:**
- ①、总是在新行上开始；
- ②、高度，行高以及外边距和内边距都可控制；
- ③、宽度缺省是它的容器的100%，除非设定一个宽度。
- ④、它可以容纳内联元素和其他块元素

四、**inline元素的特点**
- ①、和其他元素都在一行上；
- ②、高，行高及外边距和内边距不可改变；
- ③、宽度就是它的文字或图片的宽度，不可改变
- ④、内联元素只能容纳文本或者其他内联元素

**对行内元素，需要注意如下**:
- 设置宽度`width` 无效。 设置高度`height`无效，可以通过`line-height`来设置。 设置`margin`
- 只有左右`margin`有效，上下无效。
- 设置`padding`只有左右`padding`有效，上下则无效。注意元素范围是增大了，但是对元素周围的内容是没影响的。

五、**常见的块状元素**
- `address` – 地址
- `blockquote` – 块引用
- `center` – 举中对齐块
- `dir` – 目录列表
- `div` – 常用块级容易，也是`CSS layout`的主要标签
- `dl` – 定义列表
- `fieldset` – `form`控制组
- `form` – 交互表单
- `h1` – 大标题
- `h2` – 副标题
- `h3` – 3级标题
- `h4` – 4级标题
- `h5` – 5级标题
- `h6` – 6级标题
- `hr` – 水平分隔线
- `isindex` – `input prompt`
- `menu` – 菜单列表
- `noframes` – `frames`可选内容，（对于不支持frame的浏览器显示此区块内容
- `noscript` – 可选脚本内容（对于不支持`script`的浏览器显示此内容）
- `ol` – 有序表单
- `p` – 段落
- `pre` – 格式化文本
- `table` – 表格
- `ul` – 无序列表

六、**常见的内联元素**
- `a` – 锚点
- `abbr` – 缩写
- `acronym` – 首字
- `b` – 粗体(不推荐)
- `bdo` – `bidi override`
- `big` – 大字体
- `br` – 换行
- `cite` – 引用
- `code` – 计算机代码(在引用源码的时候需要)
- `dfn` – 定义字段
- `em` – 强调
- `font` – 字体设定(不推荐)
- `i` – 斜体
- `img` – 图片
- `input` – 输入框
- `kbd` – 定义键盘文本
- `label` – 表格标签
- `q` – 短引用
- `s` – 中划线(不推荐)
- `samp` – 定义范例计算机代码
- `select` – 项目选择
- `small` – 小字体文本
- `span` – 常用内联容器，定义文本内区块
- `strike` – 中划线
- `strong` – 粗体强调
- `sub` – 下标
- `sup` – 上标
- `textarea` – 多行文本输入框
- `tt` – 电传文本
- `u` – 下划线

七，**可变元素**
- 可变元素为根据上下文语境决定该元素为块元素或者内联元素。
- `applet` - `java applet`
- `button` - 按钮
- `del`- 删除文本
- `iframe` - `inline frame`
- `ins` - 插入的文本
- `map` - 图片区块(`map`)
- `object` - `object`对象
- `script` - 客户端脚本

八、**行内元素与块级元素有什么不同**
- 区别一：
  - 块级：块级元素会独占一行，默认情况下宽度自动填满其父元素宽度
  - 行内：行内元素不会独占一行，相邻的行内元素会排在同一行。其宽度随内容的变化而变化。
- 区别二：
  - 块级：块级元素可以设置宽高
  - 行内：行内元素不可以设置宽高
- 区别三：
  - 块级：块级元素可以设置`margin`，`padding`
  - 行内：行内元素水平方向的`margin-left;` `margin-right;`
- `padding-left;` `padding-right`;可以生效。但是竖直方向的`margin-bottom`; `margin-top`; `padding-top`; `padding-bottom`;却不能生效。
- 区别四：
- 块级：`display:block`;
- 行内：`display:inline`;

替换元素有如下：（和`img`一样的设置方法）

<img>、<input>、<textarea>、<select>

`<object>`都是替换元素，这些元素都没有实际的内容

可以通过修改`display`属性来切换块级元素和行内元素

------

####  定位

------

- `static`静态定位（不对它的位置进行改变，在哪里就在那里）
  - 默认值。没有定位，元素出现在正常的流中（忽略 `top`,`bottom,`  `left, right` 或者 `z-index` 声明）。
- `fixed`固定定位（参照物--浏览器窗口）---做 弹窗广告用到
  - 生成固定定位的元素，相对于浏览器窗口进行定位。 元素的位置通过 `"left"`, `"top"`, `"right"`以及 `"bottom"`属性进行规定。
- `relative`（相对定位 ）（参照物以他本身）
  - 生成相对定位的元素，相对于其正常位置进行定位。
- `absolute`（绝对定位）(除了`static`都可以，找到参照物-->与它最近的已经有定位的父元素进行定位)
- 生成绝对定位的元素，相对于 `static` 定位以外的第一个父元素进行定位。
- 元素的位置通过 "`left"`, `"top"`, `"right"` 以及 `"bottom"` 属性进行规定
- z-index
  - `z-index` 属性设置元素的堆叠顺序。拥有更高堆叠顺序的元素总是会处于堆叠顺序较低的元素的前面。
  - 定位的基本思想: 它允许你定义元素框相对于其正常位置应该出现的位置，或者相对于父元素、另一个元素甚至浏览器窗口本身的位置。
- 一切皆为框
  - 块级元素: `div`、`h1`或`p`元素 即：显示为一块内容称之为 “块框“ ;
  - 行内元素: `span`,`strong`,`a`等元素 即：内容显示在行中称 "行内框";
  - 使用display属性改变成框的类型 即：`display:block`; 让行内元素设置为块级元素，`display:none;` 没有框
- 相对定位：
  - 如果对一个元素进行相对定位，它将出现在它所在的位置上。
  - 通过设置垂直或水平位置，让这个元素“相对于”它的起点进行移动
  - `.adv_relative { position: relative; left: 30px; top: 20px; }`
- 绝对定位：
  - 元素的位置相对于最近的已定位祖先元素，如果元素没有已定位 的祖先元素，它的位置相对于最初的包含块。 `.adv_absolute { position: absolute; left: 30px; top: 20px; }`

| 定位模式         | 是否脱标占有位置     | 是否可以使用边偏移 | 移动位置基准                     |
| ---------------- | -------------------- | ------------------ | -------------------------------- |
| 静态static       | 不脱标，正常模式     | 不可以             | 正常模式                         |
| 相对定位relative | 不脱标，占有位置     | 可以               | 相对自身位置移动（自恋型）       |
| 绝对定位absolute | 完全脱标，不占有位置 | 可以               | 相对于定位父级移动位置（拼爹型） |
| 固定定位fixed    | 完全脱标，不占有位置 | 可以               | 相对于浏览器移动位置（认死理型） |

####  框架

------

- `frameset`框架：
- `<frameset>` ----  用来定义一个框架；双标签
     不能和  `<body>`  一起使用
  
- `rows`、`cols`属性

  - `rows` 定义行表示框架有多少行（取值 `px`/`%`/ `*` ）
  - `cols`   定义列表示框架有多少列（取值`px`/ `%`/ `*` ）

- frame子框架

  - <frame> ----  表示框架中的某一个部分；单标签，要跟结束标志
- `src` 显示的网页的路径
    - `name` 框架名
    - `frameborder`  边框线（取值 0 / 1）
  
- <`noframes`>属性

- <`noframes`> 提供不支持框架的浏览器显示`body`的内容；双标签

```xml
<frameset>
     <frame  src=“”  />
     <frame  src=“” />
     <frame  src=“” />
     <noframes>
      <body>内容</body>
     </noframes>
</frameset>
```

<`frames`>内联框架

- iframe元素会创建包含另外一个文档的内联框架（即行内框架）
  允许和 body 一起使用
- width 宽（取值 px / %）

- height 高（取值 px / %）

- name 框架名

- frameborder 边框线（取值 0 / 1）

- src 显示的网页的路径




####  css高级属性

------

- `opacity`透明属性

- ```
  opacity
  ```

  - 对于`IE6/7/`，使用`filter:alpha(opacity:值;`)  值为`0-100`
  - 对于`Webkit`，`Opera`，`Firefox`，`IE9+`，使用`opacity`:值; 值为`0-1`
  - 对于早期火狐，使用`-moz-opacity`:值; 值为`0-1`
  - 所以写透明属性时，一般写法



```rust
 {  
    opacity:0.5;
   filter:alpha(opacity：50);/*0-100*/
   -moz-opacity:0.5;    /*取值0-1*/-->针对早起版本的火狐兼容问题的解决
}
```

`border-radius`圆角边框属性

- 向 div元素添加圆角边框
  - `border-radius:10px`;

`box-shadow`阴影属性

- `box-shadow`属性向框添加阴影效果,后面跟4个参数。
- `box-shadow:0px 0px 10px #000;`

`<embed>`属性

- 是`HTML5`中新增的标签,媒体嵌入插件标签，可以通过`<embed>`插入音频或视频
- `<embed src=“media/music.mp3” />`
- 格式`.mid` `.wav` `.mp3`等



#### 文本溢出的几种处理方法

简单隐藏

```css
overflow： hidden
```

使用滚动条

```css
overflow： scroll
```

简单裁切

```css
    border:1px solid;
    overflow:hidden;/*超出隐藏*/
    white-space:nowrap;/*强制在一行显示*/
    text-overflow:clip;/*裁切*/
```

超出部分省略号

```css
   overflow:hidden;
    white-space:nowrap;
    text-overflow:ellipsis;/*使用省略号*/
```

#### 清除浮动的几种方法

`clearfix`只应用在包含浮动子元素的父级元素上

```css
.clearfix{zoom:1;}
.clearfix:after{
     display:block; 
     content:'clear'; 
     clear:both;
     line-height:0; 
     visibility:hidden;
}
```

在方法三的基础上的最优雅的做法

```css
.clearfix:after,
.clearfix:before {/*before 是为了防止浏览器顶部空白的崩溃*/   
     content: " ";   
     display: table;
}
.clearfix:after {    
    clear: both;
}
```

清除浮动的原理是触发`BFC`，这里只有`clear:both`起清除浮动作用，其他的`line-height:0; visibility:hidden;`都是为了隐藏生的内容需要的

额外标签法

```css
是通过在浮动元素末尾添加一个空的标签例如 <div style="clear:both"></div>，或则其他标签br等亦可
```

图片、表单和文字对齐

通过vertical-align 控制图片和文字的垂直关系了。 默认的图片会和文字基线对齐。

去除图片底侧空白缝隙

方法一：给img vertical-align:middle | top等等。  让图片不要和基线对齐

方法二：给img 添加 display：block; 转换为块级元素就不会存在问题了。

# HTML5 和 CSS 3

常用新标签

- header：定义文档的页眉 头部
- nav：定义导航链接的部分
- footer：定义文档或节的页脚 底部
- article：定义文章。
- section：定义文档中的节（section、区段）
- aside：定义其所处内容之外的内容 侧边

##### HTML5智能表单

------

input表单type

属性值：

- `type = "email"` 限制用户输入必须为`Email`类型
- `type="url"`        限制用户输入必须为`URL`类型
- `type="date"`     限制用户输入必须为日期类型
- `type="datetime"` 显示完整日期 含时区
- `type="datetime-local"` 显示完整日期 不含时区
- `type="time"`    限制用户输入必须为时间类型
- `type="month"`  限制用户输入必须为月类型
- `type="week"`    限制用户输入必须为周类型
- `type="number"` 限制用户输入必须为数字类型
- `type="range"`    生成一个滑动条
- `type="search"`  具有搜索意义的表单`results="n"`属性
- `type="color"`    生成一个颜色选择表单
- `type="tel"`    显示电话号码

##### HTML5新增表单属性

------

- `required:` `required`内容不能为空
- `placeholder:` 表单提示信息
- `autofocus:`自动聚焦
- `pattern:` 正则表达式  输入的内容必须匹配到指定正则范围
- autocomplete:是否保存用户输入值
  - 默认为`on`，关闭提示选择`off`
- `formaction:` 在`submit`里定义提交地址
- `datalist:` 输入框选择列表配合`list`使用 `list`值为`datalist`的`id`值
- `output:` 计算或脚本输出



##### CSS3 新增选择器

- :first-child :选取属于其父元素的首个子元素的指定选择器
- :last-child :选取属于其父元素的最后一个子元素的指定选择器
- :nth-child(n) ： 匹配属于其父元素的第 N 个子元素，不论元素的类型
- :nth-last-child(n) ：选择器匹配属于其元素的第 N 个子元素的每个元素，不论元素的类型，从最后一个子元素开始计数。
  n 可以是数字、关键词或公式

```css
li:first-child { /*  选择第一个孩子 */
        		color: pink; 
        	}
li:last-child {   /* 最后一个孩子 */
        		color: purple;
        	}
li:nth-child(4) {   /* 选择第4个孩子  n  代表 第几个的意思 */ 
				color: skyblue;
        	}
```

E::before和E::after

在E元素内部的开始位置和结束位创建一个元素，该元素为行内元素，且必须要结合content属性使用。

```css
div::befor {
  content:"开始";
}
div::after {
  content:"结束";
}
```



E:after、E:before 在旧版本里是伪元素，CSS3的规范里“:”用来表示伪类，“::”用来表示伪元素，但是在高版本浏览器下E:after、E:before会被自动识别为E::after、E::before，这样做的目的是用来做兼容处理。

":" 与 "::" 区别在于区分伪类和伪元素

之所以被称为伪元素，是因为他们不是真正的页面元素，html没有对应的元素，但是其所有用法和表现行为与真正的页面元素一样，可以对其使用诸如页面元素一样的css样式，表面上看上去貌似是页面的某些元素来展现，实际上是css样式展现的行为，因此被称为伪元素。是伪元素在html代码机构中的展现，可以看出无法伪元素的结构无法审查



**注意**

伪元素:before和:after添加的内容默认是inline元素**；这个两个伪元素的`content`属性，表示伪元素的内容,设置:before和:after时必须设置其`content`属性，否则伪元素就不起作用。



##### CSS3新增文本属性

- `color:rgba()`;
- `text-overflow`:是否使用一个省略标记（...）标示对象内文本的溢出
- `text-align`:文本的对齐方式
- `text-transform`:文字的大小写
- `text-decoration`:文本的装饰线，复合属性
- `text-shadow`:文本阴影
- `text-fill-color`:文字填充颜色
- `text-stroke`:复合属性。设置文字的描边
- `tab-size`:制表符的长度
- `word-wrap`:当前行超过指定容器的边界时是否断开转行
- `word-break`:规定自动换行的处理方法

- **`text-overflow:`是否使用一个省略标记（`...`）标示对象内文本的溢出**

  - `clip`： 默认值 无省略号
  - `ellipsis`：当对象内文本溢出时显示省略标记（`...`）。
  - **注意**：该属性需配合`over-flow:hidden`属性(超出处理)还有 `white-space:nowrap`(禁止换行)配合使用，否则无法看到效果

- **`text-align`:文本的对齐方式**

  - `css1`
  - `left`:默认值 左对齐
  - `right`:右对齐
  - `center`:居中
  - `justify`： 内容两端对齐。
  - `css3`
  - `start`:开始边界对齐
  - `end`:结束边界对齐

- **`text-transform`**:文字的大小写

  - `css1`

    - `none`：	默认值 无转换
    - `capitalize`： 	将每个单词的第一个字母转换成大写
    - `uppercase`：	转换成大写
    - `lowercase`：	转换成小写

  - `css3`

    - `full-width`：	将左右字符设为全角形式。不支持

    - ```
      full-size-kana
      ```

      ：将所有小假名字符转换为普通假名。不支持

      - 例如：土耳其语

- **`text-decoration`:文本的装饰线，复合属性(只火狐支持)**

  - text-decoration-line 
    - 指定文本装饰的种类。相当于`CSS1`时的`text-decoration`属性
  - text-decoration-style
    - `指定文本装饰的样式。
  - text-decoration-color
    - `指定文本装饰的颜色。
  - `blink`： 指定文字的装饰是闪烁。  `opera`和`firefox`
  - `text-decoration` : `#F00 double overline`   `CSS3`实例

- **`text-shadow`:文本阴影**

  - 取值：x  y blur   color

    ,......

    - `x  `  	横向偏移
    - `y `   	纵向偏移
    - `blur `     模糊距离(灰度)
    - `color`    阴影颜色

- `text-fill-color`:文字填充颜色

- `text-stroke`:复合属性。设置文字的描边

  - `text-stroke-width`:文字的描边厚度
  - `text-stroke-color`:文字的描边颜色

- `tab-size`:制表符的长度

  - 默认值为`8`(一个`tab`键的空格字节长度)，在	`pre`标签之内才会有显示

- `word-wrap`:当前行超过指定容器的边界时是否断开转行

  - `normal`： 默认值
  - 允许内容顶开或溢出指定的容器边界。

- `break-word`：

  - 内容将在边界内换行。如果需要，单词内部允许断行

CSS3盒模型

CSS3中可以通过box-sizing 来指定盒模型，即可指定为content-box、border-box

1、box-sizing: content-box  盒子大小为 width + padding + border   content-box:此值为其默认值，其让元素维持W3C的标准Box Mode

2、box-sizing: border-box  盒子大小为 width    就是说  padding 和 border 是包含到width里面的

##### 动画

- **动画接口**

| 属性                      | 描述                                                     |
| ------------------------- | -------------------------------------------------------- |
| @keyframes                | 规定动画。                                               |
| animation                 | 所有动画属性的简写属性，除了 animation-play-state 属性。 |
| animation-name            | 规定 @keyframes 动画的名称。                             |
| animation-duration        | 规定动画完成一个周期所花费的秒或毫秒。                   |
| animation-timing-function | 规定动画的速度曲线。                                     |
| animation-delay           | 规定动画何时开始。                                       |
| animation-iteration-count | 规定动画被播放的次数。                                   |
| animation-direction       | 规定动画是否在下一周期逆向地播放。                       |
| animation-play-state      | 规定动画是否正在运行或暂停。                             |
| animation-fill-mode       | 规定对象动画时间之外的状态。                             |

- **animation-timing-function速度曲线**

| 值                    | 描述                                                         |
| --------------------- | ------------------------------------------------------------ |
| linear                | 动画从头到尾的速度是相同的。                                 |
| ease                  | 默认。动画以低速开始，然后加快，在结束前变慢。               |
| ease-in               | 动画以低速开始。                                             |
| ease-out              | 动画以低速结束。                                             |
| ease-in-out           | 动画以低速开始和结束。                                       |
| cubic-bezier(n,n,n,n) | 在 cubic-bezier 函数中自己的值。可能的值是从 0 到 1 的数值。 |

- 在谷歌浏览器里面需要加上`-webkit-` `IE6,7,8,9`不支持`css3`运动

##### 文字阴影(CSS3)

text-shadow:水平位置 垂直位置 模糊距离 阴影颜色;

z-index只有定位才会产生

定位一定要有宽度