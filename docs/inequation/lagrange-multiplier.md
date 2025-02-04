# 拉格朗日乘子法

[https://zhuanlan.zhihu.com/p/21251956159](https://zhuanlan.zhihu.com/p/21251956159).

## 写在前面

这一篇文章仅仅涉及拉格朗日乘数法的最基本的应用, 而且**内容并不完全正确.** 这里仅针对向我一样的普通高中生了解拉格朗日乘数法的最基本的应用, 故会隐去一些细节和证明.

## 介绍

求一个函数的最值是我们经常遇到的数学问题, 但很多时候找到其显式表达式是很困难的(一般情况下有条件约束).而拉格朗日乘数法就很好的规避了求其显式表达式的步骤, 同时帮助我们轻松的求出函数的最值.

比如, 我们要求 $f(x, y)$ 在约束条件 $\phi(x, y) = 0$ 时的条件下的最值时, 我们可以通过引入拉格朗日常数 $\lambda$ 的条件下来构造拉格朗日方程 $\mathcal{L}(x, y, \lambda)$ ,并分别对 $x$ 与 $y$ 求偏导, 再将其与 $\phi(x, y) = 0$ 联立求解的方式来求得最值.

 具体说来就是,

$$
\begin{align}
  & \mathcal{L}(x, y, \lambda) = f(x, y) - \lambda\phi(x, y), \\
  & \begin{cases}
    \dfrac{\partial}{\partial x}\mathcal{L}(x, y, \lambda) = 0, \\
    \dfrac{\partial}{\partial y}\mathcal{L}(x, y, \lambda) = 0, \\
    \phi(x, y) = 0,
  \end{cases} \\
  & \Rightarrow \text{The value of} \ x \ \text{and} \ y, \\
  & \Rightarrow f_{\min/\max} = f(x, y).
\end{align}
$$

更一般地, 对含有 $n$ 个变量及 $k$ 个约束条件的情况, 有,

$$
\mathcal{L}(x_1, \dots, x_n, \lambda_1, \dots, \lambda_k) = f(x_1, \dots, x_n) - \sum_{i = 1}^{k}\lambda_i\phi_i(x_1, \dots, x_n),
$$

这里要注意的是, 我们**并不能直接判断**出我们求出来的是最小值还是最大值(甚至它可能不是最值, 也许以后会提), 但这并不是大问题.

下面来几个例子.

## 例题

$\text{Q:}$ 已知 $x + y - 4 = 0$ , 求 $\dfrac{1}{x} + \dfrac{4}{y}$ 的最小值?

$\text{A:}$ 构造拉格朗日方程 $\mathcal{L}(x, y, \lambda) = \dfrac{1}{x} + \dfrac{4}{y} - \lambda(x + y - 4)$ , 则有下面的方程组,

$$
\begin{cases}   \dfrac{\partial}{\partial x}\mathcal{L}(x, y, \lambda) = 0 \Rightarrow \dfrac{1}{x^2} + \lambda = 0, \\    \dfrac{\partial}{\partial y}\mathcal{L}(x, y, \lambda) = 0 \Rightarrow \dfrac{4}{y^2} + \lambda = 0, \\   x + y - 4 = 0, \end{cases}
$$ 

解得 $x = \dfrac{4}{3}, y = \dfrac{8}{3},$ 故 $\dfrac{1}{x} + \dfrac{4}{y}$ 的最小值为 $\dfrac{9}{4}.$ 

$\text{Q:}$ 已知 $x+2y+2xy = 3$ ,求 $x+2y$ 的最小值?

$\text{A:}$ 构造拉格朗日方程 $\mathcal{L}(x, y, \lambda) = x+2y+\lambda(x+2y+2xy-3),$ 则有,

$$
\begin{cases}   \dfrac{\partial}{\partial x}\mathcal{L}(x, y, \lambda) = 0 \Rightarrow 1-\lambda-2\lambda y = 0, \\   \dfrac{\partial}{\partial y}\mathcal{L}(x, y, \lambda) = 0 \Rightarrow 2-2\lambda-2\lambda x = 0, \\   x+2y+2xy-3 = 0, \end{cases}
$$

解得 $x = 1, y = \dfrac{1}{2},$ 故 $x + 2y$ 的最小值为 $2.$ 
