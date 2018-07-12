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


## WebStorm元素快捷创建语法
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
` <atble> <caption> 表格的标题 </caption> <thead></thead> <tr> <th> 表格的表头 </th> </tr> <tbody> <tr> </tr><td> 表格的数据 </td></tbody> <tfoot> <tr> <td> 表格尾部信息</td> </tr></tfoot></table>`

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

### 表单标签学习
- 什么是表单
	- 表单就是专门用来收集用户信息的。
- 什么是表单元素
	- 表单元素是html标签，在浏览器中表单标签有特殊的外观和功能。
- 表单的格式
	- `<form> <表单元素> </form>`
- 常用表单元素
	- input标签有一个type属性，这个属性有很多取值，值不同则表现形式也不同。
		- type=text 是一个文本输入框
		- type=password 是一个密码输入框
		- type=radio 是一个单选框，默认情况下单选框不互斥，要想有互斥，必须给单选框设置一个name属性，name属性必须设置相同的值。若想让单选框设置默认值，则添加一个checked=checked属性。
		- type=checkbox 是一个多选框,checkbox可以设置多个默认选择。
		- type=button 是一个按钮,values属性可以设置按钮的标题。
		- type=image 是一个图片按钮, 通过src指定图片的路径。
		- type=reset 是一个重置按钮，重置按钮有默认的标题，叫做重置。不想使用默认的标题则可以指定value属性，重新设置。
		- type=submit 是一个提交按钮。用来提交数据。要想把数据提交到远程服务器必须满足两个条件，一个是哪些数据要提交，二是提交到哪个服务器。提交哪些数据只需要在标签中写有name属性，含有name属性的标签都会被提交到服务器。
		- type=hidden 是一个隐藏域。作用是用来收集用户数据的。隐藏域不会出现在界面中。
	- label标签
		- 默认情况下文字和输入框是没有关联关系的，也就是说文本框不会聚焦。如果想点击文字时让对应的输入框对焦，那么就需要让文字和文本框进行绑定，绑定就需要label标签。
		- 使用label标签中的for属性来将文字与输入框进行绑定，实现点击文字，输入框实现聚焦的功能。还有一种方式实现，绑定功能就是将文本和输入框，放入label标签中去。
	- dalist标签
		- 给输入框绑定待选线
		- 格式:
			- `<datalist> <option> 待选项内容 </option> </datalist>`
	- 表单标签中其它标签
		- select标签
			- 下拉列表框,不能输入内容但是可以直接在列表中选择值。可以option标签添加selected属性来设置默认选择值。
		- textarea定义一个多行的文本框,可以换行。默认情况下可以无限换行，默认情况下有宽和高。通过col和row可以指定行数和列数。

### 多媒体标签学习
- video标签
	- 作用播放视频
	- 格式：`<video src=""></video>`
	- autoplay属性用来自动播放视频
	- controls属性用来控制是否需要显示控制条
	- poster属性用于视频没有播放之前显示一张占位图片
	- loop属性一般用视频,循环播放。
	- preload属性用于预加载视频,此属性和autoplay属性相冲突。
	- muted属性用于静音。
	- width，height属性用于宽高设置
	- 注意点：
		- 当前通过video标签的第二种格式虽然能够指定所有浏览器都支持的视频格式，但是显然所有浏览器都通过video标签播放视频还有一个前提条件就是浏览器必须支持html5标签，否则同样无法播放视频。为了让所有的浏览器都通过video标签播放视频，以后可以通过一个JS框架叫做，html5media来实现。
- audio音频标签，属性和video标签的属性相同使用方式基本相同。

### 详情和概要标签 details和summary
- 利用summary描述概要信息。利用details展示详情信息.
### marquee标签
- marquee标签作用就是用来制作跑马灯的. 各大浏览器都支持.
- direction属性用来控制滚动方向。
- scorllamount属性用来控制滚动速度,值越大滚动越快，100最快
- loop属性用来控制滚动次数。-1为无限次滚动。
- behavior 属性设置滚动类型，滚动到边界还是什么的。有两个取值，一个是slide滚动到边界就停止，一个是alternate滚动到边界就反弹回来。

### 字符实体
- 在html中对空格回车tab不敏感，多个空格只能显示一个.
- &nbsp 代表空格字符实体。
- &lt 代表小于号字符实体
- &copy 代表版权符号实体。

# CSS学习
- 通过标签修改样式的缺点，需要记忆哪些标签有哪些属性，如果该标签没有这个属性，那么设置了也没有用。
- 当需求变更时需要修改大量的代码才能满足需求。
- HTML只有一个作用，就是用来添加语义的，而修改样式都由CSS来定义。
- 通过CSS来修改样式，不用记忆哪些属性属于哪些标签，当需求变更时，不用 修改大量样式。
- CSS标签需要写在head标签的开始和结束标签之间。
- CSS定义格式为：
	- `<style type="text/css"> XXX </stype>`
	- css有个属性 type， type取值为 "text/css"。
	- `css 选择格式为：标签名称{属性名称:属性值;}
	`
- 注意点：
	- css代码必须写在style标签中，style标签必须写在head标签里面。
	- style标签中的type其实可以不用写，默认的就是type="text/css"
	- 设置样式时，必修按照固定格式来设置: key:value;
	- 其中`:`不能省略.`;`大多数情况下不能省略。

## CSS文字相关属性, 适用于WebStorm快捷语法
- 规定文字样式的属性
	- fs  font-style
		- 取值
			- italic	倾斜
			- normal 	正常，默认正常
- 规定文字粗细的属性
	- fw font-weight
		- 取值
			- bold		加粗
			- bolder	更粗
			- lighter	细线，默认是细线
			- 取值也可以为数字：100-900整百之间。
- 规定文字大小的属性
	- fz font-size
		- 取值
			- px 以像素为单位
			- 注意点通过font-size设置的大小一定要带单位，也就是一定要带 px
- 规定文字字体的属性
	- ff font-family
		- 取值
			- 系统内置太多，不列举。
			- 注意点，如果取值是中文字体，则字体名称需要用双引号或者是单引号括起来。设置的字体必须是系统里存在的字体。
		- 如果设置的字体不存在，系统使用默认的字体来替代。如果不想使用系统默认的字体，可以给定一个备用字体，具体的赋值方式为在前一个字体前面后添加另外一些备选字体，并以逗号分隔开来。`font-family: "abc", "Microsoft Sans Serif";`
		- 想给中英文设置不同的字体。
- 文字属性缩写格式：`font: italic bold 10px "微软雅黑"`
- 属性名称加冒号属性值以空格间隔开来。
- 注意点：
	- 在缩写格式中，有些属性值可以省略 style weight可以省略掉。
	- 在缩写格式中，有些属性值是不可以省略掉，size family不能省略。
	- size 和 family 位置不能随意调换，size必须写在family 前面，并且这两个属性必须写在，其它属性值的后面。

## CSS文本相关属性
- 文本装饰的属性
	- td text-decoration
		- 取值
			- underline 		添加下划线
			- linethrough		添加删除线
			- overline		添加上划线
			- none				去除下划线,用于去除超链接下划线
- 文本水平对齐的属性
	- ta text-align
		- 取值
			- left		左对齐
			- rigth	右对齐
			- center	中心对齐
- 文本缩进的属性
	- ti text-indent
		- 取值
			- em 前缀为数字,常用取值为2em,一个em代表缩进一个文字的宽度。

## 颜色属性
- color 
	- 取值
		- 可以通过对应颜色的英文单词赋值如 color:red;
		- color: rgb(255,0,0); 
		- color: rgba(255,0,0,1); 最后一个参数代表透明度,取值从 0 ~ 1
		- color: #FF0000;
		- color: #F00;

## CSS选择器
- 什么是标签选择器
	- 根据指定的标签名称在当前页面中找到对应的标签。
- 标签选择器
	- 格式：`label name{attrname:attrvalue}`
	- 标签选择器选中的是当前界面中所有的标签，而不能单独选中某个标签。
	- 标签选择器，不论标签嵌套在什么位置都能被选中。
	- 只要是HTML中的标签都可以作为标签选择器。

- id选择器
	- 什么是id选择器
		- 根据指定的id名称找到对应的标签，然后设置属性。
	- id选择器
		- 格式 `#idname {attrname:attrvalue}`
		- HTML中每个标签都有一个属性叫做id，也就是说每个标签都可以设置id。
		- 在同一个页面中id是不能重复的，是唯一的。
		- 在编写id选择器时一定要在id名称前面加上#
		- id的名称不能以数字开头，命名规范同变量命名规范相同。
		- id的名称不能是HTML的标签名称。
		- 一般情况下，在前端开发中id是留给js使用的。可以使用类名作为id的替代选择。
	
- 类选择器
	- 什么是class选择器
		- 根据指定的class名称找到对应的标签，然后设置属性。
	- 类选择器
		- 格式 `.calssname {attrname:attrvalue}`
		- HTML中每个标签都有一个属性叫做类名，也就是说每个标签都可以设置类名。
		- 在同一个页面中类名是可以重复，不是唯一的。
		- 在编写类选择器时一定要在类名称前面加上`.`
		- 类的名称不能以数字开头，命名规范同变量命名规范相同。
		- 类的名称不能是HTML的标签名称。
		- 类名就是专门用来给某个特定的标签设置样式的。
		- 在HTML中每个标签可以同时绑定多个类名，也就是可以设置多个样式。格式就是以空格间隔开来。
	
	- id选择器和class选择器的区别
		- id 唯一不能重复，class可以重复。
		- 一个html标签只能绑定一个id，但是可以绑定多个class名称。
		- id 选择器以`#`号开头，class选择器以`.`开头
		- 在企业开发中应使用class选择器。id给JS使用的，不得已不应使用id选择器。
	- 后代选择器
		- 什么是后代选择器
			- 找到指定标签的所有后代标签，然后设置属性.
		- 格式：
			- `lablename_1 lablename_2{attrname:attrvalue}`
			- 先找到标签名称为1的标签然后再标签名称1里面查找标签名称为2的标签然后再设置样式。
		- 注意点：
			- 后代选择器必须用空格间隔开来，后代不仅仅是儿子也包括孙子/重孙只要是放在指定标签中的都是后代。
			- 后代选择器不仅仅可以使用标签选择器，也可以使用其它的选择器。可以由类名id或者id与id的自由组合形式，来唯一定位需要设置属性的标签。
			- 后代选择器可无限的往下延伸。
	- 子元素选择器
		- 什么是子元素选择器
			- 找到指定标签中所有特定的直接子元素，然后设置属性。
		- 格式:
			- `labelname1>labelname2{attrname:attrvalue}`
			- 找到标签名称1的标签，然后在这个标签中查找所有名称为标签2的元素
			- 子元素选择器只会查找儿子标签，不会查找其它嵌套的标签。
			- 子元素选择器之间需要使用`>`大于号连接,并且不能有空格.
			- 子元素选择器不仅仅可以使用标签，也可以使用id选择器或者是类选择器。
			- 子元素选择器可以通过`>`符号一直延续下去。
	- 后代选择器和子元素选择器异同
		- 不同点
			- 后代选择器使用空格作为连接符号
			- 子元素选择器选择 > 符号作为连接符号
			- 后代选择器会选择所有的特定后代标签，只要是放在指定标签中的标签都会被选中。
			- 子元素选择器只会选中指定标签中，所以特定的直接标签，也就是只会选择中特定的儿子标签。
		- 相同点
			- 后代选择器和子元素选择器都可以使用标签名称或者是id名称或者是类名称又或者是上述的几种组合。只是作为连接的符号不一致而已。后代用空格，子元素用大于符号作为选择器的连接符号。
	- 交集选择器
		- 什么是交集选择器
			- 给所有选择器选中的标签中，相交的那部分标签设置属性.
		- 格式:
			`selector1selector2{attrname:attrvalue}`
		- 注意点：
			- 选择器与选择器中没有任何连接符号。
			- 选择器可以使用标签名类名。
			- 交集选择器仅仅作为了解。
	- 并集选择器
		- 什么是并集选择器
			- 给所有选择器选中的标签设置属性
			- 格式：selector1,selector2{attrname:attrvalue}
			- 注意点:
				 - 并集选择器必须使用逗号`,`作为选择器连接符号.
				 - 和交集一样使用方式。
	- 兄弟选择器
		- 相邻兄弟选择器
			- 格式：`label1+lable2{attrname:attrvalue}`
			- 给指定选择器后面紧跟的那个选择器选中的标签设置属性
		- 通用兄弟选择器
			- 格式：`label1~label2{attrname:attrvalue}`
			- 给指点选择器后面的所有选择器选中的所有标签设置属性
		- 注意点：
			- 相邻兄弟选择器必须使用`+`号作为连接符号
			- 相邻兄弟选择器只能选中紧跟其后的那个标签
			- 通用兄弟选择器必须使用`~`波浪线作为连接符号
			- 通用兄弟选择器选中的是指定选择器选中的所有标签
	- 序选择器
		- CSS3中新增的选择器最具代表性的就是序选择器。
		- 同级别的第几个
			- `labelname:first-child{attrname:attrvalue}`选中同级别的第一个标签
			- `labelname:last-child{attrname:attrvalue}`选中同级别的最后一个标签
			- `labelname:nth-child(nth){attrname:attrvalue}`选中同级别的第nth个标签
			- `labelname:nth-last-child(nth){attrname:attrvalue}`选中同级别倒数的第nth个标签
			- `labelname:only-child{attrname:attrvalue}`选中父元素中唯一的元素
			- `lablename:nth-child(odd){attrname:attrvalue}`选中同级别中所有的奇数标签
			- `lablename:nth-child(even){attrname:attrvalue}`选中同级别中所有的偶数标签
			- `labelname:nth-child(xn+y){attrname:attrvalue}`选中同级别中所有的用户自定义的顺序标签,其中x为系数，n为同级别标签个数从0开始递增，y为加数
			- 注意点：
				- 同一级别的不区分类型
		- 同类型的第几个
			- `labelname:first-of-type{attrname:attrvalue}`选中同级别的同类型的第一个标签
			- `labelname:last-of-type{attrname:attrvalue}`选中同级别的同类型的最后一个标签
			- `labelname:nth-of-type(nth){attrname:attrvalue}`选中同类型的第nth个标签
			- `labelname:nth-last-of-type(nth){attrname:attrvalue}`选中同类型的倒数第nth个标签
			- `labelname:only-of-type{attrname:attrvalue}`选中父元素中唯一类型的某个元素
			- `labelname:nth-of-type(odd){attrname:attrvalue}`选中同类型中所有的奇数标签
			- `labelname:nth-of-type(even){attrname:attrvalue}`选中同类型的所有偶数标签
			- `labelname:nth-of-type(xn+y){attrname:attrvalue}`选中同类型的用户自定义的顺序标签，其中x为系数，n为同类型标签个数从0开始递增，y为加数
	- 序选择器应用场景为不方便设置id和类名的时候使用,或者要从一堆标签中筛选出某类标签时使用，某些标签时使用。
	- 属性选择器
		- 什么是属性选择器
			- 根据指定的属性名称，找到对应的标签然后设置属性
		- 格式：`labelname[id]{attrname:attrvalue}`另一种是`labelname[attrname=somevalue]{attrname:attrvalue}`
		- 属性的取值是以什么开头的
			- `labelname[attrname|=value]{attrname:attrvalue}->CSS2` 
			- `labelname[attrname^=value]{attrname:attrvalue}->CSS3`
			- CSS2的只能找到value开头，并且value是被`-`短横和其它内容间隔开的
			- CSS3中的只要是以value来头的都可以被找到，无论有没有被间隔开
		- 属性的取值是以什么结尾的
			- `labelname[attrname$=value]{attrname:attrvalue}->CSS3`
		- 属性的取值是否包含某个特定的值
			- `labelname[attrname~=value]{attrname:attrvalue}->CSS2`
			- `labelname[attrname*=value]{attrnameLattrvalue}->CSS3`
			- CSS2只能找到被空格间隔开来的，只能找到独立的单词
			- CSS3只要包含value都能被找到
	- 通配符选择器
		- 格式：`*{attrname:attvalue}`
		- 给当前页面所有的元素设置属性
		- 注意点：
			- 由于通配符选择器是设置界面上所有元素，会遍历所有标签，性能较差一般不使用

## CSS三大特性
- 继承性
	- 什么是继承性
		- 给父元素设置一些属性，子元素也可以使用。这个就称为继承性.
		- 注意点：
			- 并不是所有的属性都可以继承，只有以color/font/line开头的属性才可以继承。
			- 在CSS继承中，不只是儿子才可以继承，只要是后代都可以继承。
			- CSS继承性中的特殊性
				- a 标签的文字颜色和下划线是不能继承的
				- h 标签的文字大小是不能继承的
		- 应用场景
			- 一般用于设置网页上的共性信息，例如网页的文字颜色字体大小。
- 层叠性
	- 什么是层叠性
		- 层叠性就是CSS处理冲突的能力，当多个选择器给同一个标签设置相同的属性值时，以最后一个设置的属性值为准。
- 优先级
	- 当多个选择器选中同一个标签。并且给同一个标签设置相同的属性时，如何层叠由优先级来确定。
	- 优先级判断的三种方式：
		- 是否是直接选中(间接选中就是继承)，如果是间接选中，那么就是谁离选中的标签近就以谁设置的属性为准
		- 是否是相同的选择器，如果是都是直接选中，并且都是同类型的选择器，谁写在后面就以谁设置的属性为准
		- 不同选择器，如果不是直接选中，并且不是相同类型的选择器，那么就会按照选择器的优先级来层叠样式。
		- 选择器优先级:
			- `id>类>通配符>继承>浏览器默认`