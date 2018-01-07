# markdown-tutorial

Markdown是一个将文本转化为HTML的工具。简单来说，Markdown是一个兼顾可读性与易用性的轻量级标记体系。Markdown并不追求大而全，它只关心HTML里最常用的几个标记，对于一些不常用的标记它允许直接将HTML标记插入文本。

## 基本用法

### 标题

一共有六级标题，用1-6个`#`来表示：
```
# 一级标题
## 二级标题
###### 六级标题
```

#### 效果：

# 一级标题
## 二级标题
###### 六级标题

除了用`#`来表示标题，还可以用在底部添加`=`的方式表示一级标题和二级标题：

```
一级标题
=
二级标题
=
```

#### 效果：

一级标题
=
二级标题
=

### 加粗

通过成对的`**`和`__`表示加粗字体：

```
**这里是需要加粗的内容**
__这里是需要加粗的内容__
```

#### 效果：

**这里是需要加粗的内容**

__这里是需要加粗的内容__

### 斜体

通过成对的`*`和`_`表示倾斜字体：

```
*这里是需要倾斜的内容*
_这里是需要倾斜的内容_
```

#### 效果：

*这里是需要倾斜的内容*
_这里是需要倾斜的内容_

### 分隔线

在一行中使用三个或三个以上的`*`、`-`或`_`可以添加分隔线，其中可以有空白，但是不能有其他字符：
```
***
---
___
```

#### 效果：
---

### 引用

行首使用`>`加上一个空格表示引用，可嵌套使用：

```
> 这里是引用的内容
> > 嵌套内容
```

#### 效果：
> 这里是引用的内容
> > 嵌套内容

### 删除字体

通过成对的`~~`表示删除字体：
```
~~删除他~~
```

#### 效果：
~~删除他~~

### 列表

使用`*`、`+`或`-`加上一个空格表示无序列表：

```
* item1
* item2
* item3
```
```
+ item1
+ item2
+ item3
```
```
- item1
- item2
- item3
```
#### 效果：
* item1
* item2
* item3
+ item1
+ item2
+ item3
- item1
- item2
- item3

使用数字加英文句号加空格表示有序列表：

```
1. item1
2. item2
3. item3
```

#### 效果：
1. item1
2. item2
3. item3

### 代码

通过成对的\`\`\`表示代码，代码段落则是在每行文字前加4个空格或者1个缩进符表示。（\`在键盘数字1的左边）：

#### 效果：

```langName
代码片段
    代码段落
```


### 标记

通过成对的\`和\`\`表示代码。（\`在键盘数字1的左边）：

```
`标记`
```

#### 效果：
`标记`

### 链接

以中括号标记显示的链接文本，后面紧跟用小括号包围的链接。如果链接有title属性，则在链接中使用空格加"title属性"：

```
[链接文本](url 'url title')
```

#### 效果：

[Merrier说](http://www.merrier.wang 'Merrier说')

### 图片

图片的使用方法基本上和链接类似，只是在中括号前加叹号。

> Markdown不能设置图片大小，如果必须设置则应使用HTML标记`<img>`，见高级用法中的html标签

```
这是一张图片：![图片替代文本](image url 'image title')
```

#### 效果：

这是一张图片：    ![Merrier说](./src/qrcode.jpg 'Merrier说')



## 高级用法


### 换行

在文字的末尾使用两个或两个以上的空格来表示换行。

### 引用链接/图片

和基础用法里面的链接类似，一般应用于多个不同位置使用相同链接。通常分为两个部分，调用部分为`[链接文本][ref]`；定义部分可以出现在文本中的其他位置，格式为`[ref]: http://some/link/address`，图片类似，在中括号前加`!`即可：

> ref中不区分大小写。

```
[ref]: http://merrier.wang

这是一个[引用链接][ref]
```

#### 效果：

[ref]: http://merrier.wang

这是一个[引用链接][ref]


### 自动链接

使用`<>`，可以为输入的URL或者邮箱自动创建链接：

```
<953075999@qq.com>
```

#### 效果：
<953075999@qq.com>

### 转义字符

Markdown中的转义字符为`\`，可以转义的有：

* ```\\``` 反斜杠 \\
* \` 反引号 \`
* ```\*``` 星号 \*
* ```\_``` 下划线 \_
* ```\{\}``` 大括号 \{\}
* ```\[\]``` 中括号 \[\]
* ```\(\)``` 小括号 \(\)
* ```\#``` 井号 \#
* ```\+``` 加号 \+
* ```\-``` 减号 \-
* ```\.``` 英文句号 \.
* ```\!``` 感叹号 \!




### 语法

* [官方语法](http://daringfireball.net/projects/markdown/syntax)
* [GitHub MakDown 语法](https://github.com/mojombo/github-flavored-markdown/issues/1)
* [PDF版本](./src/MarkDown%E8%BD%BB%E9%87%8F%E7%BA%A7%E6%A0%87%E8%AE%B0%E8%AF%AD%E8%A8%80.pdf?raw=true)

### Markdown编辑器

#### Windows 平台

* [MarkdownPad](http://markdownpad.com/)
* [MarkPad](http://code52.org/DownmarkerWPF/)
* [mdcharm](http://www.mdcharm.com/)

#### Linux 平台

* [ReText](http://sourceforge.net/p/retext/home/ReText/)

#### Mac 平台

* [Mou](http://mouapp.com/)
* [DayOne](http://dayoneapp.com/)

#### 在线编辑器

* [Draftin](https://draftin.com/)：功能强大，可发布到各种博客平台。
* [Dillinger](http://dillinger.io/)：实时预览，支持直接保存到Dropbox或是Github。
* [Markable](http://markable.in/)：实时预览，支持发布到Tumblr。
* [Oak](http://oakoutliner.com/)：不支持发布到任何地方，供在线随手记录东西使用。
* [简书](http://jianshu.io/)：国产软件，看上去不错。

#### 浏览器插件

* [MaDe](https://chrome.google.com/webstore/detail/oknndfeeopgpibecfjljjfanledpbkog) (Chrome)


### Users

* GitHub
* 简书
* Stack Overflow
* Apollo
* Moodle
* Reddit
* ...


### 参考链接

* [Markdown语法示例](http://equation85.github.io/blog/markdown-examples/)


### 需要总结的链接地址

* https://github.com/gmosx/markdown
* https://github.com/guodongxiaren/README
* https://github.com/hoosin/MarkDown
* https://markdown-it.github.io/
* https://github.com/younghz/Markdown/tree/master
* https://github.com/GitbookIO/markdown
