# 1.HTML 5历史
## 1.1 HTML历史与HTML 5
### 1.1.1 HTML发展史
HTML开始，他显得不正规，没有执行严格规范，对他的错误都极其宽容。
```html
<ol>
  <li>a
  <li>bh
</ol>
```  
这段代码在任何浏览器都显示有序列表。
### 1.1.2 HTML 4.01和XHTML
它们具有很好的兼容性，而且XHTML是更严格、更纯净的html代码,他有4条基本规则：
- 整个文档只有一个根元素；
- 除空元素外，每个元素都有开始与结束标签；
- 元素与元素之间要合理嵌套；
- 元素的属性必须有带引号的属性值。  

### 1.1.3 HTML 4.01和XHTML规范
HTML 4.01和XHTML语法规范基本相似，不过XHTML所有标签与属性都必须是小写，但很少页面完全遵守HTML 4.01和XHTML规范，这就制定新的html标准，即html 5。
### 1.1.4 从XHTML到HTML 5
html页面大量存在以下4种不规范的内容：
- 元素标签大小写混写；
- 元素没有合理结束标签；
- 元素中使用属性，却没有指定属性值；
- 元素属性值没有使用引号。  

而html5 承认他们是合法的，所以html 5 是对现实的妥协。
## 1.2 HTML 5的优势
### 1.2.1 解决垮浏览器问题
html 5出现，各个浏览器厂商积极支持，以后前端程序开发将变得更加轻松。
### 1.2.2 部分代替Javascript
通过为标签提供一些属性值增加一些实用功能，可以代替javascript。
### 1.2.3 更明确的语义支持
HTML 5以前，只能通过div标签表达文档结构，现在为页面布局提供更明确的语义元素。
```html
<header>....</header>
<nav>....</nav>
<article>
<section>
....
</section>
</article>
<aside>....</aside>
<footer>....</footer>
```
以前html只能通过em元素表达被强调的内容，但现在提供了更多语义的强调元素，如：time，mark。
### 1.2.4 增强了web程序的功能
html 5以前对Web程序而言，功能太单薄，而新规范增加了不少新的API，开发Web程序将会更加轻松。
## 1.3 HTML 5的基本结构与语法变化
HTML 5遵从以下3个规则：
- 兼容性：在老版本浏览器上能够运行；
- 实用性：封装简单功能；
- 非革命性发展。  

### 1.3.1 HTML 5结构
HTML 5的DTD定义非常简单：
```html
<!DOCTYPE html>
```
文档的根元素html，html只能包含head和body两个子元素。
元素=开始标签+内容+结束标签。
### 1.3.2 HTML 5的语法变化
- 标签不在区分大小写，下面是符合html 5规范；
```html
<p>chen</P>
```
- 元素可以省略标签
 1. 空元素标签：area、base、br、col、command、embed、hr、img、input、keygen、link、meta、param、source、wbr。
 2. 可以省略结束标签的元素：colgroup，dt，dd，li，optgroup，option，p，rt，rp，thead，tbody，tfoot，tr，td，th。
 3. 可以省略全部标签的元素：html、head、body、tbody。
- 允许省略属性值的属性：checked、readonly、disabled、selected、defer、ismap、nohref、noshade、nowrap、multiple、noresize。以下两个代码是一样的
```html
<input checked type="checkbox">
<input readonly type="text">
```
```html
<input checked="checked" type="checkbox">
<input readonly="readonly" type="text">
```
- 允许属性值不使用引号，如果属性值有空格等使浏览器混淆的，应该使用引号。  
# 2.html5 的常用元素与属性
## 2.1 HTML 5保留的常用元素
### 2.1.1 基本标签  

|标签|解释|标签|解释|  
|----------|--------|-----|-------|  
|<!-- --\>| html注释|html|文档根元素|
|head|定义文档的头，可省略|tilte|定义页面标题|
|body|页面主体|style|引入样式定义|
|h1--h6|定义标题1到标题6|p|定义段落|
|br|换行|hr|水平线|
|div|定义节，是块元素|span|是行内元素|  
### 2.1.2 文本格式化标签  

|标签|解释|标签|解释|  
|----------|-------|-----|-------|
|b|粗体文本|i|斜体文本
|em|强调文本，与斜体文本差不多|strong|同b,html5增强语义表示重要性|
|small|小号字体|sup|上标|
|sub|下标|bdo|文字方向，属性dir值只能是ltr、rtl|  
文本格式化标签能包含文本、图像、超链接等其他元素，是行内元素。
### 2.1.3 语义相关标签  

|标签|解释|标签|解释|  
|----------|-------|-----|-------|
|abbr|表示一个缩写，title属性表示全称|address|表示地址|
|blockquote|引用一个长的文本，块元素,cite属性指定所引用URL|q|定义短的引用文本，行内元素，浏览器一般加引号|
|cite|表示作品的标题 显示为斜体|code|表示计算机代码|
|dfn|定义专业术语，用粗体或斜体表示|del/ins|被删除/插入的文本，以中/下画线表示，cite属性指向原因URL，datetime属性是发生的时间|
|pre|表示代码，但空格、TAB、回车和其他格式字符保留下来，但 HTML 大部分元素被浏览器处理|samp|定义范本内容|
|kbd|键盘文本，表示该文本通过键盘输入|var|变量，用斜体显示|  
### 2.1.4 超链接与锚点
定义超链接a标签，它除了可以指定id、class、style、title等通用属性外，它有三个重要属性：
- href:指定超链接所关联的另一个资源；
- target：指定使用框架集中哪个框架转载另一个资源，属性值有:\_self、\_blank、\_top、\_parent。
- media：指定目标URL所引用的媒体类型。  

标签可以包含文本、图像、各种文本格式化元素和表单元素等内容。
一个完整的网址遵守以下的词法规则：scheme://host.domain:port/path/filename。
scheme有：file、ftp、http、news、telnet、gopher、mailto等。
html5以前插入锚点需要a标签，并指定name属性，html 每个标签id属性都可以做锚点，使用a标签href属性用“#锚点名”来定位锚点。
### 2.1.5 列表相关标签
- ul：定义无序列表，该元素只能包括li子元素。
- ol：定义有序列表，该元素只能包括li子元素。有三个属性：start、type、reversed。
- li：定义列表项，可以包括较多类型的子元素。
- dl：定义列表，该元素只能包括dt、dd。
- dt：定义标题列表项。
- dd：定义普通列表项。  

### 2.1.6 图像相关标签
定义图像的标签是img，该元素是一个空元素。它除了通用属性外，必须指定如下两个属性：
- src：指定图片文件的位置；
- alt：属性值是一段文本，作为该图片的提示信息。  

除此之外，还有两个可选属性：
- width：图像宽度；
- height：图像高度 。  

map标签定义图片映射，该元素包含一个或多个area标签，每个area标签定义一个区域，不同区域可链接到不同的URL。
area是一个空元素，除了有通用属性外，孩可以指定如下几个属性：
- shape：区域形状，默认rect，还可以是circle、ploy。
- coords：多个坐标。
- href：URL。
- alt：为图片提供信息。
还有alt、target、media等与a标签相同。  

如果使用map元素定义图片映射后，就需要用img标签指定图片使用该图片映射，通过指定img标签usemap属性值为#mapname即可。
### 2.1.7 表格相关元素
HTML5定义表格的如下标签：
- table：定义表格。该标签只能包括0或1个caption、thead、tfoot,多个tr和tbody。特有的属性有：
  1. cellpadding:单元格与边框之间的距离，属性值可以是百分比或像素。
  2. cellspacing:单元格之间的间距。
  3. width：表格宽度。  
- caption：定义表格标题。
- tr:定义表格行，该标签包含th、td标签。
- td：定义单元格，能包含各种标签包括table，它有几个重要属性：
  1. colspan：该单元格跨几列；
  2. rowspan：该单元格跨几行；
  3. width：单元格宽度。
- th：定义表格页面的单元格，同td，只是浏览器呈现不同。
- tbody：定义表格主体，该标签只能包括tr，作用是将表格分成几个部分。
- thead/tfoot:定义表格头与脚，用法同tbody，使用它们可以让表格头与页脚之间内容进行滚动，而且打印时每页都有标题与页脚。
- col:该元素用于为表格一个或多个列指定属性值，该元素只能出现在table、colgroup中，其中span属性，指定它能跨多少列。
- colgroup：该元素用于为表格一个或多个列指定属性值，该元素只能出现在table、colgroup中。它的作用只是组织多个col元素。  

### 2.1.8 框架元素
HTML 5只保留iframe标签，他在普通html页面生成内联框架，src属性指定URL。
## 2.2 HTML通用属性
HTML通用属性，及全局属性适应任何html标签：  

|属性|描述|属性|描述|
|----|---|---|---|
|accesskey|规定激活元素的快捷键|class|规定元素的1个或多个类名|
|contentEditable|规定元素内容是否可编辑|contextmenu|规定元素的上下文菜单|
|data-*|用于存储页面或应用程序的私有定制数据|dir|规定元素内容的文本方向|
|draggable|规定元素是否可拖动|dropzone|规定在拖动数据是是否进行复制、移动或链接|
|hidden|元素是否隐藏|id|元素唯一id|
|lang|元素语言|spellcheck|是否进行拼写和语法检查|
|style|元素行内样式|tabindex|规定元素的tab键次序|
|title|规定元素的额外信息|translate|规定是否应翻译元素内容|  

### 2.2.1 contentEditable属性
HTML5新增加的属性，如果属性值为true，允许直接编辑html元素里内容。它具有可继承的特点。
### 2.2.2 designMode属性
该属性相当于全局的contentEditable属性。属性值on、off，只能在文档中定义。
### 2.2.3 hidden属性
hidden属性值为true，浏览器不显示该组件。
### 2.2.4 spellcheck属性
该属性支持ture、false两个值
## 2.3 HTML5新增标签
### 2.3.1 文档结构元素
HTML5新提供article、section、nav、aside、header、footer等文档结构标签。与div区别：div是一个通用的容器组件，而它们是语义明确的组件。
* article:用于代表页面上独立、完整的“文章”，使用规则：
  1. 内部使用header定义文章标题；
  2. 使用footer定义文章脚注；
  3. 使用section定义文章段落；
  4. 可嵌套article作为它附属文章。
* section:该元素对页面内容进行分块，可指定cite属性，简单规则如下：
  1. 通常建议包含一个标题（h1~h6）；
  2. 包含article，表示分块内部包含多篇文章；
  3. 可以嵌套section。
* nav：定义页面导航条。
* aside：定义当前页面或文章的附属信息，通常用css。
* header：主要用于article元素中定义文章头部信息。
* hgroup：当header元素中有多个h1~h6标题时，可以用该元素组织。
* footer：主要用于article元素中定义脚注部分，包括作者信息、作者版权等。
* figure：表示一组图片信息。
* figcaption：在figure中，定义图片区域的标题。  

### 2.3.2 HTML5新增的语义标签
- mark：显示页面重点关注的内容，一般显示成黄色。
- time：用来显示被标注的内容是日期时间，其属性datatime只是用来向机器提供时间，格式yyyy-mm-ddTHH:MM。
- details和summary：details显示详细信息，summary显示摘要。摘要信息默认可见，点击显示details内容。  

### 2.3.3 两个特殊功能的元素
- meter:用于一个已知最大值和最小值的计数仪表，除通用属性，还有以下属性：
  1. value：计数仪表的当前值。
  2. min、max：最小值、最大值
  3. low、high 指定范围最小值与最大值；
  4. optimum:有效范围最佳值。
- progress：表示一个进度条，max：进度完成时的值，value：当前完成的值。  

### 2.4 HTML5头部与元信息
head定义文档头，它可以包括以下子元素：
- script：该元素包含javascript脚本。
- style：该元素用于定义内部CSS样式。
- link：该元素用于链接外部css样式。
- title：定义文档标题。
- base:用于指定该页面中所有链接的基准链接：
  1. href属性是指所有链接的基准链接；
  2. target属性指定在哪个窗口打开链接。
- meta：定义页面的元信息，除了id属性外，还可以指定如下属性：
  1. http-equivbb属性值主要有：Expires（网页过期时间）、Pragma（无法脱机浏览）、Refresh（刷新时间）、Set-Cookie（网页过期cookie删除）、content-Type（内容类型）。
   ```html
  <meta http-equiv="Expires" content="sat....">
  <meta http-equiv="Pragma" content="no-cache">
  <meta http-equiv="Refresh" content="2">
  <meta http-equiv="Set-Cookie" content="">
  <meta http-equiv="content-Type" content="text/html;charset=uft-8">
  ```
  2. name 指定元信息名称。
  ```html
  <meta name="keywords" content="chen ">
  ```
  3. content元信息的值。  

## 2.5 HTML 5新增拖放API
html5新增拖放API，可以让任何html元素变成可拖动的。
### 2.5.1 启动拖动
img、a（指定href、src）等元素默认是可拖动的，对于其他普通元素，设置draggable属性为true即可。为了让拖动操作能携带数据，应该为被拖动的意思ondragstart事件指定监听器。同时，要让操作可以携带数据。
```html
source.ondragstart=function(evt){
  evt.dataTransfer.setData("text/plain","www.fkjava.org");
}
```
### 2.5.2 接受放
当被拖动的元素经过拖过document对象时，document对象默认是阻止了拖动事件。为了让document可以接受放，应该为document的ondragover事件指定监听器，在其中取消document对拖动事件的默认行为。
```html
document.ondragover=function(evt){
  return false;
}
```
不同浏览器对拖放操作的默认动作并不相同，所以为document的ondrop事件绑定监听器：
```html
document.ondrop=function(evt){
  return false;
}
```
拖放事件，可能触发事件如下：   

|事件|事件源|描述|
|---|-----|-----|
|ondragstart|被拖动的HTML元素|开始拖动时触发事件|
|ondrag|被拖动的HTML元素|拖动过程中不断触发事件|
|ondragend|被拖动的HTML元素|拖动结束时触发事件|
|ondragenter|拖动时鼠标经过的HTML元素|被拖动的元素进入本元素范围时触发事件|
|ondragover|拖动时鼠标经过的HTML元素|被拖动的元素进入本元素范围时不断触发事件|
|ondragleave|拖动时鼠标经过的HTML元素|被拖动的元素离开本元素范围时触发事件|
|ondrop|拖动时鼠标经过的HTML元素|其他元素放入本元素中时触发事件|  
### 2.5.3 DataTransfer对象
拖放触发的拖放事件有一个dataTransfer属性，该属性值就是一个DataTransfer对象，该对象包含以下属性与方法：
- dataTransfer.dropEffect:设置或返回拖放目标上允许发生的拖放行为，属性值：none、copy、link和move。
- dataTransfer.effectAllowed:设置或返回被拖元素允许黄色的拖动行为，属性值：none、copy、copylink、link、linkmove、move。
- dataTransfer.items:返回DataTransferItems对象，该对象代表了拖动数据。
- dataTransfer.setDragImage(element,x,y):设置拖放操作的自定义图标。
- dataTransfer.addElement(element):添加自定义图标。
- dataTransfer.types:返回一个DOMStringList对象。该对象包括了存入dataTransfer中数据的所有类型。
- dataTransfer.getDate(format):获得对象中format格式的数据。
- dataTransfer.setData(format,data):向DataTransfer对象中存入格式为format，数据data。
- dataTransfer.clearData（[format]):清除数据。  

# 3.HTML5 表单相关元素与属性
## 3.1 HTML原有的表单及表单控件
### 3.1.1 表单元素
form元素用于生成输入表单，但不会生成可视化部分。form除了通用属性与事件外还可以指定如下属性：
- action：当单击表单内的确认按钮时，该表单被提交到该属性值的地址。
- method：提交类型，该属性值是post或get，即发出POST或GET类型请求。
  1. GET方式的请求：表单默认以GET方式发送请求，它会将请求参数的名字与值转换成字符串附加在原URL后，该方式传送的数据较小。超级链接也是这种请求方式。
  2. POST方式的请求：发出请求参数以及对应的值放在HTML HEADER中传输，数据量大，安全性高。
- enctype：对表单内容进行编码所使用的字符集。该属性值有三种：
  1. application/x-www-form-urlencoded:默认的编码方式，以URL编码方式。
  2. multipart/form-data:以二进制流方式编码，主要用于上传文件。
  3. text/plain：action的属性值是mailto：URL时，使用他比较方便。
- name：指定表单的唯一名称，建议与id值保持一致。
- target：指定使用哪种方式打开目标URL。  

表单控件转换成请求参数的规则如下：
- 每个有name属性的表单控件对应一个请求参数，没有name属性不能生成表单参数。
- 如果多个控件具有相同name属性，则多个表单控件只生产一个请求参数，该参数有多个值。
- name属性是参数名，value是参数的值。
- 如果某个表单控件设置disabled或disabled=“disabled”，该控件不再生成参数。  

### 3.1.2 使用input元素
- 单行文本框：设置type="text"；
- 密码输入框：设置type=“password”;
- 单选框：设置type="radio";
- 隐藏域：设置type="hidden"，用于提供额外请求参数，不需要输入，所以要通过value的值；
- 复选框：设置type="checkbox";
- 图像域：设置type="image"，与提交按钮一样，单击提交表单。
- 文件上传域：设置type="file";
- 提交、重置、无动作按钮，type对应的属性值是：submit、reset、button。  
input的属性：
- checked：设置单选框与复选框的初始状态是否被选中。
- disable：设置禁用该元素，type=“hidden” 不能设置该属性。
- maxlength：指定文本框最大字符数。
- readonly：不允许用户修改。
- size：指定该元素的宽度。，type=“hidden” 不能设置该属性。
- src、width、height：只有type="image"时有用。  

### 3.1.3 使用label标签
在表单中定义标签，点击标签可以使其关联的表单控件自动获取焦点，让标签与表单关联有两种方法：
- 隐式使用for属性：指定for属性值为关联表单控件的id值。
- 显示关联：将表单控件放在label内,尽量少用，有的浏览器不支持。  

### 3.1.4 button定义按钮
button定义按钮可以包含普通文本、文本格式化标签、图像等，比&lt;input type="button"&gt;功能更加强大。它有以下属性：
- disable：是否禁用；
- name：按钮唯一名称，应该与id属性值保持一致；
- type：它的值只能是submit、reset或nutton；
- value：初始值。  

### 3.1.5 列表框与下来菜单
select用于创建列表框或下拉菜单，该元素必须和option元素结合使用，每个option元素代表一个列表项或菜单项。select的属性：
- disable：禁用标签；
- multiple：设置是否多选；
- size：可以同时显示多少项，select是列表框还是下拉菜单由multiple或size决定，只要有这两种属性之一，就是列表框。  

select只能包含下面两种子元素：
- option：用于定义列表框选项或菜单项，该元素只能包含文本；
- optgroup：定义组。子元素只能是option。label属性指定选项组的标签，必填。  

option元素的属性有：
- disable：禁用；
- selected：指定初始状态是否被选定。
- value：请求参数。  

### 3.1.6 textarea定义文本域
textarea定义多行文本，主要属性有cols、rows、readonly。name是参数名，不能指定value属性。
## 3.2 HTML5 表单新增的属性与元素
### 3.2.1 HTML5为表单控件新增属性
- form属性：属性值为所属表单id,通过为表单控件定义form属性，可以让表单控件定义在form元素之外，这样为页面布局提供更大灵活性。
- formxxx：属性formaction、formenctype、formmethod、formtarget 对&lt;input type="submit"&gt;和&lt;button&gt;等按钮，可以改变enctype、action、method、target的值。
- autofocus：自动获得焦点，只能一个控件可设置此属性。
- placeholder：input属性，该属性值就是单行文本框和多行文本框的提示信息。
- list:input属性值，相当于文本框与下拉菜单组合，该属性值是datalist的id，datalist相当于看不见的select，所包含的子元素与select完全相同。
- autocomplete:input属性，属性值on、off。大多数浏览器不支持。  

### 3.2.2 功能丰富的input元素
HTML5中input属性type新增很多功能：
- color：颜色选择器；
- date：日期选择器；
- time：时间选择器；
- datetime：UTC日期时间选择器；
- datetime-local：本地日期时间选择器；
- week：周选择器；
- month：月份选择器；
- email：E-mail输入框；
- tel：电话输入框；
- url：url输入框；
- number：数字框；
- range：拖动条，有三个属性：min、max、step；
- search：搜索框。  
### 3.2.3 output控件
该元素用于显示输出，for属性的值是要显示控件的id。onforminput属性是事件监听器属性，当如何表单控件有输出是触发该事件（好像已失效，解决方法在form标签中增加oninput属性。）。
## 3.3 HTML5增加的文件上传
HTML5以前文件上传有很大局限：不支持多文件上传；只上传文件路径，不能访问实际文件。
### 3.3.1 FileList对象与File对象
HTML5为type=“file”的input元素增加两个属性：
- accept：该属性值为一个或多个MIME类型的字符串，控制上传文件的类型。
- multipe：该属性允许选择多个文件。  

&lt;input type="file"&gt;的files属性返回FileList对象，相当一个数组，数组元素就是javascript的File对象。File对象包含如下常用属性：
- name：文件名，不包含路径。
- type：返回File对象对应的文件的MIME类型字符串。
- size：文件大小。  

### 3.3.2 使用FileReader读取文件内容
FileReader是一个javascript对象，开发者可以通过该对象在客户端读取文件上传域所选择的文件内容。
- readAsText(file,encoding):以文本方式读取该文件，其中encoding是文件的字符集，参数默认值utf-8。
- readAsBinaryString(file):以二进制方式读取文件。
- readAsDataURL(file):以DataURL方式读取文件。
- abort（）：停止读取。
- onloadstart：FileReader开始读取数据时触发该事件指定的函数。
- onprogress：FileReader正在读取数据时触发该事件指定的函数。
- onload：FileReader成功读取数据时触发该事件指定的函数。
- onloadend：FileReade结束读取数据时触发该事件指定的函数，不管有没有成功。
- onerror:FileReader开始读取数据失败时触发该事件指定的函数。  

## 3.4 HTML5新增的客户端校验
HTML5为表单控件新增了输入校验属性。
### 3.4.1 使用校验属性进行校验
- required：该属性指定表单控件必须输入。
- pattern：该属性指定该表单控件的值必须符合指定的正则表达式。
- min、max和step：对数字、日期的&lt;input&gt;元素有效。  

### 3.4.2 调用checkValidity方法进行校验
使用通过校验属性进行校验，比较简单，可以使用html5提供的表单、表单控件的checkValidity（）方法进行校验。
- 如果表单对象调用checkValidity（）方法返回true，则表明所有表单控件通过校验。
- validity：该属性的值是一个ValidityState对象，其中vaild属性值可以表示是否通过校验。  

### 3.4.3 自定义错误提示
HTML5 为每个校验规则提供相应的错误提示，如果定制自己的错误提示信息，需要setCustomValidity（）方法。
### 关闭校验
关闭校验使用novalidate属性或使用formnovalidate属性。
# 4.HTML5的绘图支持
HTML5新增canvas元素，通过该元素获得CanvasRenderingContext2D对象，该对象是一个强大的绘图API。
## 4.1 使用canvas元素
canvas元素相当于画布，是一个绘制图形的容器，必须通过javascript脚本来绘制图形。canvas除了通用属性外，可以指定如下两个属性：
- height：画布高；
-width：画布宽。  

为了向画布绘制图形必须经过如下3步：
1. 获取canvas元素的DOM对象；
```html
document.getElementById("canvasId");
```
2. 调用canvas对象的getContext（）方法，返回CanvasRenderingContext2D对象；
3. 调用CanvasRenderingContext2D对象的方法绘图。   

## 4.2 绘图
- 颜色、样式和阴影  

|属性|描述|
|--|--|
|fillStyle|设置或返回用于填充绘画的颜色、渐变(gradient对象)或模式（pattern）|
|strokeStyle|设置或返回用于笔触的颜色、渐变或模式|
|shadowColor|设置或返回用于阴影的颜色|
|shadowBlur|设置或返回用于阴影的模糊级别|
|shadowOffsetX|设置或返回阴影距形状的水平距离|
|shadowOffsetY|设置或返回阴影距形状的垂直距离|  

|方法|描述|
|--|--|
|createLinearGradient(x0,y0,x1,y1)|创建线性渐变（用在画布内容上）两点坐标(x0,y0)(x1,y1)|
|createPattern(image,"repeat/repeat-x/repeat-y/no-repeat")|在指定的方向上重复指定的元素|
|createRadialGradient(x0,y0,r0,x1,y1,r1)|创建放射状/环形的渐变（用在画布内容上）|
|addColorStop(stop,color)|规定渐变对象中的颜色和停止位置,stop介于 0.0 与 1.0 之间的值，表示渐变中开始与结束之间的位置。|  
- 线条样式   

|属性|描述|
|--|--|
|lineCap|设置或返回线条的结束端点样式,属性值：butt（平直）、round、square|
|lineJoin|设置或返回两条线相交时，所创建的拐角类型：bevel（斜角）、round（圆角）、miter（默认尖角）|
|lineWidth|设置或返回当前的线条宽度|
|miterLimit|设置或返回最大斜接长度|
- 矩形  

|方法|描述|
|--|--|
|rect(x,y,width,height)|向当前路径上创建矩形|
|fillRect(x,y,width,height)|绘制“被填充”的矩形|
|strokeRect(x,y,width,height)|绘制矩形（无填充）|
|clearRect(x,y,width,height)|在给定的矩形内清除指定的像素|
- 路径  

|方法|描述|
|--|--|
|fill()|填充当前绘图（路径）|
|stroke()|绘制已定义的路径|
|beginPath()|起始一条路径，或重置当前路径|
|moveTo(x,y)|把路径移动到画布中的指定点，不创建线条|
|closePath()|创建从当前点回到起始点的路径|
|lineTo(x,y)|添加一个新点，然后在画布中创建从该点到最后指定点的线条|
|clip()|从原始画布剪切任意形状和尺寸的区域|
|quadraticCurveTo(cpx,cpy,x,y)|创建二次贝塞尔曲线，程序，控制点cx,cy，结束点新，y|
|bezierCurveTo(cp1x,cp1y,cp2x,cp2y,x,y)|创建三次方贝塞尔曲线,控制点cx1,cy2,cx2,cy2，结束点x，y|
|arc(x,y,r,sAngle,eAngle,el)|创建弧/曲线（用于创建圆形或部分圆）,x,y,圆心，el顺时针逆时针|
|arcTo(x1,y1,x2,y2,r)|创建两切线之间的弧/曲线，参数：起始、结束、半径|
|isPointInPath()|如果指定的点位于当前路径中，则返回 true，否则返回 false|
- 转换  

|方法|描述|
|--|--|
|scale(scalewidth,scaleheight)|	缩放当前绘图至更大或更小
|rotate(angle)|以弧度旋转当前绘图|
|translate(x,y)|重新映射画布上的 (0,0) 位置|
|transform(a,b,c,d,e,f)|替换绘图的当前转换矩阵|
|setTransform(a,b,c,d,e,f)|将当前转换重置为单位矩阵。然后运行 transform()|
- 文本   

|属性|描述|
|--|--|
|font|设置或返回文本内容的当前字体属性|
|textAlign|设置或返回文本内容的当前对齐方式，属性：center、end、left、right、start|
|textBaseline|设置或返回在绘制文本时使用的当前文本基线，属性alphabetic、top、hanging、middle、ideographic、bottom|

|方法|描述|
|--|--|
|fillText(text,x,y,maxWidth)|在画布上绘制“被填充的”文本|
|strokeText(text,x,y,maxWidth)|在画布上绘制文本（无填充）|
|measureText(text)|返回包含指定文本宽度的对象|
- 图像绘制  

|方法	|描述|
|--|--|
|drawImage(img,sx,sy,swidth,sheight,x,y,width,height)|向画布上绘制图像、画布或视频|  
- 像素操作  

|属性|描述|
|--|--|
|width|返回 ImageData 对象的宽度|
|height	|返回 ImageData 对象的高度|
|data|返回一个对象，其包含指定的 ImageData 对象的图像数据|

|方法|描述|
|--|--|
|createImageData(width,height)|创建新的、空白的 ImageData 对象|
|getImageData(x,y,width,height)|返回 ImageData 对象，该对象为画布上指定的矩形复制像素数据|
|putImageData(imgData,x,y,dirtyX,dirtyY,dirtyWidth,dirtyHeight)|把图像数据（从指定的 ImageData 对象）放回画布上|
- 合成  

|属性|描述|
|--|--|
|globalAlpha|设置或返回绘图的当前 alpha 或透明值，必须介于 0.0（完全透明） 与 1.0（不透明） 之间。|
|globalCompositeOperation|设置或返回新图像如何绘制到已有的图像上|

### 4.2.2 绘制几何图形
CanvasRenderingContext2D提供了两种方法绘制几何图形：
- fillRect(float x,float y, float height,float width):填充矩形区域；
- strokeRect(float x,float y, float height,float width):绘制矩形边框。  

### 4.2.3 绘制字符串
- fillText(String text,float x ,float y,[float maxWidth]):填充字符串
- stokeText(String text,float x ,float y,[float maxWidth]):绘制字符串边框。
- textAlign：设置对齐方法，属性值:center、end、left、right、start
- textBaseline:设置或返回在绘制文本时使用的当前文本基线，属性alphabetic、top、hanging、middle、ideographic、bottom。
### 设置阴影
- shadowBlur:设置阴影的模糊度，浮点数越大，模糊程度越高。
- shadiwColor：设置阴影的颜色。
- shadowOffsetX、shadowOffsetY：x，y方向偏移。  

### 使用路径
CanvasRenderingContext2D的对象只提供了两种绘制矩形的方法，绘制更复杂的图形就要使用路径，可以按照以下步骤进行：
- 调用beginPath()开始定义路径；
- 使用各种方法添加子路径；
- 调用closePath()方法关闭路径；
- 调用fill()或stroke()来填充或绘制路径的边框。   

CanvasRenderingContext2D对象提供了如下方法添加路径：
- act（x,y,radius,startAngle,endAngle，counterclockwise）：绘制以x，y为圆心，以radius为半径，从startAngle角度开始，到endAngle角度结束的圆弧，counterclockwise可选，省略或false顺时针。
- actTo(x1,y1,x2,y2,radius):绘制开始点x1,y1到结束点x2,y2,半径为radius的圆弧。
- bezierCurveTo（cpx1,cpy1,cpx2,cpy2,x,y):绘制两个控制点的贝塞尔曲线，结束点位x,y。
- lineTo(x,y):绘制到x,y的直线。
- moveTo（x,y):移动到点x,y。
- quadraticCurveTo(cpx,cpy,x,y):绘制二次曲线。
- rect（x,y,width,height):绘制矩形。   

### 绘制位图
- void drawImage(image,x,y):把image绘制到x,y。
- void drawImage(image,x,y,w,h):把image绘制到x,y 进行缩放。
- void drawImage(image,sx,sy,sw,sh,dx,dy,dw,dh):把image从sx,sy位置高宽sw,sh的图像，放在dx,dy的位置进行缩放。   

创建图像image，用new image（）、new image(w,h),然后，给image的src属性赋予图像地址，这时就要装载图像，这种装载是异步的，为了保证装载完才能绘制图像，要把绘制图像放在onload事件中。
## 4.3 图形特效处理
### 4.3.1 使用坐标变换
- translate(dx,dy):坐标原点平移dx,dy。
- scale(sx,sy):缩放坐标系统，sx、sy是缩放因子。
- rotate(angle):旋转坐标。  

### 4.3.2 坐标变换与路径结合使用
### 4.3.3 使用矩阵变换
transform(m11,m12,m21,m22,dx,dy):m11、m12、m21、m22是矩阵，dx、dy将坐标平移，公式 x=m11*x+y*m21，y=m12*x+y*m22 它可以实现translate、scale、ratote等方法，但比较复杂。
## 4.4 控制风格叠加
- source-over:新绘制的顶层，默认；
- destination-over：新绘制在后面；
- source-in：新与原做in运算，只显示重叠部分；
- destination-in：原与新做in运算，只显示不重叠部分；
- source-out：新与原做out运算，只显示重叠部分；
- destination-out:原与新做out运算，只显示不重叠部分；
- source-atop:只绘制新与旧重叠部分和原绘制图形不重叠部分；
- destination-atop：只绘制重叠部分和新绘制不重叠部分；
- lighter：重叠部分颜色叠加；
- xor：不绘制重叠部分；
- copy：只绘制新图。  

## 4.5 控制填充风格
### 4.5.1 线性渐变
- 调用canvasRenderingContext2D对象的createLinearGradient(x1,y1,x2,y2)方法创建一个线性渐变，该方法返回CanvasGradient对象。
- 调用addColorStop(offset,color)方法添加颜色。
- 将CanvasGradient对象赋值给fillStyle或strokeStyle属性。
### 4.5.2 圆形渐变
createRadialGradient(x1,y1,r1,x2,y2,r2)方法创建圆形渐变。
### 4.5.3 位图填充
createPattern(image,repetitionstyle)方法创建位图填充。
## 4.6 位图处理
### 4.6.1 位图裁剪
- 需要从创建路径；
- 调用clip（）方法；
- 绘制。  

### 4.6.2 像素处理
- getImageData(x,y,w,h):获取x,y点大小为宽高为w,h的图像，返回值为CanvasPixelArray对象，该对象具有width、height、data等属性。data属性是r、b、g、a数组。每4个元素对应1个像素点
- putImageData（CanvasPixelData，x，y）：把数据放入x，y处，该方法会改变canvas图像。
## 4.7 输出位图
toDataURL（str）：canvas的方法，将对应的位图编码成DataURL字符串，str参数是形如image/png的MIME字符串
# 5.HTML 5的多媒体支持
HTML5 新增audio、video两个标签支持多媒体播放。
## 5.1 使用audio、video元素
这两个标签与img类似，区别是它们不是空元素标签，标签之间放置文本内容，不支持标签的显示此内容。它们的属性如下：  

|属性名|描述|
|--|--|
|src|指定源URL地址|
|autoplay|如果指定该属性，会自动播放|
|controls|如果指定该属性，显示控制条|
|loop|如果指定该属性，循环播放|
|preload|auto预加载；metadata，预加载元数据，第一帧；none不预加载|
|poster|对video有效，指定图片URL，在下载完成前显示|
|width、height|video有效，指定宽高|  

考虑各浏览器对音视频支持互不相同，可以增加source子元素指定多个媒体源：src属性是源URL地址，type属性是媒体类型，MIME字符串，如：audio/ogg、audio/mpeg、audio/x-wav。
## 5.2 使用javascript脚本控制媒体播放
### 5.2.1 HTMLAudioElement和HTMLVideoElement支持的方法
Javascript脚本获取audio对应的对象是HTMLAudioElement，video对应的对象是HTMLVideoElement。它们有如下的方法：
- play（）：播放；
- pause(): 暂停；
- load（）：重载；
- canPlayType（type）：判断该元素能否播放type类型的媒体，返回三个值：probably（能)、maybe（可能行）、空字符串（不行）。  

### 5.2.2 HTMLAudioElement和HTMLVideoElement的属性
- buffered：只读，返回媒体缓存的TimeRanges对象；
- currentSrc:只读，返回媒体的URL；
- currentTime：只读，返回当前时间点；
- defaultPlaybackRate：返回对象默认的播放速度，可修改；
- duration：只读，媒体持续时间；
- ended：只读，播放结束时，返回false；
- error：只读，正常返回null，其他返回数字；
- muted：返回是否静音，可修改；
- networkState：只读，返回网络下载状态；
- paused：只读，返回暂停状态；
- playbackRate：返回媒体当前的播放速度，可修改；
- played：只读，返回媒体已播的TimeRanges对象；
- readyState：只读，返回媒体的准备状态；
- seekable：只读，返回媒体定位的TimeRanges对象；
- seeking：只读，返回媒体是否正在定位；
- startTime：只读，返回媒体开始时间；
- volume：返回音量，可修改。  

TimeRanges对象是一个类似数组的对象，包含多个时间段，通常就一个时间段，有两个方法：
- start（index）：返回索引index的开始时间段；
- end（index)：返回索引index的结束时间段。  

## 5.3事件监听
### 5.3.1 事件
audio与video元素除了触发通用事件onclick、onfocus等通用事件外，还触发他们特有的事件：
- onabort：媒体没有下载完，中止；
- oncanplay：能播放，但还需要缓冲；
- oncanlaythrough，能播放，但中间不需要缓冲；
- ondurationchange：媒体长度改变；
- onemptied：媒体元素突然为空；
- onnded：媒体播放结束时；
- onerror：加载出错时；
- onloadeddata：加载媒体数据完成后；
- onloadedmetadata：加载媒体元数据完成后；
- onloadedstart：开始加载媒体；
- onpause：暂停播放时；
- onplay：开始播放时；
- onplaying：正在播放时；
- onprogress：加载数据时；
- onratechange：播放速率改变时；
- onreadystatechange：readyState属性改变时；
- onseeked：成功定位到媒体指定位置，且seeking为false；
- onseeking：正在定位媒体位置；
- onstalled：获取媒体数据的过程中发生错误时；
- onsusped：未获得全部媒体数据前中途停止；
- ontimeupdate：播放位置发生改变时；
- onvolummechange：音量发生变化；
- onwaiting：播放时，由于等不到下一帧而暂停时。  
