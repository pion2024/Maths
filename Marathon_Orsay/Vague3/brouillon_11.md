# Prob11 

![image-20250412194636784](C:\Users\T480s\AppData\Roaming\Typora\typora-user-images\image-20250412194636784.png)

条件： 

	1. $\forall x,\forall y, f(2^x+2y)=2^yf(f(x))f(y)$ . 
	1. 令$x=0$，由1得 $f(1+2y)=2^yf(f(0))f(y)$
	1. 令$y=0$，由1得 $f(2^x)=f(f(x))f(0)$

由2知，$f(0)=0 \implies f(f(0))=f(0)=0 \implies \forall t\in\mathbb{R},f(t)=f(1+2\frac{t-1}{2}) = 0 \implies f=0$.

若 $f(0) \neq 0 $，则

- 利用1，分别考虑令 $x=a,y=2^{b-1}$ 和 $x=b,y=2^{a-1}$，得到：

  - (4) $\forall a\in\mathbb{N},\forall b\in\mathbb{N},f(2^a+2^b) = f(2^a+2\times2^{b-1}) = 2^{2^{b-1}}f(f(a))f(2^{b-1}) = 2^{2^{b-1}}f(f(a))f(f(b-1))f(0)$

  - (5)$\forall a\in\mathbb{N},\forall b\in\mathbb{N},f(2^b+2^a) = f(2^b+2\times2^{a-1}) = 2^{2^{a-1}}f(f(b))f(2^{a-1}) = 2^{2^{a-1}}f(f(b))f(f(a-1))f(0)$
  - 重点研究商量个式子的比较。

- 令 $b=a+1$，得到 $\forall a\in\mathbb{R}$ :

  - $f(2^a+2^{a+1}) = 2^{2^{a}}f(f(a))f(f(a))f(0) = f(2^{a+1}+2^a) = 2^{2^{a-1}}f(f(a+1))f(f(a-1))f(0)$
  - 注意到存在等比数列的特征，于是尝试获得 $f$ 在整数集子集上的取值通项公式。
  - 因为$f(0)\neq 0$, 于是 $2^{2^{a-1}}f(f(a))f(f(a))= f(f(a+1))f(f(a-1))$.
  - 令 $g(x)=f(f(x)), h(n)=\frac{g(n)}{2^{2^n}}$, 则 $\forall n\in\mathbb{N}, h^2(n)=h(n+1)h(n-1), h(0)=\frac{g(0)}{2}=\frac{f(f(0))}{2}$。
  - 但是要想得到等比数列通项，还需要确保没有$h$的取值不为零。下面分类讨论 $h(0)$ 的取值情况。

- $h(0) = \frac{f(f(0))}{2} = 0 \implies f(f(0))=0 \implies \forall y\in\mathbb{R}, f(1+2y) = 2^yf(f(0))f(y) = 0 \implies \forall t\in\mathbb{R}, f(t)=0$

- 假设 $h(0) \neq 0$ 即 $f(f(0)) \neq 0 $， 

  - 首先用归纳法证明 $\forall n\in\mathbb{N}, f(f(n))\neq 0$：
    - 由(4)和(5)，有等式 $2^{2^{b-1}}f(f(a))f(f(b-1))f(0) = 2^{2^{a-1}}f(f(b))f(f(a-1))f(0) \implies$ 
      (6) $ 2^{2^{b-1}-2^{a-1}}f(f(a))f(f(b-1)) = f(f(b))f(f(a-1))$对于任意实数$a,b$成立。于是可令$b=1,a=0$得 $2^{1/2}f(f(0))f(f(0))=f(f(1))f(f(-1))$.
    - $h(0) \neq 0 \iff f(f(0))\neq 0 \implies f(f(1))f(f(-1)) \neq 0 \implies f(f(1)) \neq 0 \implies h(1) \neq 0$
    - 现在令(6)中的 $a=n,b=n+1$，于是 $\forall n\in\mathbb{N},$
      $h(n)\neq0 \implies f(f(n))\neq 0 \implies$
      $f(f(n+1))f(f(n-1)) = 2^{2^{n}-2^{n-1}}f(f(n))f(f(n+1-1)) = 2^{2^{n-1}}f(f(n))f(f(n)) \neq 0 $$\implies f(f(n+1)) \neq 0 \implies h(n+1) \neq 0$
    - 所以 $\forall n\in\mathbb{N}, f(f(n))\neq0, i.e. h(n)\neq 0$.
  - 前面已经得到 $\forall n\in\mathbb{N}, (\frac{f(f(n))}{2^{2^n}})^2 = h^2(n)=h(n+1)h(n-1)$ 且 $h(n) \neq 0$, 于是
    - $\exists k\neq 0, \frac{h(n)}{h(n-1)} = \frac{h(n-1)}{h(n-2)} = \cdots = \frac{h(1)}{h(0)} = k$
    - 记 $A=f(f(0)) \neq 0$
    - $\forall n\in\mathbb{N}, h(n)=k^n\cdot h(0) = \frac{f(f(0))}{2}k^n \implies f(f(n)) = \frac{f(2^n)}{f(0)} = 2^{2^n-1}Ak^n $$\implies f(2^n)= 2^{2^n-1}Ak^nf(0)$  ----(7)
    - 我们还想求出$k$，从而能够估计$f(2^n)$。于是考虑构造某个含有$k$的等式。
  - 现在我们能够处理类似 $f(2^n)$ 的项了
    - 再次考虑式子(5)并将(7)代入. 得 $\forall a\in\mathbb{N},\forall b\in\mathbb{N},f(2^a+2^b) = 2^{2^{a-1}}f(f(b))f(2^{a-1}) = 2^{2^{a-1}}\frac{f(2^b)}{f(0)}f(2^{a-1})$ 
      $ = 2^{2^{a-1}}\cdot2^{2^b-1}Ak^b\cdot2^{2^{a-1}-1}Ak^{a-1}f(0) = 2^{2^a+2^b}\cdot \frac{A^2}{4}\cdot k^{a+b-1}f(0)$
    - 令$a=b=n$,于是 $f(2^{n+1}) = 2^{2^n+2^n}\cdot \frac{A^2}{4}\cdot k^{2n-1}f(0) = \frac{1}{4}2^{2^{n+1}}k^{2n-1}A^2f(0)$
    - 另一方面，由(7)，$f(2^{n+1})=2^{2^{n+1}-1}Ak^{n+1}f(0)$。于是$\frac{1}{4}2^{2^{n+1}}k^{2n-1}A^2f(0) = 2^{2^{n+1}-1}Ak^{n+1}f(0)$，于是 $\forall n\in\mathbb{N}, k^{n-1}=\frac{2}{A}$ 因为根据假设 $A=f(f(0))\neq0, f(0)\neq0$。
  - 注意到$\forall n\in\mathbb{N}, k^{n-1}=\frac{2}{A}$对于任意$n$都成立，而$k,A$是定值，故矛盾。

- 于是$f(f(0))=0$，由2，符合题意的函数必须满足$f=0$。代入$f=0$ 满足题目条件，所以所有满足条件的函数$f$为 $f=0$。
