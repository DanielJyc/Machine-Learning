title: ML学习笔记--梯度和牛顿算法
date: 2014-05-21 
tags: ML
---

[TOC]
<!--more-->

#一、 符号说明
$m$:样本数目（行数）<-->$i$某一行
$n:$特征数目（列数）<-->$j$某一列
$x,y$:输入和输出变量
$i^{th}$:training example<-->$(x^{(i)}, y{(j)})$
$\theta$学习参数
$h_{\theta}(x)$:输出函数



#二、 算法总结
##1. 最小均方（误差）算法LMS
该算法是为了使损失函数最小。**损失函数**为：
![enter image description here][1]
![enter image description here][2]
**得到梯度下降的基本算法**，下面会对其展开详细说明
![enter image description here][3]
###1.1 批量梯度下降
缺点：不适合数据量很大的情况
![enter image description here][4]
###1.2 随机梯度下降
![enter image description here][5]
###1.3 另外一种最小化$J_{\theta}$的算法**最小二乘法**
![enter image description here][6] $(J=0)$
##2. 局部加权线性回归
优点：在一定程度上防止了过拟合和欠拟合

* 参数化的学习算法：有固定参数学习，用来数据拟合
* 非参数学习算法： 局部加权线性回归
![enter image description here][7]
##3.逻辑回归（第一种：最大化$L(\theta)$）
* 基本公式：
![enter image description here][8]
* **$\theta$**的训练方法：利用梯度上升，来最大化似然函数(Likehood Function):
![enter image description here][9]
* **注：**得到的最终结果，与LMS中的循环规则完全一样。但是，不同之处在于：此处$h_{\theta}(x^{(i)})$为非线性的。

##4.牛顿（第二种：最大化$L(\theta)$）













![enter image description here][10]



#三、 从概率角度解释最小化$J$的含义
使误差为0的概率最大<-->最大化相似函数**$l(\theta)$或者$L(\theta)$**<-->最小化**$J$** ：最大似然估计
![enter image description here][11]






> Written with [StackEdit](https://stackedit.io/).


  [1]: https://lh6.googleusercontent.com/-ol10ZJK9cPo/U3t1OIb2MCI/AAAAAAAAAOw/LNjQEVvwcsg/s0/cost+function.jpg "cost function.jpg"
  [2]: https://lh3.googleusercontent.com/-4mWbVm1nT1c/U3wENr2EzmI/AAAAAAAAARc/oXMSN244R0Q/s0/hx.jpg "hx.jpg"
  [3]: https://lh6.googleusercontent.com/-yKTMmTUpAF0/U3t2oP6iCrI/AAAAAAAAAPE/Zo5gG0WfJmM/s0/gradient+descent.jpg "gradient descent.jpg"
  [4]: https://lh5.googleusercontent.com/-CQbW2GrkIPs/U3t23xymGBI/AAAAAAAAAPQ/slVUqCcAQdY/s0/batch.jpg "batch.jpg"
  [5]: https://lh4.googleusercontent.com/-eG2nD3WCY50/U3t3Lm22MMI/AAAAAAAAAPc/1Bl4lcqqvwI/s0/stochastic+gradient+descent.jpg "stochastic gradient descent.jpg"
  [6]: https://lh5.googleusercontent.com/-W1kHzCe7eLI/U3t4HBY1RrI/AAAAAAAAAPw/YgOyhxwX5aA/s0/Least+squares+revisited.jpg "Least squares revisited.jpg"
  [7]: https://lh6.googleusercontent.com/-jnTUq0qekYE/U3t7j27beSI/AAAAAAAAAQc/cWQi353jmzk/s0/Locally+weighted+linear+regression.jpg "Locally weighted linear regression.jpg"
  [8]: https://lh4.googleusercontent.com/-KWT4CR3C4Vs/U3t8K_dBSXI/AAAAAAAAAQo/NqpWlHf1Fm0/s0/logistic+function.jpg "logistic function.jpg"
  [9]: https://lh5.googleusercontent.com/-UUaGwVVAbjQ/U3wEuS9XJmI/AAAAAAAAARo/O_TDqJHv3So/s0/logistic+function2.jpg "logistic function2.jpg"
  [10]: https://lh5.googleusercontent.com/-fFqF7wklLcQ/U3wJKyGh3PI/AAAAAAAAAR0/O9fF82XRmFM/s0/%E7%89%9B%E9%A1%BF%E6%96%B9%E6%B3%95.jpg "牛顿方法.jpg"
  [11]: https://lh3.googleusercontent.com/-TP7AitLa8bg/U3t5mi8JLqI/AAAAAAAAAQM/3zIC3IrN04s/s0/likelihood.jpg "likelihood.jpg"