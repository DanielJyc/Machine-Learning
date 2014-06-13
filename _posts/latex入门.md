title: LaTex入门
date: 2014-05-19 00:09:33
tags: LaTex
---
[TOC]
<!--more-->
##1. [安装](http://www.ctex.org/HomePage)

##2. 简单语法
###最简单的Hello world.
打开WinEdt，建立一个新文档，将以下内容复制进入文档中，保存，保存类型选择为UTF-8。 

``` LaTex
\documentclass{article} 
\begin{document} 
  hello, world 
\end{document} 
```
然后在WinEdt的工具栏中找到编译按钮（在垃圾桶和字母B中间），在下拉菜单中选择XeTeX，并点击编译。 
如果顺利的话，我们就可以顺利生成出第一个pdf文件，点击工具栏中的放大镜按钮就可以快速打开生成的pdf文件。 

###加入*中文，标题，作者和注释*后的Hello World.
```
\documentclass{article}
\usepackage{CJK}  %中文1
  \author{My Name}
  \title{The Title}
\begin{document}
\begin{CJK*}{GBK}{song}  %中文2
\maketitle
Hello World. \\  %回车
这里输入中文
\end{CJK*}  %中文3
\end{document}
```
##章节和段落
```
\documentclass{article}
\usepackage{CJK}
  \author{My Name}
  \title{The Title}
\begin{document}
\begin{CJK*}{GBK}{song}
\maketitle
  \section{一级标题} 中国……
    \subsection{二级标题} Beijing is the capital of China.
      \subsubsection{三级标题}
        \paragraph{Tian'anmen Square}is in the center of Beijing
          \subparagraph{Chairman Mao} is in the center of Tian'anmen Square
      \subsection{二级标题}
        \paragraph{Sun Yat-sen University} is the best university in Guangzhou.
\end{CJK*}
\end{document}
```
## 加入目录
将`\maketitle`改为`\tableofcontents`，即可。
```
\documentclass{article}
\usepackage{CJK}
  \author{My Name}
  \title{The Title}
\begin{document}
\begin{CJK*}{GBK}{song}
\tableofcontents
  \section{一级标题} 中国……
    \subsection{二级标题} Beijing is the capital of China.
      \subsubsection{三级标题}
        \paragraph{Tian'anmen Square}is in the center of Beijing
          \subparagraph{Chairman Mao} is in the center of Tian'anmen Square
      \subsection{二级标题}
        \paragraph{Sun Yat-sen University} is the best university in Guangzhou.
\end{CJK*}
\end{document}
```
## 加入公式
```
\documentclass{article}
  \usepackage{amsmath}
  \usepackage{amssymb}
\begin{document}
The Newton's second law is F=ma.

The Newton's second law is $F=ma$. 

The Newton's second law is  $$F=ma$$

The Newton's second law is  \[F=ma\]

Greek Letters $\eta$ and $\mu$

Fraction $\frac{a}{b}$

Power $a^b$

Subscript $a_b$

Derivate $\frac{\partial y}{\partial t} $

Vector $\vec{n}$

Bold $\mathbf{n}$

To time differential $\dot{F}$
\end{document}
```
> **公式效果**
>The Newton's second law is F=ma.

>The Newton's second law is $F=ma$. 

>The Newton's second law is  $$F=ma$$

>The Newton's second law is  \[F=ma\]

>Greek Letters $\eta$ and $\mu$

>Fraction $\frac{a}{b}$

>Power $a^b$

>Subscript $a_b$

>Derivate $\frac{\partial y}{\partial t} $

>Vector $\vec{n}$

>Bold $\mathbf{n}$

>To time differential $\dot{F}$


