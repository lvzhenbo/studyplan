# WEB考点
## 一、HTML部分
### 1.格式
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>无标题文档</title>
</head>
<body>
</body>
</html>
```
### 2.常用标记
头标记：`<meta>`、`<title></title>`、`<link href="" rel="" type="">`、`<style>`

文本标记：`<h1>-<h6>`、`<p></p>`、`<hr>`、`<br>`
#### 常用文本格式化标记
|标记|显示效果|
|----|----|
|`<b></b>`和`<strong></strong>`|文字以粗体方式显示（b定义文本粗体，strong定义强调文本）|
|`<i></i>`和`<em></em>`|文字以斜体方式显示（i定义斜体字，em定义强调文本）|
|`<s></s>`和`<del></del>`|文字以加删除线方式显示（HTML5不赞成使用s）|
|`<u></u>`和`<ins></ins>`|文字以粗体方式显示（HTML5不赞成使用u）|
#### 常用特殊字符的表示
|特殊字符|描述|字符的代码|
|----|----|----|
| |空格符|`&nbsp;`（重要）|
|<|小于号|`&lt;`（重要）|
|>|大于号|`&gt;`（重要）|
|&|和号|`&amp;`|
|￥|人民币|`&yen;`|
|©|版权|`&copy;`|
|®|注册商标|`&reg;`|
|°|摄氏度|`&deg`|
|±|正负号|`&plusmn;`|
|×|乘号|`&times;`|
|÷|除号|`&divide;`|
|²|平方2（上标2）|`&sup2;`|
|³|立方3（上标3）|`&sup3;`|

图像标记：`<img src="" alt="" width="" height="" align="" vspace="" hspace="">`

超链接标记：`<a href="跳转目标" target="目标窗口的弹出方式（_self/_blank）">文本或图像</a>`

锚点链接：id属性

表格标记：`<table></table>`、`<tr></tr>`、`<td></td>`、`<th></th>`
### 3.页面元素和属性
列表元素：`<ul></ul>`（无序）、`<ol></ol>`（有序）、`<li></li>`

交互元素：`<details></details>`、`<summary></summary>`、列表
## 二、CSS3部分
### 1.样式规则
选择器{属性1:属性值1;属性2:属性值2;属性3:属性值3;...}
### 2.引入规则
行内式：<标记名 style="属性1:属性值1;属性2:属性值2;属性3:属性值3;...">内容</标记名>

内嵌式
```html
<head>
<style type="text/css">
    选择器{属性1:属性值1;属性2:属性值2;属性3:属性值3;...}
</style>
</head>
```
链入式
```html
<head>
<link href="CSS文件的路径" type="text/css" rel="stylesheet">
</head>
```
### 3.基础选择器
标记选择器：标记名{属性1:属性值1;属性2:属性值2;属性3:属性值3;...}

类选择器：.类名{属性1:属性值1;属性2:属性值2;属性3:属性值3;...}

id选择器：#id名{属性1:属性值1;属性2:属性值2;属性3:属性值3;...}

通配符选择器：*{属性1:属性值1;属性2:属性值2;属性3:属性值3;...}

标签指定式选择器：标签.类名{属性1:属性值1;属性2:属性值2;属性3:属性值3;...}

后代选择器：外标签 内标签{属性1:属性值1;属性2:属性值2;属性3:属性值3;...}

并集选择器：标记/类/id,标记/类/id,标记/类/id,...{属性1:属性值1;属性2:属性值2;属性3:属性值3;...}
### 4.文本样式属性
#### 字体样式属性
font-size:字号大小（px）

font-family:字体

font-weight:字体粗细（normal/bold/bolder/light/100~900）

font-style:字体风格（normal/italic/oblique）

font:综合设置字体样式

@font-face属性（自定义未安装字体）
```css
@font-face{
    font-family:字体名称;
    src:字体路径;
}
```
word-wrap属性（自动换行）：选择器{word-wrap:属性值（normal/break-word）;}
#### 文本外观属性
color:文本颜色

letter-spacing:字间距

word-spacing:单词间距

line-height:行间距

text-transform:文本转换

text-decoration:文本装饰（none，underline，overline，line-through）

text-align:水平对齐方式

text-indent:首行缩进

white-space:空白符处理

text-shadow:阴影效果

text-overflow:标示对象溢出文本
### 5.链接伪类
|  超链接标记`<a>`的伪类  |  含义  |
|----|----|
|  a:link{css样式规则}  |  未访问时超链接的状态  |
|  a:visited{css样式规则}  |  访问后超链接的状态  |
|  a:hover{css样式规则}  |  鼠标经过悬停时超链接的状态  |
|  a:active{css样式规则}  |  鼠标单击不动时超链接的状态  |
### 6.盒子模型
#### 盒子模型的属性
```css
.box{
    width: 200px;               /* 盒子的长度 */
    height: 50px;               /* 盒子的高度 */
    border: 15px solid red;     /* 盒子的边框大小、线条及颜色 */
    background: #CCC;           /* 盒子的背景色 */
    padding: 30px;              /* 盒子的内边距 */
    margin: 20px;               /* 盒子的外边距 */
}
```
#### 盒子的宽与高

* 盒子的总宽度=width+左右内边距之和+左右边框高度之和+左右外边距之和

* 盒子的总宽度=width+左右内边距之和+左右边框高度之和+左右外边距之和

#### 边框属性

|  设置内容  |  样式属性  |  常用属性值  |
|----|----|----|
|  边框样式  |  border-style:上边[右边 下边 左边];  |  none 无(默认)、solid 单实线、dashed 虚线、dotted 点线、double 双实线  |
|  边框宽度|bordeer-width:上边[右边 下边 左边]  |  像素值  |
|  边框颜色|border-color:上边[右边 下边 左边]  |  颜色值、#十六进制、rgb(r,g,b)、rgb(r%, g% b%)  |
|  综合设置边框  |  border:四边宽度 四边样式 四边颜色;  ||
|  圆角边框  |  border-radius:水平/垂直半径参数  |  像素值或百分比  |
|  图片边框  |  border-images:图片路径 裁切方式/边框高度/边框扩展距离 重复方式;  ||
#### 背景属性
背景颜色：background-color:颜色值、#十六进制、rgb(r,g,b)、rgb(r%, g% b%);

背景图像：background-image:url(图片地址);

图像平铺：background-repeat:repeat/no-repeat/repeat-x/rpeat-y;

图像位置（no-repeat）：background-position:水平位置 垂直位置;

图像大小：background-size:属性值1 属性值2;
|属性值|说明|
|---|---|
| 像素值 | 设置背景图像的高度和宽度。第一个值设置宽度，第二个值设置高度。如果只设置一个值，则第二个值会默认为auto |
| 百分比 | 以父元素的百分比来设置背景图像的宽度和高度。第一个值设置宽度，第二个值设置高度。如果只设置一个值，则第二个值会默认为auto |
| cover | 把背景图像扩展至足够大，是背景图像完全覆盖背景区域。背景图像的某些部分也许无法显示在北京定位区域中 |
| contain | 把图像扩展至最大尺寸，以是其宽度和高度完全适应内容区域 |

### 7.浮动与定位

#### 浮动属性float
* 选择器{float:属性值;}
#### 清除浮动
* 选择器{clear:属性值}
#### overflow属性
选择器{overflow:属性值}
|属性值|描述|
|---|---|
|visible|内容不会被修剪，会呈现在元素之外(默认值)|
|hidden|溢出内容会被修剪，并且被修剪的内容时不可见的|
|auto|在需要时产生滚动条，即自适应所要显示的内容|
|scroll|溢出内容会被修剪，且浏览器会始终显示滚动条|
#### 定位属性
选择器{position:属性值}
|值|描述|
|----|----|
|static|静态定位（默认定位方式）|
|relative|相对定位，相对于其原文档流的位置进行定位|
|absolute|绝对定位，相对于其上一个已经定位的父元素进行定位|
|fixed|固定定位，相对于浏览器窗口进行定位|
#### 边偏移
top（上），bottom（下），left（左），right（右）
#### 元素的转换
选择器{display:属性值}
* inline:此元素将显示为行内元素
* block:此元素将显示为块元素
* inline-block:元素将显示为行内块元素
* none:此元素将被隐藏不显示，也不占用页面内容
### 8.表单
#### input元素的相关属性
<table>
<tr>
<th>属性</th>
<th>属性值</th>
<th>描述</th>
</tr>
<tr>
<td rowspan="18">type</td>
<td>text</td>
<td>单行文本输入框</td>
</tr>
<tr>
<td>password</td>
<td>密码输入框</td>
<td>
</tr>
<tr>
<td>radio</td>
<td>单选按钮</td>
<td>
</tr>
<tr>
<td>checkbox</td>
<td>复选框</td>
<td>
</tr>
<tr>
<td>button</td>
<td>普通按钮</td>
<td>
</tr>
<tr>
<td>submit</td>
<td>提交按钮</td>
<td>
</tr>
<tr>
<td>reset</td>
<td>重置按钮</td>
<td>
</tr>
<tr>
<td>image</td>
<td>图像形式的提交按钮</td>
<td>
</tr>
<tr>
<td>hidden</td>
<td>隐藏域</td>
<td>
</tr>
<tr>
<td>file</td>
<td>文件域</td>
<td>
</tr>
<tr>
<td>email</td>
<td>E-mail地址的输入域</td>
<td>
</tr>
<tr>
<td>url</td>
<td>URL地址的输入域</td>
<td>
</tr>
<tr>
<td>number</td>
<td>数值的输入域</td>
<td>
</tr>
<tr>
<td>range</td>
<td>一定范围内数字值的输入域</td>
<td>
</tr>
<tr>
<td>Date pickers(date，month，week，time，datetime，datetime-local)</td>
<td>日期和时间的输入类型</td>
<td>
</tr>
<tr>
<td>search</td>
<td>搜索域</td>
<td>
</tr>
<tr>
<td>color</td>
<td>颜色输入类型</td>
<td>
</tr>
<tr>
<td>tel</td>
<td>电话号码输入类型</td>
<td>
</tr>
<tr>
<td>name</td>
<td>由用户自定义</td>
<td>控件的名称</td>
<td>
</tr>
<tr>
<td>value</td>
<td>由用户自定义</td>
<td>input控件中的默认文本值</td>
<td>
</tr>
<tr>
<td>size</td>
<td>正整数</td>
<td>input控件在页面中的显示宽度</td>
<td>
</tr>
<tr>
<td>readonly</td>
<td>readonly</td>
<td>该控件内容为只读（不能编辑修改）</td>
<td>
</tr>
<tr>
<td>disabled</td>
<td>disabled</td>
<td>第一次加载页面时禁用该控件（显示为灰色）</td>
<td>
</tr>
<tr>
<td>checked</td>
<td>checked</td>
<td>定义选择控件默认被选中的项</td>
<td>
</tr>
<tr>
<td>maxlength</td>
<td>正整数</td>
<td>控件允许输入的最多字符数</td>
<td>
</tr>
<tr>
<td>autocomplete</td>
<td>on/off</td>
<td>设定是否自动完成表单字段内容</td>
<td>
</tr>
<tr>
<td>autofocus</td>
<td>autofocus</td>
<td>指定页面加载后是否自动获取焦点</td>
<td>
</tr>
<tr>
<td>form</td>
<td>form元素的id</td>
<td>设定字段隶属于哪一个或多个表单</td>
<td>
</tr>
<tr>
<td>list</td>
<td>datalist元素的id</td>
<td>设定字段的候选数据值列表</td>
<td>
</tr>
<tr>
<td>multiple</td>
<td>multiple</td>
<td>指定输入框是否可以选择多个值</td>
<td>
</tr>
<tr>
<td>min、max和step</td>
<td>数值</td>
<td>规定输入框所允许的最大值、最小值及间隔</td>
<td>
</tr>
<tr>
<td>pattern</td>
<td>字符串</td>
<td>验证输入的内容是否与定义的正则表达式匹配</td>
<td>
</tr>
<tr>
<td>placeholder</td>
<td>字符串</td>
<td>为input类型的输入框提供一种提示</td>
<td>
</tr>
<tr>
<td>required</td>
<td>required</td>
<td>规定输入框填写的内容不能为空</td>
<td>
</tr>
</table>

#### 其他表单元素
textarea元素
````html
<textarea cols="每行中的字符数" rows="显示的行数">
    文本内容
</textarea>
````
select元素
````html
<select>
    <option>选项1</option>
    <option>选项2</option>
    <option>选项3</option>
    ...
</select>
````
datalist元素
````html
<input type="text" list="namelist"/>
<datalist id="namelist">
    <option>选项1</option>
    <option>选项2</option>
    <option>选项3</option>
    ...
</datalist>
````
### 9.多媒体
视频：`<video src="视频文件路径" controls="controls"></video>`

音频：`<audio src="音频文件路径" controls="controls"></audio>`
## 三、课本内所有例题和阶段案例源代码
链接: https://pan.baidu.com/s/1EMlvPRDJSSRolEjtQVZTrQ 提取码: jym7