+++
Title = "Markdown Syntax"
date = "2016-01-01T13:34:32+08:00"
+++

# Markdown Syntax
Markdown 是一個輕量級標記式語言([wiki][wiki])，它是以純文字的方式編寫文件， 使用起來很方便，我喜歡用它來做筆記，它還可以表示數學表示式(Latex語法)且能夠輕易地將其轉成其他格式(HTML, PDF) 以下針對幾個常用的語法做記錄：

<a name="font"/>
## Font
- _Italic 斜體_

    Syntax

    `*Italic*`  

    `_Italic_`

    Preview

  > _Italic_

- **Bold 粗體**

  Syntax

    `**Bold**`

  Preview

  > **Bold**

- **_Italic and Bold_**

  Syntax

    `***Italic and Bold***`  

    `*_Italic and Bold_*`    

    `_*Italic and Bold*_`

  Preview

  > **_Italic and Bold_**

- Color

  Syntax

    `<font color='red'> words </font>`

  Preview  
<font color='0x00ffcc'> Hi </font>

- Delete line

  Syntax

    `~~words~~`

  Preview

  > ~~Error~~

## Heading
- number of # represent the heading number  
- using dash `___`(more than 3) under heading can do the same thing  

Preview

# Head 1
## Head 2
### Head 3
#### Head 4
##### Head 5
### indent
Syntax<br> `&nbsp;`

Preview<br> Hi    Hello

### Line
Syntax

  `Using dash ___ (more than 3)`

Preview

--------------------------------------------------------------------------------

### Paragraph or new line
在 markdown 裡換行主要有兩個方式：
- soft break: 在句尾多加兩個空白
- hard break: 在兩句之間塞一行空白

## Block quote
假如需要用到引用可以使用 `>` 將文字標註起來

Syntax  

`>`

Preview

> I'm Josh.

> My country is Taiwan.<br>Welcome to my website. Hope you would like it.

## Link
- inline link

  Syntax

  `[words](links)`

  Preview

  > [Google](https://www.google.com.tw)

- extern link  

  Syntax

  `[words][tags]`

  Preview

  > [Google][homepage]

### Image link
Markdown 也可以嵌入圖片方式跟連結一樣只是在前面多加了`!`  

Syntax

 `![name](link)`<br> `![name][link_tag]`  

Preview

> ![Github](https://cdn1.iconfinder.com/data/icons/picons-social/57/github-128.png)<br>![Github][gitimg]

### Head link
Markdown 可以link 同一份markdown 裡的標題  

Syntax   
 There must be a flag `<a name="tag"/>` in front of heading, and then  
 `[a link](#tag)` link will work.  

Preview  
 [Font](#font)

## List
- 有序條列

  Syntax  

    `1. Item_1`     

    `2. Item_2`  

  Preview  
  1. Item_1
  2. Item_2

- 無序數列

  Syntax  

  `* Item_1`  

  `* Item_2`

  Preview
  - Item_1
  - Item_2

- Nested

  Syntax  

  `* Item 1`  

    `* Item 1_1`

  Preview  
  - Item_1
    - Item 1_1

## Math
用`$`包起來的表示式可以呈現成數學式的樣子
- inline display  

  Syntax   

  `$expression$`

  Preview  

  The equation: $I = \int \rho R^2 dV$

- extern display  

  Syntax  

  `$$expression$$`

  Preview  

  The equation:

  $$I = \int \rho R^2 dV$$

### Fraction
  Syntax<br>  `$\frac{numerator}{denominator}$`

  Preview<br>  

  $$\frac{x^2+y^2}{y^3}$$

### Index
  Syntax<br>  `$x^upper$`<br>  `$x_sub$`

  Preview<br>  $x^2$   $x_2$

### Function
  `sqrt{}` : $\sqrt{27}$  

  `int{}`  : $\int{}$  

  `binom{}{}`: $\binom{n}{m}$

  `overline{}`: $\overline{x}$  

  `\log{}` : $\log{x}$  

  `\sin{}` : $\sin{x}$

  `\frac{\partial f}{\partial x}` : $\frac{\partial v}{\partial t}$  

  `\lim_{xtoy}`: $\lim_{x \to y}$

### Expression
`x \in A` : $x \in A$<br>`A \cap B`: $A \cap B$<br>`A \cup B`: $A \cup B$<br>`5 \pm 2` : $5 \pm 2$<br>`\infty`  : $\infty$

## Table

name | mail
---- | --------------------
josh | joshsyu.tw@gmail.com

## Reference
[Markdown Online Lecture](http://markdowntutorial.com/lesson/1/)<br>[Markdown Example](http://www.unexpected-vortices.com/sw/rippledoc/quick-markdown-example.html)<br>[Markdown Math Expression](http://www.calvin.edu/~rpruim/courses/m343/F12/RStudio/LatexExamples.html)  

[homepage]: https://www.google.com.tw
[gitimg]: https://cdn4.iconfinder.com/data/icons/ionicons/512/icon-social-github-128.png
[wiki]: https://zh.wikipedia.org/wiki/Markdown#.E7.BC.96.E8.BE.91.E5.99.A8
