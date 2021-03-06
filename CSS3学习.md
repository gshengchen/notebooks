# 1.级联样式单与CSS选择器

Cascading Style Sheet（级联样式单），缩写CSS，也称层叠样式单。主要用于网页风格设计，包括字体大小、颜色，以及元素的精准定位等。

## 1.1 样式单概述

样式单是一种专门描述结构文档表现方式的文档,包括描述在屏幕上显示效果、打印效果、声音效果等。一般不包括在结构文档内部。它的优点如下：

1. 表达效果丰富；
2. 文档体积小；
3. 便于信息检索；
4. 可读性好。  

样式单推荐标准：CSS、XSL。

### 1.1.1 CSS概述

级联式单是一系列格式规则，用于控制网页内容外观，主要提供如下内容：

- 页面字体、颜色控制更加细腻，更富表现力；
- 控制整站风格。  

### 1.1.2 CSS发展史

CSS最新版本是CSS3,2010年规范推出。

## 1.2 CSS样式单的基本使用

在HTML中使用CSS样式单，有如下4种规则：

1. 链接外部样式文件；
2. 导入外部样式文件；
3. 使用内部样式定义；
4. 使用内联样式.

CSS样式单有一个或几个样式组成，语法如下：

```html
选择器 {property: value}；
```

### 1.2.1 链接外部样式文件

HTML文档中使用link元素来链接外部样式文件，语法如下：

```html
<link type="text/css" rel="stylesheet" href="CSS外部样式文件URL">
```

### 1.2.2 导入外部样式单

语法如下：

```html
@import url("样式单文件") sMedia;
```  

语法格式中url可省略。sMedia是指定仅对某种显示设备有效。
应该尽量避免使用这种模式。

### 1.2.3 使用内部样式

使用内部样式的规则:只针对某个页面有效,不影响整个网站。
语法规则如下：

```html
<style type="text/css">
  样式定义
</style>
```

### 1.2.4 使用内联模式

内联CSS对标签有效，可以精确某个元素的外观表现，并且可以通过javascript动态修改元素的css样式。语法如下：

```html
style ="property1:value;property2:value;"
```  

## 1.3 CSS选择器

选择器有多种定义方法。

### 1.3.1 元素选择器

元素选择器是最简单的选择器，其语法如下：

```html

E {....} //E就是代表有效的元素标签。
```  

### 1.3.2 属性选择器

元素选择器是属性选择器的特例，属性选择器有以下几种语法格式：

- E{...}:定义的CSS对所有E元素起作用；
- E[attr]{...}:定义的CSS对包含属性attr的E元素起作用；
- E[attr=value]{...}:定义的CSS对包含属性attr,且属性值为value的E元素起作用；
- E[attr~=value]{...}:定义的CSS对包含属性attr,且属性值空格隔开的系列值，其中某个值为value的E元素起作用；
- E[attr|=value]{...}:定义的CSS对包含属性attr,且属性值连字符隔开的系列值，其中第一个值为value的E元素起作用；
- E[attr^=value]{...}:定义的CSS对包含属性attr,且属性值以value字符串开头的E元素起作用；
- E[attr$=value]{...}:定义的CSS对包含属性attr,且属性值以value字符串结尾的E元素起作用；
- E[attr*=value]{...}:定义的CSS对包含属性attr,且属性值包含value字符串的E元素起作用。  

除了第一种方式，其他并没有得到所有浏览器支持，最后三种是CSS 3.0新增的选择器。

### 1.3.3 ID选择器

id选择器语法：

- #idValue{...}:定义的CSS对具有指定id属性值的元素起作用；
- E#idValue{...}:对指定E元素起作用的id选择器。  

### 1.3.4 Class 选择器

语法结构：
[E].classValue{...}:定义的CSS对具有class属性值的元素起作用，E元素可省略。

### 1.3.5 包含选择器

语法结构：
selector1 selector2 {...}:selector2 必须包含在selector1对应元素的内部。

### 1.3.6 子选择器

语法结构：
selector1>selector2 {...}:目标选择器是selector1对应元素的子元素；与包含选择器有点相似，但他只能是子元素。

### 1.3.7 CSS3新增的兄弟选择器

语法结构:
selector1 ~ selector2:与selector1对应的元素后面，能匹配selector2的兄弟节点。

### 1.3.8 组合选择器

语法结构：
selector1，selector2，... {...}：定义的css对所有的选择器都有效。

## 1.4 伪元素选择器

伪元素选择器并不是针对真正的元素使用选择器，而是对CSS中已有的伪元素起作用：

- :first-letter:对象的第一个字符，对块元素起作用；
- :first-line:对象的第一行，对块元素起作用；
- :before/:after:在对象的前/后插入内容。
