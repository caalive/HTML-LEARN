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
	

