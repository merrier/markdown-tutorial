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

除了用`#`来表示标题，还可以用在底部添加`=`（任意数量）的方式表示一级标题和二级标题：

```
一级标题
=
二级标题
==
```

#### 效果：

一级标题
=
二级标题
==

### 斜体、粗体、删除线

通过成对的`**`和`__`表示加粗字体；通过成对的`*`和`_`表示倾斜字体；通过成对的`~~`表示删除字体：

> 斜体、粗体、删除线可混合使用

|语法|效果|
|----|-----|
|`*斜体1*`|*斜体1*|
|`_斜体2_`| _斜体2_|
|`**粗体1**`|**粗体1**|
|`__粗体2__`|__粗体2__|
|`这是一个 ~~删除线~~`|这是一个 ~~删除线~~|
|`***斜粗体1***`|***斜粗体1***|
|`___斜粗体2___`|___斜粗体2___|
|`***~~斜粗体删除线1~~***`|***~~斜粗体删除线1~~***|
|`~~***斜粗体删除线2***~~`|~~***斜粗体删除线2***~~|


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

### 列表

使用`*`、`+`或`-`加上一个空格表示无序列表，列表可嵌套：

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
```
* 编程语言
    * 脚本语言
        * Python
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
* 编程语言
    * 脚本语言
        * Python

使用数字加英文句号加空格表示有序列表，和无序列表一样，也可以嵌套：

```
1. item1
2. item2
7. 不用担心数字不对，显示的时候我们会自动把这行的 7 纠正为 3
```

```
1. 这是一级的有序列表，数字1还是1
   1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的有序列表，数字在显示的时候变成了英文字母
```

#### 效果：
1. item1
2. item2
3. 不用担心数字不对，显示的时候我们会自动把这行的 7 纠正为 3
---
1. 这是一级的有序列表，数字1还是1
   1. 这是二级的有序列表，阿拉伯数字在显示的时候变成了罗马数字
      1. 这是三级的有序列表，数字在显示的时候变成了英文字母

### 代码

通过成对的\`\`\`表示代码，同时后面可以加上编程语言的名字，代码段落则是在每行文字前加4个空格或者1个缩进符表示。（\`在键盘数字1的左边）：

#### 效果：

```langName
代码片段
    代码段落
```
如果不需要代码高亮，可以用下面的方式禁用：

```nohighlight
不需要高亮的代码片段
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

> Markdown不能设置图片大小，如果必须设置则应使用HTML标记`<img>`，见高级用法中的HTML标签

```
这是一张图片：![图片替代文本](image url 'image title')
```

#### 效果：

这是一张图片：    ![Merrier说](./src/qrcode.jpg 'Merrier说')


### 表格

用`|`表示表格纵向边界，表头和表内容用`-`隔开，并可用`:`进行对齐设置，两边都有`:`则表示居中，若不加`:`则默认左对齐：

> 表格中可以添加图片、加粗字体、斜体等markdown元素

```
|默认居左|        居左      |       居右       |       居中      |
|------|:-----------------|----------------:|:--------------:|
|默认居左|只有左侧有`:`表示居左|只有右侧有`:`表示居右|两侧都有`:`表示居中|
```

#### 效果：

|默认居左|        居左      |       居右       |       居中      |
|------|:-----------------|----------------:|:--------------:|
|默认居左|只有左侧有`:`表示居左|只有右侧有`:`表示居右|两侧都有`:`表示居中|



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

|语法|效果|
|---|---|
|```\\```|\\|
|```\*```|\*|
|```\_```|\_|
|```\{\}```|\{\}|
|```\[\]```|\[\]|
|```\(\)```|\(\)|
|```\#```|\#|
|```\+```|\+|
|```\-```|\-|
|```\.```|\.|
|```\!```|\!|


### HTML标签

markdown中可以插入html标签，包括`<kdb> <b> <i> <em> <sup> <sub> <br>`，如：

|语法|效果|
|---|---|
|`[回到顶部](#markdown-tutorial)`|[回到顶部](#markdown-tutorial)|
|```使用 <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Del</kbd> 重启电脑```|使用 <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Del</kbd> 重启电脑|
|```<pre>代码块</pre>```|<pre>代码块</pre>|
|```<b>加粗字体</b>```|<b>加粗字体</b>|


### 锚点

#### 效果：

其实在Markdown文件中，每一个标题都是一个锚点，和HTML的锚点（`#`）类似，比如我们

|语法|效果|
|---|---|
|`[回到顶部](#markdown-tutorial)`|[回到顶部](#markdown-tutorial)|

不过要注意，标题中的英文字母都会被转化为**小写字母**。
> 以前GitHub对中文支持的不好，所以中文标题不能正确识别为锚点，但是现在已经没问题啦！


### 任务列表

`- [x] 内容1`表示内容1已完成，`- [ ] 内容2`表示内容2未完成，一般使用这个功能来标注某个项目各项任务的完成情况

```
- [x] 已完成
- [ ] 未完成
```

#### 效果：

- [x] 已完成
- [ ] 未完成


### 表情

Github的Markdown语法支持添加emoji表情，输入不同的符号码（两个冒号包围的字符）可以显示出不同的表情。

比如`:blush:`，可以显示:blush:。

具体每一个表情的符号码，可以查询GitHub的官方网页[http://www.emoji-cheat-sheet.com](http://www.emoji-cheat-sheet.com)。

但是这个网页每次都打开奇慢。。所以有位大牛整理到了自己的repo中，大家可以直接在此查看[emoji](http://github.com/guodongxiaren/README/blob/master/emoji.md)。


### diff语法
版本控制的系统中都少不了diff的功能，即展示一个文件内容的增加与删除。GFM中可以显示的展示diff效果。使用绿色表示新增，红色表示删除。

其语法与代码高亮类似，只是在三个反引号后面写diff，并且其内容中，以 `+ `开头表示新增，`- `开头表示删除：

```
```diff
+ 新增内容
- 删除内容
```

#### 效果：

```diff
+ 新增内容
- 删除内容
```


### 公式

当你需要在编辑器中插入数学公式时，可以使用两个美元符`$$`包裹TeX或LaTeX格式的数学公式来实现，并且支持HTML属性：

```
$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a}. $$
$$
(x+1)^2 = \cssId{step1}{\style{visibility:hidden}{(x+1)(x+1)}}
$$
```

$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a}. $$
$$
(x+1)^2 = \cssId{step1}{\style{visibility:hidden}{(x+1)(x+1)}}
$$


### GFM VS SM

下面对GFM和SM的区别进行一下总结：

* GFM二级标题自动带有下划线
* GFM在issue中通过`#和数字`自动链接到对应的issue（request也支持）（eg：#1）
* GFM自动识别链接，链接不用尖括号括起来也会被认为是链接。
* GFM实现代码语法高亮
* GFM自动@别人
* GFM自动引用，包括项目，用户名，issue等
* GFM支持上面介绍过的任务列表


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
* [MarkDown书写规范](https://github.com/hoosin/MarkDown)
* [Markdown 编辑器语法指南](https://segmentfault.com/markdown)
* [Markdown 基本语法](https://github.com/younghz/Markdown/tree/master)
* [README文件语法解读](https://github.com/guodongxiaren/README)
* [markdown-it](https://markdown-it.github.io/)

### 题外话

不同的Markdown解释器或工具对相应语法（扩展语法）的解释效果不尽相同，具体可参见工具的使用说明。 虽然有人想出面搞一个所谓的标准化的Markdown，[没想到还惹怒了健在的创始人John Gruber](http://blog.codinghorror.com/standard-markdown-is-now-common-markdown/)。