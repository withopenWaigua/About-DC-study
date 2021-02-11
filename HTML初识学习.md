# HTML基础知识



## 什么是HTML？

HTML: Hyper Text Markup Language (超文本标记语言)

目前常用HTML5+CSS3+js编写网页



互联网需要统一标准，因此W3C（万维网联盟）制定了相关标准：

- 结构化标准语言（HTML、XML）

- 表现标准语言（CSS）

- 行为标准[DOM(文档对象)、ECMAScript（JavaScript需要遵守其规范）]

  

## IDEA中编写HTML的命令

**生成某一种标签的快捷方法：先写标签英文，再按下Tab键**

```
<!-- X --> ：X内填写注释，可以使用CTRL+/ 快速创建
```



## ————编写HTML标签————



## 特殊符合

```
&nbsp;  每一个&nbsp; 代表每一个空格，需要几个空格就用几次(PS:字符串内无论N个空格，只会显示一个空格)
&gt;	>号标志
&lt;	<号标志
&copy;	© 商标号标志
........
```



## 基础标签

head标签：代表网页头部  

- title标签：网页的标题
- meta-描述类标签，用来描述我们网站的信息（一般用来做SEO ，可以写入name、content等相关信息）

```
<body>	代表网页主体
```

```
<!DOCTYPE html>  告诉浏览器使用HTML规范
```

```
<hN>：N级标题标签  
```

```
<p>：段落标签
```

```
<br/>：换行标签，是自闭合标签，只用写一个在末尾，且换行紧凑，无段落标签的段落空行
```

```
<hr/>:水平线标签，也是自闭合标签，画一条分割线
```

```
<strong>：粗体标签	
```

```
<em>：斜体标签
```



## 图像标签

```
<img src="" alt="" title="" width="" height="">
src一般写相对路径	(../图片文件夹/图片文件名.jpg)    必填
alt内写找不到图片后返回的信息内容 					 必填
title内写图片显示的悬停文字
width内写图片的宽带
height内写图片的高度
```



## 链接标签

**链接标签**：**用于点击跳转的标签**

```
<a href="" target="">	</a>
href：要跳转的链接
双标签中间填写超链接的显示文字或者嵌套显示图片（<img src="" alt="" title="" width="" height="">）
target="" ：超链接打开方式，默认在当前页面跳转（target="_self"）
target="_blank" ：在新的页面打开
```



### 锚链接

**#**:锚链接的跳转

```
<a name="top">标记</a>
<a href="（其他网页）#top">回到顶部</a>   用#+标签名作为超链接（跨网页跳锚链接：前面还可以加其他网页，这样可以直接跳到其他网页的top标记处）
```

1.需要一个锚标记 :	\<a name="top">可填标记处的文字信息</a>

2.跳转到标记:	\<a href="#top">显示文字信息</a>



### 功能型链接

可以打开email，QQ等

类似QQ推广链接：

\<a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=&site=qq&menu=yes"><img border="0" src="http://wpa.qq.com/pa?p=2::52" alt="给我发信息" title="给我发信息"/></a>



## 行内元素和块元素

块元素:无论内容多少独占一行（p、hN）

行内元素：内容撑开宽度，可以排在一行（a、strong、em）



## 列表标签

### 有序列表

ol标签下用li标签表示

前面自带123.....

```
<ol>
    <li>内容</li>
    <li>内容</li>
</ol>
```





### 无序列表

有序列表：ul标签下用li标签表示

前面自带小黑点

```
<ul>
    <li>内容</li>
    <li>内容</li>
</ul>
```



### 自定义列表

dl：表示自定义标签

dt：列表名称

dd：列表内容

无数字和小黑点，但前面有列表名称

```
<dl>
	<dt></dt>
    <dd></dd>
</dl>
```





## 表格标签

table标签下

border：代表分割线

tr：表示行

tr嵌套的td代表每一行的每一列（有几个td每一行就有几列）

```html
<table border="1px">
    <tr>
        <td>1-1</td>          
        <td>1-2</td>          
    </tr>
    <tr>
        <td>2-1</td>
        <td>2-2</td>
    </tr>
</table>
```

### 跨列

（colspan="2"：跨两列）

```
<table border="1px">
    <tr>
        <td colspan="2">1-1</td>                   
    </tr>
    <tr>
        <td>2-1</td>
        <td>2-2</td>
    </tr>
</table>
```

### 跨行

（rowspan="2"，第一个跨两行）

```
<table border="1px">
    <tr>
        <td rowspan="2">1-1</td>
        <td>1-2</td>
    </tr>
    <tr>
        <td>2-1</td>

    </tr>
</table>
```



## 添加媒体元素



### 添加视频

```
<video src="../文件夹/XX.MP4" controls autoplay></video>
```

src：资源路径

contros：控制条元素 

autoplay：自动播放



### 添加音频

与视频同理

```
<audio src="../文件夹/XX.MP3" controls autoplay></audio>
```



