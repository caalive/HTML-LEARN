# HTML && CSS LEARN

**000_simple-html-doucment**

```
<!DOCTYPE html> 
标签的作用是，告诉浏览器这是一个 html 文档
<html lang="en">
告诉浏览器使用的语言
<body>
	body 标签内元素被显示在界面上。
</body>

<head>
	head 标签内的元素不被显示在界面上。
</head>

HTML			--> structure
CSS				--> formating
JAVASCRIPT	--> functionality

```
**Self-closing tags**

```
<meta>
<link>
<hr>
<br>
<img>
<input>
<source>
<embed>
<param>
<wbr>
```
**html基本标签中不带斜杠的标签称为开始标签，带斜杠的标签为结束标签。**

head标签用于给网站添加一些配置信息。或者指定网站的小图标，添加网站SEO的相关信息。只定网站的描述信息，外挂一些JS CSS文件。或者添加一些浏览器的相关内容。
#####注意点：
		一般情况下head标签中内容不会显示给用户查看，也就是写在head标签中的内容给浏览器用的。
title标签的作用是专门用于只定网站的标题，并且这个只定的标题将来还会作为用户保持网站的默认标题。

**body标签专门用来包含显示给用户查看的内容的，一对html标签中只能有一对body标签**

**字符集问题 meta标签的作用是指定当前网页的字符集，不指定当前网页的字符集会导致网页乱码,网页中常见的字符集有GBK和UTF-8**
在网页中指定字符集的意义在于告诉浏览器我使用的是哪个字符集

- 字符集注意点
	- 在html中指定的字符集要和保存的文件的字符集要一致。不然在加载html解析时会导致乱码问题。解决问题的办法是将文件另存为，保存为和html文件中指定的字符集一致。

- 标签分类
	- 单标签
		- 只有开始标签没有结束标签即 <>标签
	- 双标签
		- 由开始标签和结束标签组成的标签 即 <></>标签

- 标签有并列关系和嵌套关系。
- DTD 文档声明
	- 在html网页开头位置写入 <!DOCTYPE html> 浏览器看到此声明就认为这个文档类型为 html5网页类型, 浏览器就使用html5规范来解析该网页, html5 网页类型是向下兼容的。任何一个标准的html网页第一行一定是 DTD文档声明，DTD文档声明不区分大小写。
	- 浏览器并不会完全依赖DTD文档声明。


##WebStorm元素快捷创建语法
### 创建子元素使用 > 大于号
- html>head 按下 Tab键即可在 html标签中创建 head标签
- 在一段内容前后加上一个标签， 按住 ctrl+alt+t选择 tag

## 基础标签学习
### H系列标签学习（Header1～Header6）
- 格式：
	-  `<h1>XXX</h1>`
- H标签是用来给文本添加语义的，而不是用来修改文本样式的
- H标签一共有6个从H1～H6超过 H6则无效。被H标签包裹的元素单独占一行
- 在H系列的标签中 H1 最大 H6最小。在企业开发中要慎用H系列标签，并且在一个页面中一般情况下只能有一个 H1 标签。和SEO有关

### P标签（Paragraph）	
- 作用
	- 用来告诉浏览器哪些文字是段落
	- 格式：
		- `<p>XXX</p>` 
	- 注意点
		- 	被p标签包裹的文本，会单独占据一行
		
### Hr标签
- 作用
	- 在浏览器中实现一条水平线
- 格式：
	- `<hr/>`是单标签
- 注意点：
	- 在浏览器中单独占据一行
	- 在html5规范中hr后面不写 / 斜杠，一样可以正常解析，如果不写/按照html规范来编写，写/则按照xhml规范来编写。

### img 标签
- img标签告诉浏览器，将要显示一个图片
- 格式：
	-` <img src="">`img标签中src就是用来告诉img标签，需要显示的图片名称是什么
- 注意点：
	- img 标签不会独占一行
	- img 有 width， height 宽高属性,如果没有指定宽高，则按照默认宽高来显示图片, 如果手动指定宽高属性，有可能使图片变形失真，如果想指定宽高又不想让图片显示失真，则只需要指定宽高中的其中一个属性即可，系统会根据宽高自动计算另一个属性进行等比拉伸，不会造成图片显示失真。
	- title属性的作用，当鼠标悬停在图片上时，弹出框将要显示的内容
	- alt 属性当需要加载的图片找不到时，系统显示的图片描述信息

### br标签
- br标签的作用是用来换行的，br标签是单标签
- br标签的注意点，br标签可以连续使用，使用多少个br就可以换多少行
- br标签不起另一个段落换行，企业开发中一般情况下需要换行都是因为需要另起一个段落，一般不使用br换行。br代表不另起一行换行，它的语义是这个。如果一个段落没有描述完需要换行则使用br标签，描述完了则使用能单独占据一行的标签。

### 路径问题
- 给img的src赋值有两种方式
	- 通过相对路径,每次都从html文件所在的文件夹开始查找，同级目录直接写图片名称即可.
	- 下级目录
		- html文件和存储图片的文件夹，在同一级目录中
		- `<img src="images/letter.jpg" alt="这是图片"> <!--下级目录图片地址-->`
	- 上级目录
		- 上级目录就是存储html文件的文件夹和图片在同一级目录中
		- `<img src="../letter.jpg" alt="这是图片"> <!--上级目录图片地址-->`
	- 通过绝对路径
		- 每次都从指定的盘符开始查找

### a标签的基本使用
- a标签的作用用于控制页面与页面之间跳转的
- 注意点，a标签不仅可以让文字可以点击，也可以让图片可以点击。
- 一个a标签必须有一个href属性，否则a标签不知道跳转到哪里
- 如果通过a标签的href属性指定一个URL地址，那么必须在地址前面加上http://或者https://
- a标签的href属性除了可以跳转到网络上的地址也可以跳转到本地的地址
- a标签有一个target属性，这个属性的作用就是用来控制，页面如何跳转。一个是 `_self`，一个是`_blank`属性。`_self`属性在当前的选项卡中跳转，`_blank`新建一个选项卡.
- a标签中的title属性用来控制，鼠标悬停时显示的文本.
- a标签假链接，点击之后不会跳转的链接为假链接。
- 假链接格式一个是 # 另一个是 javascript：
- 两者之间区别，#号的假链接会回到网页的顶部。另一个不会回到顶部
### base标签
- 就是专门用来指定当前网页中所有的超链接也就是a标签的打开行为的。属性target的使用方法和a标签的使用方式一致。
- 注意点：base标签必须写在 head标签中。
- 如果既在base标签中指定了target属性又在a标签中指定了target属性，则浏览器按照a标签中指定的target属性，来打开网页。

### 锚点
- 使用a标签的锚点功能实现，在当前页面中跳转到指定位置
- 通过a标签跳转到指定位置，给跳转到位置添加一个id, 使用方式为#id，跳转为直接跳转，没有滚动效果。
- a标签除了可以跳转至本页到指定位置，还可以跳转到其它页面的指定位置。

### 列表标签的基本使用
- 列表标签的作用，给一堆数据添加列表语义。告诉浏览器这堆数据是一个整体。
- 列表标签分类
	- 无序列表（最多）unordered list
		- 给一堆数据添加列表语义，数据次序没有先后之分
		- 格式`<ul> <li>XXX</li> </ul>` li = list item
	- 注意点：
		- ul 标签是给数据添加语义的，不是添加小圆点的
		- ul标签和li标签是组合使用的，不会单独出现
		- 由于 ul标签和li标签是一个组合，不推荐包含其它标签。但是可以在li标签中继续添加其它标签。
	- 无序列表应用场景
		- 新闻列表
		- 商品列表
		- 导航条
	- 有序列表（最少）ordered list
		- 有序列表中所有数据都有序。
	- 定义列表（一般）definistion list
		- 格式 `<dl> <dt>XXX</dt> <dd>XX</dd></dl>`
		- dt用来定义列表中标题
		- dd用来定义标题对应的描述
		- 作用和无序有序列表一样，区别是先通过dt定义标题，然后通过dd定义描述。
		- 应用场景：做网站尾部的相关信息。还可以做图文混排。
		- 定义列表注意点：和ul，ol一样是一个整体，所以不会单独出现，dl中建议只放 dt和dd。推荐使用一个dt对应一个dd。当需要丰富界面时可以在dt和dd标签中，添加其它标签。
	- 通过标签属性可以修改样式，但是在企业开发中不推荐这么使用，定义样式一定要使用CSS样式来定义

### 表格标签的基本使用
- 表格标签作用，用来给数据添加表格语义。
- 表格标签被div和CSS取代了现在，一般不常使用了。
- 表格标签格式：
- `<table> <tr> <td> </td> </tr></table>`
- 表格标签中的 table代表整个表格，tr代表整个表格中的一行数据，一个tr标签就是表格中的一行。td标签代表一行的一个单元格。
- 注意点
	- 表格标签有一个边框属性，默认情况下边框值boder为0,所以表格不显示。
	- 表格标签和列表标签是一个组合标签。
- 表格标签的宽度和高度属性
	- 可以给table标签和td标签使用，tr标签不能使用
	- 表格的宽度和高度默认是按照内容的尺寸来调整的，也可以通过给table标签设置宽高属性方式来手动指定。
	- 给td标签设置了宽高属性后只会影响当前的单元格的宽高，不会影响整个表格的宽高。
- 水平对齐和垂直对齐属性
	- 水平对齐可以给table标签tr标签td标签使用
	- 给table设置aligen属性可以控制表格在水平方向的对齐方式。
	- 垂直对齐只能给tr标签td标签使用.
	- valign用来设置单元格的数据的垂直方向的对齐方式
- 外边距和内边距属性
	- 单元格与单元格之间的距离称为外边距,默认的外边距为2px,`cellspacing`属性用来设置表格的外边距。
	- 内边距是指表格中的数据与单元格边框之间的距。内边距属性设置使用 `cellpadding` 来设置,默认情况下内边距为1px.
	- 只能给table标签使用。
- 细线表格
	- 在表格标签中想通过将表格外边距设置为0即 `cellspacing=0`是做不到的，只能将单元房格的线和表格线重合。
	- 细线表格的制作方式是将table的`cellspacing`属性设置为1px，table的`bgcolor=black`然后将tr的`bgcolor=white`,即可制作出细线表格。
- 表格中其它标签
	- 表格标题`caption`,标签使用时一定要写在table标签中，否则无效。一定要紧跟在table标签后面。则表格标题就会自动处于表格的中心位置。
	- 标题单元格标签`th`,只要将当前列的标题存储在这个标签中，标题就会自动居中并且加粗。
	- 表格中有两种单元格，一种是td，一种是th，th是用来存放表格的标题的，td是用来存储数据表格的数据的。
- 表格结构
	- 表格中存储的数据比较复杂，所以表格中存储的数据可以分为四类
		- 表格的标题
		- 表格的表头信息
		- 表格的主体信息
		- 页尾信息
- 表格的完整结构

` <atble> <caption> 表格的标题 </caption> <thead></thead> <tr> <th> 表格的表头 </th> </tr> <tbody> <tr> </tr><td> 表格的数据 </td></tbody> <tfoot> <tr> <td> 表格尾部信息</td> </tr></tfoot>
</table>`

- caption作用：指定表格的标题
- thead的作用：指定表格的表头信息
- tbody作用：指定表格的主体信息
- tfoot作用：指定表格的附加信息
- 注意点:
	- 当更改表格的高度时，表格的表头和表尾信息，不会随着表格设定的高度更改而更改。
- 表格单元格合并
	-  单元格水平合并,给td标签添加`colspan`属性，并设置值。并需要删除一些单元格，才能正常显示。
	-  单元格合并永远是向后或者向下合并。
	-  单元格垂直合并，给td标签添加`rowsspan`属性，并设置值。并需要删除一些单元格，才能正常显示。