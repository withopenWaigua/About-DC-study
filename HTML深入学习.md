# HTML深入学习



## 网页结构分析

| 元素名  |                      描述                      |
| ------- | :--------------------------------------------: |
| header* |  标题头部区域内容（用于页面或页面的一块区域）  |
| footer* | 标记脚部区域的内容（用于页面或页面的一块区域） |
| section | Web中页面的一块独立区域（一般可作为网页主体）  |
| article |                 独立文章的内容                 |
| aside   |         相关内容或应用（常用于侧边栏）         |
| nav*    |                 导航类辅助内容                 |

```
<body>
<header>
    <h2>网页头部</h2>
</header>
<section><h2>网页主体</h2></section>
<footer>
    <h2>网页脚部</h2>
</footer>
</body>
```



## iframe内联框架

构建直接显示的内联框架：

```
<iframe src="https://www.baidu.com" frameborder="0" width="800px" height="1000px"></iframe>
```

构建跳转的内联框架：

```
<!--构建一个空的iframe框架（src为空，不直接显示）
用hello命名框架
href内的可填url
页面先只显示一个点击跳转
点击跳转后进入iframe内联框架，其跳转网页为href的网址--百度
-->
<iframe src="" name="hello" frameborder="0" width="800px" height="1000px"></iframe>
<a href="www.baidu.com" target="hello">点击跳转</a>
```





**！！！以下需要上传的所有数据都需要指定一个name，以区分它的类型再上交服务器！！！**



## 表单提交

action：提交到的地方，网站或请求处理的地方

method：get，post

​				get：在url能看到我们的信息，不安全但高效

​				post：比较安全，且可以传输大文件

```
<form action="https://www.baidu.com" method="post">
    <p>账号：<input type="text" name="user-name"></p>
    <p>密码：<input type="password" name="pwd"></p>
    <p>
    <input type="submit">
        <input type="reset">
    </p>
</form>    简单的账号密码框的构建
```





### 文本框

```
<p>名字：<input type="text" name="user-name" value="请输入账号" maxlength="8" size="30"></p>
```

value：默认文本框内显示的值

maxlength：最大可输入的长度

size：文本框的长度



### 单选框

```
<p>性别:
    <input type="radio" value="boy" name="sex" />男
    <input type="radio" value="girl" name="sex" checked/>女
</p>
```

单选框默认选择女性

单选框：type="radio"

value=值，

外面的只是显示内容

**必须填value值**

**且如果要单选就得指定他们的name是一样的（保证其为同一组标签）**

**不然因为他们的组不同都是可以选的，且可以被一并提交**



### 多选框



```
<p>爱好：
    <input type="checkbox" value="sleep" name="hobby">睡觉
    <input type="checkbox" value="sleep" name="hobby">敲代码
    <input type="checkbox" value="sleep" name="hobby">聊天
    <input type="checkbox" value="sleep" name="hobby" checked>游戏
</p>
```

多选框，默认是选择男性



### 按钮

```
按钮:<input type="button" name="button1" value="请点击我">
图片形成点击按钮：<input type="image" src="../">
```

value值是按钮显示的文本



### 下拉框

```
国家：
    <select name="列表名称" id="">
        <option value="China">中国</option>
        <option value="US">美国</option>
        <option value="RS" selected>瑞士</option>
        <option value="india">印度</option>
    </select>
```



### 文本域

可以写多行文本

```
<textarea name="textarea" cols="50" rows="10">文本内容</textarea>
```



### 文件域

可以上传文件

```
<input type="file" name="file">
```



### 自带验证效果的信息提交

```
<input type="email" name="emali">
<input type="url" name="url">
<input type="number" name="num" max="100" min="10" step="10">
```

email：能简单判断输入的邮件（但不够准确）

url：判断是否为网址

number：可以输入数量，验证最大需要为100，最小需要为10，且点击上调的步长为10



### 音量滑块

```
<input type="range" min="0" max="100" name="voice" step="2">
```

max音量最大可调到的数值

min音量最小的数值

step：调动的步长



### 搜索框

```
<input type="search" name="search">
```



### 标签更改禁止

后面加readonly：只能看，不能改

后面加disabled：不能选



### 隐藏标签

后面加hidden就看不到标签了，隐藏了但标签仍然在



###  增强鼠标的可用性

```
<label for="mark">点击就自动到文本框内</label>
<input type="text" id="mark">
```

点击上面显示的文字，鼠标指标自动到下面的输入框内



## 表单的初级验证



### 内容提醒

```
标签控件后+（需要输入的文本框）placeholder="XX"
```

显示让用户输入什么内容



### 不能为空

```
<input type="search" name="search" required>
```

不能留空白



### 正则表达式验证

```
<input type="search" name="search" pattern="正则表达式">
```

