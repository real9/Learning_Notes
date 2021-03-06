# 1.HTML的概述
  HTML 描述了一个网站的结构，是一种标记语言而非编程语言。一个HTML元素是HTML文件的基本组成单元。  
  浏览器使用 HTML 标签（即`<html>`）和脚本（JavaScript）来诠释网页内容，但不会将标签显示在页面上。
# 2.认识HTML
## 2.1HTML元素的结构
### 2.1.1HTML标签
HTML标签有以下特点：
* 1.由尖括号包围关键词组成，如`<p>` `<h>` `<span>` 。  
* 2.通常成对出现，如`<div>` `</div>`。
* 3.也有单独出现的标签，如`<img>` `<input>`。  
>注：在HTML中，标签大小写不敏感，但是要求成对的标签大小写统一。  
### 2.1.2HTML元素的结构
`<p> Hello, World! </p> `  
开始标签+内容+结束标签。  
## 2.2HTML中的嵌套
`<div> <p> Hello, World! </p> </div>`  
div元素是p元素的父元素，p元素是div的子元素。  
## 2.3完整的HTML文档结构
```html
<!DOCTYPE HTML>
<html lang = "en">
  <head>
    <!--系统内置 start-->
<script type="text/javascript" src="//qgt-style.oss-cn-hangzhou.aliyuncs.com/commonJSCSS/console.js"></script>
<!--系统内置 end-->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>标题</title>
  </head>
  <body>
    <h1>两只口袋</h1>
    <p>普罗米修斯创造了人，又在他们每人脖子上挂了两只口袋，一只装别人的缺点，另一只装自我的。他把那只装别人缺点的口袋挂在胸前，另一只则挂在背后。因此人们总是能够很快地看见别人的缺点，而自我的却总看不见。<strong>这故事说明人们往往喜欢挑剔别人的缺点，却无视自身的缺点。</strong></p>
  </body>
</html>
```
[点击查看网页效果](https://ham.youkeda.com/workspaces/5dc566fb0f101ed7c2333ead/5eabd9eeda3d645484759f95/index.html?time=1611840572465)
#### 1.`<!DOCTYPE HTML>`
(1). 作用：告知浏览器该页面文件的文档类型，指示 web 浏览器使用哪个 HTML 版本编写页面。  
(2). 位置：<!DOCTYPE> 声明必须是 HTML 文档的第一行，位于 <html> 标签之前。  
(3). <!DOCTYPE> 声明对大小写不敏感。  
(4). <!DOCTYPE> 声明 **没有** 结束标签。
#### 2.`<html lang = "en">` 
(1). 此元素可告知浏览器其自身是一个 HTML 文档。  
(2). `<html> `与 `</html> `标签限定了文档的开始点和结束点，在它们之间是文档的头部和主体。文档的头部由` <head>` 标签定义，而主体由` <body> `标签定义。  
(3). lang 属性（语言属性）：当搜索引擎或者浏览器拿到语言属性后，有可能做一些针对指定语言的辅助操作，‘en’表示英文。  
#### 3.标签属性
(1). 标签可以拥有零个或多个标签属性，注意：标签属性与标签名称、标签属性与标签属性之间需用一个空格隔开。  
  (2). 标签属性可以赋予标签更多的信息，标签属性通常是以 key="value" 即 名称="值" 的形式出现。   
  (3). 常见的标签属性有：class、id、style、lang、src 等。
#### 4.文档的头部`<head>...</head>`
  (1). head 元素定义文档的头部，我们通常在这里引用样式表、提供元信息等。  
  (2). 文档的头部中的`<title>...</title>`定义文档的标题，在网页上体现为网页标签的标题。
  (3). 一个` <head> `元素必须包含且只能包含一个 `<title> `元素。（title元素之间必须有标题）  
#### 5.文档的主体`<body>...</body>`
  body 元素定义文档的主体，包含文档的所有内容（比如文本、超链接、图像、表格和列表等等）。
## 2.4HTML中的注释
  在HTML中我们用`<!-- ... -->`标签来表示注释。
## 2.5MDN
  [MDN](https://developer.mozilla.org/zh-CN/docs/Web/HTML)是学习 Web 开发的一个权威、全面、高质量的网站，文档丰富，资料全面，非常适合大家学习使用，是Web 开发学习时的百科全书。   
  在 MDN 中查询'audio'，为网页添加一段音频文件。 [audio 标签文档的地址`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/audio)
  ```html
  <body>
    <audio muted controls="controls">
      <source src="https://document.youkeda.com/P3-1-HTML-CSS/1.2/nocturne.mp3" autoplay>
      Your browser does not support the <code>audio</code> element.
    </audio>
  </body>
  ```
  [效果预览](https://ham.youkeda.com/workspaces/5dc566fb0f101ed7c2333ead/5eb2a2a529fdc7737671a7b1/index.html?time=1611843293648)     
在 MDN 中查询'progress'，在网页中插入一个进度条。 [progress 标签文档的地址](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/progress)  
  ```html
  <body>
   <progress value="50" max="100">
     50%
   </progress> 
   <p>
     <img src="https://y.gtimg.cn/music/photo_new/T002R300x300M000002mWhlf2aBPQ7_1.jpg?max_age=2592000" \>
   </p>
  </body>
  ```
  [效果预览](https://ham.youkeda.com/workspaces/5dc566fb0f101ed7c2333ead/5eb2a2a529fdc7737671a7b1/index.html?time=1611843494911)  
 # 3.HTML 文本标签
  ## 3.1块状和内联标签  
  块状标签和内联标签是 HTML 中两种主要的标签类型，它们**最大的区别**就是：块状标签会为自己的内容占据新的一行，而内联标签则不会。  
  常见块状标签：`<p>` `<h>` `<div>`  
  常见内联标签：`<img>` `<span>` `<strong>`  
  **内联标签常常被嵌套在块状标签中。**
  ## 3.2标题标签
  标题分为6个等级，从`<h1>`到`<h6>`，标题逐级减小。  
  > 注意：标题之间不可越级，比如一级标题`<h1>`下直接写三级标题`<h3>`，因为这样会导致文章失去清晰的文章结构。  
  ## 3.3常用文本标签
  标签类型|用法|作用
  --|---|--
  段落标签|`<p>...</p>`|表示一个段落  
  内联标签|`<span>...</span>`|不会产生换行，使网页有条理  
  内联标签|`<strong>...</strong>`|加粗文本
  ## 3.4图片标签
  例如：`<img src="https://document.youkeda.com/P3-1-HTML-CSS/1.3/x-1-3-1.gif" alt="">`
  在标签属性`src`中写入图片的**相对路径**或**绝对路径** 
  `alt`属性定义了描述图像的替换文本。若*图片不在支持的列表中*或者*图片未被下载*，则会替换成相应的文本。 
  ## 3.5链接标签
  `<a>`标签是内联标签，用户点击后，浏览器会跳转到指定的网址。  
  `<a>`标签内部不仅可以放置文字，也可以放置其他元素，比如段落、图像、多媒体等等。  
  如：`<a href="https://www.youkeda.com/post/detail/778d9f1b590f4b9a8e0f67fac4a2a438"> 原文链接 </a>`  
  链接标签的属性|说明
  --|--
  href|属性给出链接指向的网址。它的值应该是一个 URL 或者锚点
  title|给出链接的说明信息。鼠标悬停在链接上方时，浏览器会将这个属性的值，以提示块的形式显示出来。
  target|指定如何展示打开的链接。
  > target 属性的值也可以是“_self”、“_blank”、“_parent”、“_top”四个关键字之一。
  > 当它为_self 时表示在当前页面打开，target 默认为“_self”。
  > 当它为_blank 时表示在新页面打开。
  ```html
  _self: <a href="https://www.youkeda.com/" target="_self">优课达</a>
  _blank: <a href="https://www.youkeda.com/" target="_blank">优课达</a>
  ```
  ## 3.6列表
  标签| 含义
  --|--
  `<ol>...</ol>`| 有序列表，每一项均带有数字编号。
  `<ul>...</ul>`| 无序列表，每一项之前是一个黑点。  
  列表中的每一项都使用`<li>...</li>`。  
  # 4.HTML表单标签
  ## 4.1form标签
  属于同一个表单的表单控件要包含在同一个块状元素`<form>`里。  
  标签的属性|内容
  --|--
  `action`|一个处理此表单信息的程序所在的 URL，所述表格信息将在表单提交时被发送到定义的地址
  `method`|它的值可以是GET或POST，用来规定如何发送表单信息
  `<form>...</form>`不能嵌套使用。
  ## 4.2单行文本输入框
  ```html
  <!-- action=""则表单信息将提交到当前页面 -->
<form action="">
  <input type="text" />
</form>
  ```
 `input`不但是一个内联元素，还是一个只有开始标签，没有结束标签的内联元素，我们可以认为它是一个“自闭”元素。
  `input`标签属性|含义
  --|--
  占位文本 “placeholder”|用来提示用户需要输入什么，输入框中输入内容后，提示消失
  输入框名字 “name”|给输入框命名，区别于其他输入框
  输入框的值 “value”|希望在输入框中预填写用户的昵称
  不可修改的输入框 “readonly”和“disabled”|输入框变成只读输入框！这样用户就不能自己修改预填写的内容
  > 注意readonly和disabled的区别
  示例：`<input type="text" placeholder="昵称" name="nick" value="小明" disabled />`  
  ## 4.3多行文本输入框和密码输入框
  #### 4.3.1多行文本输入框
  当多行文本输入框中输入的内容超过一行的长度时，它会自动换行，而单行文本输入框则不会换行。
  ```html
  <!-- name属性表示表单元素的名称，placeholder属性表示表单元素的占位文本 -->
<textarea
  name="sign"
  rows="5"
  cols="30"
  placeholder="请输入个性签名"
></textarea>
  ```
> rows：行数（高度）； 
> cols：文本域的可视宽度；
  #### 4.3.2密码输入框
  密码输入框和昵称输入框有点区别，用户输入的内容将会以 黑圆点 的形式显示。
  ```html
  <!-- type属性表示表单元素的类型，name属性表示表单元素的名称，placeholder属性表示表单元素的占位文本 -->
<input type="password" name="password" placeholder="密码" />
  ```
  > 改变type类型，变原来的text为password。
  ## 4.4单选框和复选框
  #### 4.4.1单选框（以性别为例）
  示例：
  ```html
  <label> <input type="radio" name="gender" value="male" />男 </label>
<label> <input type="radio" name="gender" value="female" />女 </label>
  ```
  标签属性|含义
  --|--
  type|改变表单属性为radio
  name|属于同一道单选题的单选按钮应该有相同的名字
  value|表示值
  男/女|加入在`<input>`标签后面，表示选项内容
  `<lable>`|使得点击文字内容也能选中选项
  另一种写法：  
  ```html
  <input id="male" type="radio" name="gender" value="male" />
<label for="male">男</label>
<input id="female" type="radio" name="gender" value="female" />
<label for="female">女</label>
  ```
  #### 4.4.2复选框（以兴趣为例）
  示例：
  ```html
  <label> <input type="checkbox" name="interest" value="coding" />编程 </label>
<label> <input type="checkbox" name="interest" value="other" />其他 </label>
  ```
  type值改变，同一道多选题的name值应该相同。
  ## 4.5选项菜单（以职业选择为例）
  示例：
  ```html
  <select name="career">
  <option value="default">请选择职业</option>
  <option value="staff">公司职员</option>
  <option value="freelancer">自由职业者</option>
  <option value="student">学生</option>
  <option value="other">其他</option>
</select>
  ```
  > 这是一个单选菜单，如果用户选择了“学生”，那么提交的数据将会是：`career:“student”`  
  
  提交的内容是每个`<option>`标签内的value的值，所以每个值需要不相同。  
  多选菜单则需要将`<select>`标签中添加multiple属性：`<select name = "career" multiple>`(需按住ctrl并单击)。  
  ## 4.6按钮
  `<button>注册</button>`   
  > 标签内可以添加图片、文字等内容。  
  
  `<button type = "submit">注册</button>`  
  > 考虑到浏览器的兼容性问题，添加submit来确保数据的提交。  
  ## 4.7input标签小结
  类型|作用
  --|--
  text|单行输入框
  number|输入浮点数的控件
  password|值被遮盖的单行文本字段，使用maxlength可以控制最大长度
  checkbox|复选框，必须使用value定义提交的数据的值。
  radio|单选按钮，必须使用value定义单选题提交时的数据的值
  
  示例：
  ```html
<!DOCTYPE html>
<html lang="en">
  <head>
<!--系统内置 start-->
<script type="text/javascript" src="//qgt-style.oss-cn-hangzhou.aliyuncs.com/commonJSCSS/console.js"></script>
<!--系统内置 end-->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>编程题</title>
    <link rel="stylesheet" href="./index.css">
  </head>
  <body>
    <form action="https://www.youkeda.com/">
    <input type="text" name="name" placeholder="姓名" >
    <input type="number" name="mobile" placeholder="手机号" />
    <input type="password" name="password" placeholder="密码不少于6位" />
    <input type="checkbox" name="agree" value="agree" id="agreement"/>
    <label for="agreement">已阅读并同意使用条款以及非活跃号处理规范</label>
    <button type="submit">立即注册</button>
    </form>
  </body>
</html>

```


  
  
  
  
  
  
  
  
  
  
  
  
  
