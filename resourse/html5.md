## HTML5

初识HTML
网页基本标签
图像,超链接，网页布局
列表,表格,媒体元素
表单及表单应用
表单初级验证



### 初识HTML

> 概述

- HTML 
  - Hyper Text Markup Language (超文本标记语言) 

HTML 5,提供了一些新的元素和一些有趣的新特性，同时也建立了一些新的规则。这些元素、特性和规则的建立，提供了许多新的网页功能，如使用网页实现动态渲染图形、图表、图像和动画，以及不需要安装任何插件直接使用网页播放视频等。 

- W3C 
  - World Wide Web Consortium(万维网联盟)
  - www.w3.org
  - www.china3c.org
- w3c包括
  - 结构化标准语言（HTML、XML）
  - 表现标准语言（CSS）
  - 行为标准（DOM、ECMAScript）



### 网页基本标签

用idea开发

浏览器路径可以通过 setting ->Tools-->web browsers设置

成对的标签 <body></body> 叫做开放标签和闭合标签，单独呈现的标签</br> 自闭合标签

注释：<!-- --->

- 标题标签
- 段落标签
- 换行标签
- 水平线标签
- 字体样式标签
- 注释和特殊符号



```html
<h1>一级标签</h1>
<p>aaa</p>
<hr/>
<br/>
<strong></strong>
<em></em>
&nbsp;
&gt;
&lt;
&copy;版权符号

```



### 图像,超链接，网页布局



> 图像

```html
<img src="../resourse/image/1.gif" alt="头像" title="悬停文字" width="100" height="100">
src : 图片地址（必填）
    相对地址，绝对路径
    ../     --上一级目录
alt : 图片名字（必填）图片未找到显示的文字
title ： 图标悬停文字
```

> 链接标签

```html
<!--    a标签
href : 必填，表示要跳转到哪个页面
target : 表示窗口在哪里打开
    _blank:在新标签页面打开
    _self :在自己的网页种打开（默认）
-->
<a href="https://www.baidu.com" target="_self"> 点我跳转到百度</a>

<!--锚链接
1.需要一个锚标记
2.跳转到标记
# 
-->

<a href="#top">回到顶部</a>

<!--功能性链接
    邮件链接 ： mailto :
-->
<a href="mailto:ximpermanence@qq.com">点击联系我</a>

```



#### 网页布局

> 行内元素和块元素

- 块元素
  - 无论内容多少，该元素独占一行
  - (p、h1-h6...)
- 行内元素
  - 内容撑开宽度，p 左右都是行内元素的可以排在一行
  - (a.strong.em)

> 列表

- 什么是列表
  - 列表就是信息资源的一种展示形式。它可以使信息结构化和条理化，并以列表的样式显示出来，以便浏览者能更快捷地获得相应的信息
- 列表的分类
  - 无序列表
  - 有序列表
  - 定义列表

```html
<ol>
    <li>java</li>
</ol>

<ul>
    <li>java</li>
</ul>

<dl>
    <dt>学科号</dt>
    <dd>java</dd>
    
    <dt>位置</dt>
    <dd>北京</dd>
</dl>
```



> 表格

- 为什么使用表格
  - 简单通用
  - 结构稳定
- 基本结构
  - 单元格
  - 行
  - 列
  - 跨行
  - 跨列



###  列表,表格,媒体元素

> 列表

```html
<!--有序列表
orderlist 和list简写
应用范围：试卷，问答。。。
-->
<ol>
    <li>java</li>
</ol>

<!--无序列表
应用范围：导航，侧边栏...
-->
<ul>
    <li>java</li>
</ul>

<!--自定义标签
dl: 标签
dd: 列表名称
dd: 列表内容
-->
<dl>
    <dt>学科号</dt>
    <dd>java</dd>
    <dd>前端</dd>
    
    <dt>位置</dt>
    <dd>北京</dd>
</dl>    
```



> 表格

```html
<!--表格table
行 tr rows
列 td
-->
<table border="1px">
    <tr>
<!--        colspan 跨列-->
        <td colspan="3">1-1</td>
        <td>1-4</td>
    </tr>
    <tr>
<!--        rowspan 跨行-->
        <td rowspan="2">2-1</td>
        <td>2-2</td>
        <td>2-3</td>
        <td>2-4</td>
    </tr>
    <tr>
        <td>3-1</td>
        <td>3-2</td>
        <td>3-3</td>
    </tr>
</table>
```



> 媒体元素

- 视频元素
  - video
- 音频元素
  - audio

```html
<!--音频和视频
 src:资源路径
 controls :控制条
 autoplay:自动播放
-->
<!--<video src="../resourse/video/弱音-彩虹节拍竖屏.mp4" controls autoplay></video>-->

<audio src="../resourse/audio/以冬%20-%20花与剑.mp3" controls></audio>
```



> 页面结构分析

| 元素名  | 描述                                             |
| ------- | ------------------------------------------------ |
| header  | 标题头部区域的内容(用于页面或页面中的一块区域)   |
| footer  | 标记脚部区域的内容(用于整个页面或页面的一块区域) |
| section | Web页面中的一块独立区域                          |
| article | 独立的文章内容                                   |
| aside   | 相关内容或应用（常用于侧边栏)                    |
| nav     | 导航类辅助内容                                   |



> iframe内联框架

```html
<!-- iframe内联框架
src： 引用页面地址
width: 宽度
height: 高度
 name:框架标识名-->

<!--<iframe src="https://www.bilibili.com/" frameborder="0" width="1000px" height="800px"></iframe>-->

<iframe src="" name="hello" frameborder="0" width="1000px" height="800px"></iframe>
<!--通过a标签将内联框架跳转到对应href位置-->
<a href="1.我的第一个网页.html" target="hello">点击跳转</a>

<!--<iframe src="//player.bilibili.com/player.html?aid=55631961&bvid=BV1x4411V75C&cid=97257967&page=11"-->
<!--        scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>-->
```



### 表单及表单应用

> 表单

```html
<!--表单form
action: 表单提交的位置，可以是网站，也可以是一个请求处理地址
method: post, get提交方式
    get方式提交: 我们可以在url种看到我们提交的信息,不安全,搞笑.
    post : 比较安全,传输大文件.
-->

<form action="1.我的第一个网页.html" method="post">

<!--    文本输入框 ：<input type="text">-->
    <p>名字： <input type="text" name="username"></p>

<!--    密码框 <input type="password" name="pwd">-->
    <p>密码： <input type="password" name="pwd"></p>

    <p>
    <input type="submit">
    <input type="reset">
    </p>
</form>
```

| 属性      | 说明                                                         |
| --------- | ------------------------------------------------------------ |
| type      | 指定元素的类型。text、password、checkbox、radio、submit、reset、file、hidden、image和button，默认为text |
| name      | 指定表单元素的名称                                           |
| value     | 元素的初始值。type为radio时必须指定一个值                    |
| size      | 指定表单元素的初始宽度。当type 为text或password时，表单元素的大小以字符为单位。对于其他类型，宽度以像素为单位 |
| maxlength | type为text或 password时，输入的最大字符数                    |
| checked   | type为radio或checkbox时，指定按钮是否是被选中                |

详见10.学习表单.html



> 表单应用

- 隐藏域 hidden
- 只读 readonly
- 禁用 disabled



### 表单初级验证

 

- 思考 为什么要进行表单验证
- 常用方式
  - placeholder 提示信息
  - required  非空判断
  - pattern 正则表达式

### HTML总结

