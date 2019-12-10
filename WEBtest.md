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