
---
layout: post
title: "第一篇博客"
date: 2012-06-26 23:01
comments: true
categories:
---
##两种加入数学公式的办法

###[第一种:markdown保持rdiscount不变](http://greglus.com/blog/2011/11/29/integrate-MathJax-LaTeX-and-MathML-Markup-in-Octopress/)

<div markdown="0">
\[ i\hbar\frac{\partial \psi}{\partial t}
  = \frac{-\hbar^2}{2m} \left(
    \frac{\partial^2}{\partial x^2}
    + \frac{\partial^2}{\partial y^2}
    + \frac{\partial^2}{\partial z^2}
  \right) \psi + V \psi \]
</div>

###[第二种:markdown改成kramdown](http://www.idryman.org/blog/2012/03/10/writing-math-equations-on-octopress/)

$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
