# 高数笔记

## 第一讲 预备知识

### 预备知识

题目1 

> 已知$f(x)=\ln{(x+\sqrt {x^2+1})}$，求$f^{-1}(x)$及其定义域 

- 扩展1:
公式扩展
$$
\sqrt a-\sqrt b=\cfrac{a-b}{\sqrt a+\sqrt b}
$$
证明$f(x)=\ln{(x+\sqrt {x^2+1})}$为奇函数
$$
f(-x)=\ln {(-x+\sqrt{x^2+1})}=\ln{\cfrac{1}{x+\sqrt{x^2+1}}}=-f(x)
$$
- 扩展2:
双曲正弦函数
$$
\sinh x=\cfrac{\mathrm{e}^x-\mathrm{e}^{-x}}{2}
$$
反双曲正弦函数
$$
\sinh{^{-1}x}=f(x)=\ln{(x+\sqrt{x^2+1})}
$$
导数
$$
(\sinh{^{-1}x})^\prime=f^\prime(x)=\cfrac{1}{\sqrt{x^2+1}}
$$
导数的原函数
$$
\int_{}^{}\cfrac{1}{\sqrt{x^2+a^2}}\,\mathrm{d}x=\ln{(x+\sqrt{x^2+a^2})+C}
$$
- 扩展3:
双曲余弦函数(**悬链线**)
$$
\cosh x=\cfrac{\mathrm{e}^x+\mathrm{e}^{-x}}{2}
$$
反双曲余弦
$$
\cosh{^{-1}x}=\ln{(x+\sqrt{x^2-1})}
$$

### 如何写出复合函数
1. 写出广义函数$f[\varphi(x)]=\cdots$
2. 画出内层函数$\varphi(x)$图像
3. 写出结论

> 例题：已知
$$
f(x) =
\begin{cases} 
\ln \sqrt x,  & x\ge1\\
2x-1, & x<1
\end{cases}
$$
求$f[f(x)]$

### 其他
#### 因式分解公式
$$
\begin{aligned}
a^3-b^3&=(a-b)(a^2+ab+b^2) \\
a^3+b^3&=(a+b)(a^2-ab+b^2) \\
a^n-1&=(a-1)(a^{n-1}+a^{n-1}+\cdots+a+1)\\
 &=(a-1)\sum\limits_{i=1}^{n-1}{a^i}=a\sum\limits_{i=0}^{n-1}{a^i}-\sum\limits_{i=0}^{n-1}{a^i}\\
 a^n-b^n&=b^n[(\frac{a}{b})^n-1]=b^n(\frac{a}{b}-1)\sum\limits_{i=0}^{n-1}{(\frac{a}{b})^i}
\end{aligned}
$$

#### 万能公式(算积分有奇效)
$$
\text{let }u=\tan{\cfrac{x}{2}} \Rightarrow \left\{
\begin{array}{ll}
\mathrm{d}x &=& \cfrac{2}{1+u^2}\mathrm{d}x \\
\sin x      &=& \cfrac{2u}{1+u^2} \\
\cos x      &=& \cfrac{1-u^2}{1+u^2} \\
\end{array}
\right.
$$


#### 常用不等式
$$
\sqrt{ab} \le \cfrac{a+b}{2} \le \sqrt{\cfrac{a^2+b^2}{2}}(a,b>0)
$$
$$
\sin x<x<\tan x (0<x<\cfrac{\pi}{2})
$$
$$
\cfrac{1}{1+x}<\ln{(1+\cfrac{1}{x})}<\cfrac{1}{x}(x>0)
$$

## 第二讲 数列极限
### 定义法
#### 数列极限定义
1. (任取) $\forall\varepsilon>0, |x_n-a| < \varepsilon $  
2. 反解出 $n>g(\varepsilon)=\cdots$
3. 取$N=\lfloor g(\varepsilon) \rfloor+1$ 
- 结论：当$n>N=\lfloor g(\varepsilon) \rfloor+1$时，$\forall\varepsilon>0$，$|x_n-a|<\varepsilon $

```
注：\lfloor \rfloor是向下取整。\lceil \rceil是向上取整
```
- $\varepsilon-N$语言  

$$
\lim_{n \to \infty}x_n=a \Leftrightarrow  \exists N>0,当 n>N,恒有|x_n-a|<\varepsilon
$$

$$
\exists N>0,当 n>N,恒有|x_n-a|<\varepsilon  \Leftrightarrow  \lim_{n \to \infty}x_n=a  
$$

```
注：双向箭头互推注意 反着也可以推。
```


#### 例题
>证明：若$\lim\limits_{n\to\infty}{a_n}=A$,则$\lim\limits_{n\to\infty}{|a_n|}=|A|$

### 性质
- 唯一性
- 有界性
- 保号性(脱帽法)
- 推论(戴帽法)

#### 保号性(脱帽法)

设$a_n$存在极限$a$，且$a>0($或$a<0)$，则存在正整数$N$，当$n>N$时，有$a_n>0($或$a_n<0)$

$$
\lim\limits_{n\to\infty}{a_n}=a>0 \Rightarrow\exists n>N,a_n>0
$$

#### 推论1(戴帽法)
$$
\left.\begin{array}{r}
a_n>0  \\ 
\exists n>N,\lim\limits_{n\to\infty}{a_n}=a 
\end{array}\right\} \Rightarrow a\ge 0
$$
```
戴帽法有等号(a>=0)！脱帽法没有等号！
```
#### 推论2(重要)
若$\ \lim\limits_{n\to\infty}{a_n}=A\ne0$，则$\ \exists N$，当$\ n>N\ $时，$\quad|a_n|>\lambda|A|\quad (0<\lambda<1)$
>例题：设$\lim\limits_{n\to\infty}{a_n}=a$，且$a\ne0$，则当$\ n\ $充分大时，有(  )  
>$\text{(A)}\quad|a_n|>\cfrac{|a|}{2}\qquad\text{(B)}\quad a_n>a-\cfrac{1}{n}\quad\cdots$

###  运算规则
```
只需注意极限必须先存在才可以进行运算！
```
### 夹逼准则(数列)
如果数列$\{x_n\},\{y_n\},\{z_n\}$满足以下条件  
$$
\begin{cases}
y_n\le x_n\le z_n  \\
\lim\limits_{n\to\infty}{y_n}=a,\lim\limits_{n\to\infty}{z_n}=a
\end{cases}
$$
则数列$\{x_n\}$的极限存在且$\lim\limits_{n\to\infty}{x_n}=a$  
```
可以不验证等号，y_n和z_n与x_n中间可以是小于或小于等于。
```

```
一般只动分母，不动分子！
```

```
注意有些数列的通项公式是∑求和的形式
```

>例题：求极限
$$
\lim\limits_{n\to\infty}{\left(\cfrac{1}{n^2+n+1}+\cfrac{2}{n^2+n+2}+\cdots+\cfrac{n}{n^2+n+n}\right)}
$$

### 单调有界准则
单调有界数列必有极限。即若数列$\{x_n\}$单调递增(递减)，且有上界(下界)，则$\lim\limits_{n\to\infty}{x_n}$存在

#### 做题技巧
1. 证明<u>**数列单调性**</u>和求出<u>**数列上/下界**</u>
2. 如果需要计算$\lim\limits_{n\to\infty}{a_n}$那么可以假定$\lim\limits_{n\to\infty}{a_n}=A$，解方程得到极限值  

### 证明数列没有极限(发散)
- 方法一：找两个极限不同的<u>**_子列_**</u>，如写出$\{a_n\}$的$\{a_{2k}\}$和$\{a_{2k+1}\}$，证明其极限值不同    
- 方法二：找一个发散的子数列  

```
数列收敛=数列有极限；数列发散=数列没有极限
```
>设$a_n=\big(1+\cfrac{1}{n}\big)\sin{\cfrac{n\pi}{2}}$，证明数列$a_n$没有极限

### 其他注意事项
```
数学归纳法
```

## 第三讲 函数极限与连续性  
### 邻域

### 函数极限定义  
- 四句话定义
$$
\begin{array}{ll}
\lim\limits_{x\to x_0}{f(x)}=A & \Leftrightarrow \\
& \forall\varepsilon>0,\quad\exists\delta>0,& \text{使当}\\
& 0<|x-x_0|<\delta, & \text{恒有} \\
& |f(x)-A|<\varepsilon
\end{array}
$$
- 7种情况
$$
\left\{\begin{array}{l}
\text{1. }x\rightarrow x_0\left\{\begin{array}{l}
x\rightarrow x_0\\
x\rightarrow x_0^+\\
x\rightarrow x_0^-\\
\end{array}\right.  \\
\text{2. }x\rightarrow\infty\left\{\begin{array}{l}
x\rightarrow \infty\\
x\rightarrow +\infty\\
x\rightarrow -\infty\\
\end{array}\right.  \\
\text{3. }n\rightarrow N(\varepsilon-N)
\end{array}\right.
$$
注：固定的两句定义为第一句和最后一句，即
$$
\begin{array}{l}
\forall\varepsilon>0  \\
\quad\vdots  \\
|f(x)-A|<\varepsilon
\end{array}
$$


- 极限存在的充要条件  
$$
\begin{array}{l}
\lim\limits_{x\to x_0}{f(x)}=A\ \Leftrightarrow\ \lim\limits_{x\to x_0^+}{f(x)}=\lim\limits_{x\to x_0^-}{f(x)}=A \\  
\lim\limits_{x\to x_0}{f(x)}=A\ \Leftrightarrow\ f(x)=A+\alpha(x),\ \lim\limits_{x\to x_0}{\alpha(x)}=0
\end{array}
$$
注：在第二行的描述中，$\alpha(x)$代表的是无穷小量，也是误差。可以通过移项表示具体式。在之后的<u>**已知某一极限，求另一极限**</u>中是一个普适解法思路。
> 例：如果$\lim\limits_{x\to 0}{\cfrac{x-\sin x+f(x)}{x^4}}$存在，求$\lim\limits_{x\to 0}{\cfrac{x^3}{f(x)}}\qquad$  
> 解：
$$
\begin{align}
\text{let }\lim\limits_{x\to 0}{\cfrac{x-\sin x+f(x)}{x^4}} &= A\text{ (constant)} \nonumber\\
\Rightarrow\quad\cfrac{x-\sin x+f(x)}{x^4} &= A+\alpha(x)\quad[\alpha(x)\to 0] \nonumber\\
\Rightarrow\quad f(x)&=x^4[A+\alpha(x)]+(\sin x-x)\nonumber\\
\lim\limits_{x\to 0}{\cfrac{f(x)}{x^3}} &=\lim\limits_{x\to 0}{x(A+\alpha(x))+\lim\limits_{x\to 0}{\cfrac{\sin x-x}{x^3}}} \nonumber\\
&=0-\frac{1}{6} \nonumber\\
&\Rightarrow \lim\limits_{x\to 0}{\cfrac{x^3}{f(x)}}=-6\nonumber
\end{align}
$$

### 函数极限的性质
#### 唯一性
#### <u>**局部**</u>有界性  
1. 极限存在只是函数局部有界的充分条件，而非必要条件
$$
\begin{array}{rcl}
\lim{f(x)}=A & \Rightarrow & |f(x)|\le M \\
& \nLeftarrow&  \\
\text{e.g. }f(x)=\sin x & & \sin x\le 1, \text{ but } \lim\sin x=\text{undefined}
\end{array}
$$
2. 若$f^\prime(x)$在有限区间$(a,b)$内有界，则$f(x)$在该区间有界(附证明)
$$
\begin{array}{rcl}
f(b)-f(a)&=&f^\prime(\xi)(b-a) \\
f(x)-f(x_0)&=&f^\prime(\xi)(x-x_0) \\
f(x)&=&f(x_0)+f^\prime(\xi)(x-x_0)\\
|a\pm b|\le|a|+|b| &\Rightarrow &f(x)=\Big|f(x_0)+f^\prime(\xi)(x-x_0)\Big|\le\Big|f(x_0)\Big|+\Big|f^\prime(\xi)(x-a)\Big| \\
&\Rightarrow & f(x)\le M\qquad (M\ \text{ is a constant)}
\end{array}
$$
- 证明函数有界(bounded)
$$
\left.\begin{array}{}
\lim\limits_{x\to a^+}{f(x)}=\text{constant}  \\
\lim\limits_{x\to b^-}{f(x)}=\text{constant}  \\
f(x)\text{ is continuous on the open interval (a, b)}
\end{array}\right\}\Rightarrow f(x)\text{ is bounded.}
$$

#### 局部保号性★  
注：与[数列极限性质](#性质)相同，其中局部保号性的证明恰好是数列极限[保号性推论2](#推论2重要)中的证明方法。 
证明：  
$\lim\limits_{x\to x_0}{f(x)}=A\ \Rightarrow\ \forall\varepsilon>0,\ \exists\delta>0,\ $当$0<|x-x_0|<\delta$, 恒有$|f(x)-A|<\varepsilon$
$$
\begin{array}{rc}
\Rightarrow  & -\varepsilon<f(x)-A<\varepsilon  \\
\Rightarrow  & A-\varepsilon<f(x)<A+\varepsilon \\
\text{let }  \varepsilon=\cfrac{A}{2}>0 \Rightarrow & f(x)>A-\varepsilon=\cfrac{A}{2}>0
\end{array}
$$

局部保号性原文：如果$\ f(x)\to A(x\to x_0)\ $，且$\ A>0(A<0)\ $，那么存在常数$\ \delta>0\ $，使得当$\ 0<|x-x_0|<\delta\ $时，有$\ f(x)>0\ $(或$\ f(x)<0\ $)

-------

局部保号性：如果$\ \lim\limits_{x\to x_0}{f(x)}=A\ $，且$\ A>0(A<0)\ $，那么存在常数$\ \delta>0\ $，使得当$\ 0<|x-x_0|<\delta\ $时，有$\ f(x)>0\ $(或$\ f(x)<0\ $)

```
局部保号性在1.5以及1.6费马定理证明中大放异彩
```

-------

#### 局部保号性推论(戴帽法)★
如果$(x\to x_0)$时$\ f(x)\ge 0\ $(或$\ f(x)\le 0\ $)，且$\ \lim\limits_{x\to x_0}{f(x)}=A\ $，则$\ A\ge 0(A\le 0)\ $
$$
\left.
\begin{array}{l}
f(x)\ge 0\quad / \quad f(x)\le 0    \\
\lim\limits_{x\to x_0}{f(x)}=A
\end{array}
\right\}\Rightarrow
\ A\ge 0(A\le 0)\ 
$$

- 戴帽法再拓展：广义化

将$\ 0\ $替换为任意常数$\ c\ $
$$
\left.
\begin{array}{l}
f(x)\ge c\quad / \quad f(x)\le c    \\
\lim\limits_{x\to x_0}{f(x)}=A
\end{array}
\right\}\Rightarrow
\ A\ge c(A\le c)\ 
$$

```
与数列戴帽法一样，脱帽无等号，戴帽有等号！
```


### 极限运算规则

### 夹逼准则(函数)
注意： 
$$
\left.\begin{array}{}
\varphi(x)\le f(x)\le g(x) \\
\lim\limits_{x\to\infty}{[g(x)-\varphi(x)]}=0
\end{array}\right\} {\color{red}\nRightarrow \lim\limits_{x\to\infty}{f(x)}\ =\text{ exist.}}
$$

### 洛必达法则
$$
\begin{array}{rcl}
\lim\limits_{x\to\cdot}{\cfrac{f(x)}{F(x)}}&\overset{0/0\text{ or }\infty/\infty}{===}&\lim\limits_{x\to\cdot}{\cfrac{f^\prime(x)}{F^\prime(x)}} \\
A & \Leftarrow & A \\
\infty & \Leftarrow & \infty \\
\left\{\begin{array}{l}
\text{exist} \\
\text{undefined}
\end{array}\right.
& \color{red}\nLeftarrow & \text{undefined}
\end{array}
$$
```
洛必达是一个结果反推过程的法则！
```

典型反例：
$$
\begin{array}{l}
\text{correct answer: } & \lim\limits_{x\to 0}{\cfrac{x^2\cdot\sin{\cfrac{1}{x}}}{x}}=\lim\limits_{x\to 0}{x\cdot\sin\cfrac{1}{x}}=0 \\
\text{wrong solution: } & \lim\limits_{x\to 0}{\cfrac{x^2\cdot\sin{\cfrac{1}{x}}}{x}}=\lim\limits_{x\to 0}{\Big(2x\cdot\sin\cfrac{1}{x}-\cos\cfrac{1}{x}\Big)}=\text{undefined}
\end{array}
$$

### Taylor公式
#### 常用泰勒公式
$$
\begin{aligned}
\mathrm{e}^x &= \sum\limits_{n=0}^{\infty}{\cfrac{x^n}{n!}}\\
&=1+x+\cfrac{x^2}{2}+\cfrac{x^3}{6}+o(x^3)  \\
\sin x &= \sum\limits_{n=0}^{\infty}{\cfrac{(-1)^n}{(2n+1)!}x^{2n+1}}\\
&=x-\cfrac{x^3}{6}+o(x^3)  \\
\cos x &= \sum\limits_{n=0}^{\infty}{\cfrac{(-1)^n}{(2n)!}x^{2n}}\\
&=1-\cfrac{x^2}{2}+\cfrac{x^4}{24}+o(x^4)  \\
\ln{(1+x)} &= \sum\limits_{n=0}^{\infty}{\cfrac{(-1)^n}{n+1}x^{n+1}}\\
&=x-\cfrac{1}{2}x^2+\cfrac{1}{3}x^3+o(x^3)  \\
(1+x)^k &=1+\sum\limits_{n=1}^{\infty}{\cfrac{k(k-1)\cdots(k-n+1)} {n!}x^n}=1+\sum\limits_{n=1}^{\infty}{\cfrac{\mathrm{A}_n^k}{n!}}x^n\\
&=1+kx+\cfrac{k(k-1)}{2!}x^2+o(x^2)    \\
\tan x &= x + \cfrac{1}{3}x^3 + o(x^3)  \\
\arctan x &= x - \cfrac{1}{3}x^3 + o(x^3)  \\
\arcsin x &= x + \cfrac{1}{6}x^3 + o(x^3)  \\
(1+x)^k-1 &\sim kx\quad (x\to 0)
\end{aligned}
$$


#### 展开到几次幂
- $\cfrac{A}{B}$型，<u>**上下同阶**</u>原则  
```
A/B是除法，但乘法也可转换成除法，比如M×N=M/(N^-1)
```

- $A-B$型，<u>**幂次最低**</u>原则★  
将$A,B$分别展开到它们的系数不相等的$x$的最低次幂为止
```
A-B是减法，但也可以转换成加法，比如M-N=M-(-N)
```
  - 典型例子
$$
\begin{array}{l}
\begin{array}{lrrr}
\text{1.} & x-\sin x \\
& x =&x^1 &+& 0\cdot x^3 \\
& \sin x  = &x^1 &+& \Big(-\cfrac{1}{6}\Big)x^3 &+\ o(x^3) \\
\end{array}\\
\begin{array}{l}
&\Rightarrow \quad x-\sin x\sim \cfrac{1}{6}x^3
\end{array} \\
\begin{array}{lrrl}
\text{2.} & x+\sin x \\
& x =&x^1&\\
& -\sin x  = &-x^1&+o(x^1) \\
\end{array}\\
\begin{array}{l}
&\Rightarrow & x+\sin x\sim 2x \\
&\text{tips:}& \bbox[yellow]{x+\sin x=x-(-\sin x)}
\end{array}
\end{array}
$$

#### Taylor公式例题
>例：
$$
\begin{align}
&\lim\limits_{x\to 0}{\cfrac{\sin^2x-x^2}{\mathrm{e}^{x^4}-1}}\nonumber\\
=&\lim\limits_{x\to 0}{\cfrac{(\sin x+x)(\sin x-x)}{\mathrm{e}^{{(x^2)}^2}-1}}\nonumber\\
=&\lim\limits_{x\to 0}{\cfrac{2x\cdot\big(-\cfrac{x^3}{6}\big)}{x^4}}\nonumber\\
=&-\cfrac{1}{3}\nonumber
\end{align}
$$

### 海涅定理(归结原则)
$$
\begin{array}{l}
&\lim\limits_{x\to x_0}{f(x)}=A \quad\Leftrightarrow  \\
&\forall\{x_n\}\to x_0,\ \lim\limits_{n\to\infty}{f(x_n)}=A  \\
\text{1. }&\Leftarrow  \quad\text{often used to negate.(by counterexamples)}\\
\text{2. }&\Rightarrow \quad\text{often used to calculate.}\\
\end{array}
$$

对于第一种情况，即向左举反例证明极限不存在。
>e.g.  证明$\lim\limits_{x\to 0}{\cfrac{1}{x}\sin\cfrac{1}{x}}$不存在
$$
\begin{array}{l}
& f(x)=\cfrac{1}{x}\sin\cfrac{1}{x} \\
\text{1. }& \text{let }x_n=\cfrac{1}{n\pi} \\
&\lim\limits_{n\to\infty}{x_n}=n\pi\sin(n\pi)=0  \\
\text{2. }& \text{let }x_n=\cfrac{1}{\big(2n+\cfrac{1}{2}\big)\pi}\\
&\lim\limits_{n\to\infty}{x_n}=\big(2n+\cfrac{1}{2}\big)\pi\sin\cfrac{\pi}{2}=\infty\\
&0\ne\infty\Rightarrow\lim\limits_{x\to 0}{\cfrac{1}{x}\sin\cfrac{1}{x}}\text{ doesn't exist.}
\end{array}
$$

对于第二种情况，即计算极限。
>e.g.  $\lim\limits_{n\to\infty}{\big(n\tan\cfrac{1}{n}\big)^{n^2}}$
$$
\begin{array}{l}
&f(x_n)=\big(n\tan\cfrac{1}{n}\big)^{n^2}  \\
&\text{let }x_n=\cfrac{1}{n} \qquad(x_n\to 0)  \\
\Rightarrow & f\big(\cfrac{1}{n}\big)=\big(n\tan\cfrac{1}{n}\big)^{n^2}\Rightarrow f(x)=\big(\cfrac{\tan x}{x}\big)^{1/x^2}  \\
&
\begin{align}
\lim\limits_{x\to 0}{f(x)}&=\lim\limits_{x\to 0}{\big(\cfrac{\tan x}{x}\big)^{1/x^2}}\nonumber\\
&=\lim\limits_{x\to 0}{\mathrm{e}^{\frac{1}{x^2}\ln{\frac{\tan x}{x}}}}\nonumber\\
\lim\limits_{x\to 0}{\frac{1}{x^2}\ln{\frac{\tan x}{x}}}&=\lim\limits_{x\to 0}{\frac{1}{x^2}\ln{\big[1+(\frac{\tan x}{x}}-1)\big]}\nonumber\\
&=\lim\limits_{x\to 0}{\frac{1}{x^2}\cdot\big(\frac{\tan x}{x}}-1\big)\nonumber\\
&=\lim\limits_{x\to 0}{\frac{\frac{1}{3}x^3}{x\cdot x^2}}\nonumber\\
&=\frac{1}{3}\nonumber\\
&\Rightarrow\lim\limits_{x\to 0}{f(x)}=\lim\limits_{x\to 0}{\big(\cfrac{\tan x}{x}\big)^{1/x^2}}=\mathrm{e}^{1/3}\nonumber
\end{align}\\
\Rightarrow & \lim\limits_{n\to\infty}{\big(n\tan\cfrac{1}{n}\big)^{n^2}}=\mathrm{e}^{1/3}
\end{array}
$$

### 无穷小比阶(★经典笔记)   
#### 一个扩展结论 
$x\to x_0\ $时，$f(x)\to 0,g(x)\to 0\quad\Rightarrow\quad\mathrm{e}^{f(x)}-\mathrm{e}^{g(x)}\sim f(x)-g(x)$   

- 广义化扩展：
$x\to x_0\ $时，$f(x)\to 0,g(x)\to 0\quad\Rightarrow\quad a^{f(x)}-b^{g(x)}\sim f(x)\ln a-g(x)\ln b$  

>例题：已知$a>0,\ b>0$，求$\lim\limits_{x\to +\infty}{x(a^\frac{1}{x}-b^\frac{1}{x})}$
解答：$\lim\limits_{x\to +\infty}{x(a^\frac{1}{x}-b^\frac{1}{x})}=\lim\limits_{t\to 0^+}{\cfrac{a^t-b^t}{t}}=\lim\limits_{t\to 0^+}{\cfrac{t\ln a-t\ln b}{t}}=\ln\cfrac{a}{b}$

- 简要证明这个结论的正确性
    - 证明1：
    $$
    \mathrm{e}^{f(x)}-\mathrm{e}^{g(x)}=\mathrm{e}^{g(x)}(\mathrm{e}^{f(x)-g(x)}-1)
    $$
    - 证明2：
    $$
    \mathrm{e}^{f(x)}-\mathrm{e}^{g(x)}=(\mathrm{e}^{f(x)}-1)-(\mathrm{e}^{g(x)}-1)
    $$
    注：拆分的可行性在于拆分后的两部分极限分别存在，所以成立。

#### 等价无穷小与极限计算的扩展
扩展1：    
例如，我们知道，$x\to 0,\quad\ln{(1+x)\sim x}$
如果直接“翻转”$\ x(\text{ let }t=\cfrac{1}{x})$，得到$x\to\infty,\quad\ln{\big(1+\cfrac{1}{x}\big)}\sim\cfrac{1}{x}$     

这种做法，虽然结果上是正确的，但是实际上属于结果反推结论的推断，可能会出错。  
正确的推导方式应该是这样的：  
>$x\to 0,\quad\ln{(1+x)\sim x}$，用$\cfrac{1}{x}$替换$x$，则有  
>$\cfrac{1}{x}\to 0,\quad\ln{(1+\cfrac{1}{x})\sim \cfrac{1}{x}}$   
>$\Rightarrow x\to\infty,\quad\ln{\big(1+\cfrac{1}{x}\big)}\sim\cfrac{1}{x}$  
>顺带记住这个结论:   
$$
x\to\infty, \quad \ln{\big(1+\cfrac{1}{x}\big)}=\ln{\cfrac{x+1}{x}}\sim \cfrac{1}{x}
$$

在实际使用中，可以这样应用   
应用举例：当做题时做到中间步骤需要知道$\lim\limits_{t\to\ -\infty}{\ln{(1+\mathrm{e}^t)}}$，此时凭直觉想代换为$\sim \mathrm{e}^t$，只需要试一下$\mathrm{e}^t\to 0$时，反解出的$\ t\ $是否趋于$\ -\infty\ $，验证成立即可直接代换。  


-------

扩展2：   
例题：计算$\lim\limits_{x\to +\infty}{\cfrac{\ln(2^x+1)}{x}}$    
答案：
$$
\begin{array}{rl}
\lim\limits_{x\to +\infty}{\cfrac{\ln(2^x+1)}{x}} &=\lim\limits_{x\to +\infty}{\cfrac{\ln[2^x(1+2^{-x})]}{x}} \\
&=\lim\limits_{x\to +\infty}{\cfrac{\ln{2^x}+\ln(1+2^{-x})}{x}} \\
&=\lim\limits_{x\to +\infty}{\cfrac{x\ln2+0}{x}} \\
&=\ln 2
\end{array}
$$
```
本题提出了一个之前没讲过的极限计算，实质上还是在”凑”。
因为x趋于+∞，所以要提出2^x使得括号内出现1+0
```

-------
通过扩展1和扩展2，我们可以得到关于$\ \ln{(1+2^x)}\ $的处理方法：  
$$
\ln{(1+2^x)}
\left\{\begin{array}{l}
x\to +\infty & =\ln{2^x(1+2^{-x})}=x\ln 2+\ln{(1+2^{-x})}=x\ln 2 \\
x\to -\infty & \sim 2^x
\end{array}\right.
$$

-------


扩展3：    
例题：若$\lim\limits_{x\to 0}{\cfrac{\sin x(\cos x-b)}{e^x-a}}=5,\quad a=\quad b=$  
解答：由于分子$\lim\limits_{x\to 0}{\sin x(\cos x-b)}=0$，**若要<u>整体极限</u>为一个常数**，只能**使分母也趋于0**，  
所以可以得到$\lim\limits_{x\to 0}{(e^x-a)}=0\quad\Rightarrow\quad a=1$  
这样可以得到原式$=\lim\limits_{x\to 0}{\cfrac{\sin x(\cos x-b)}{e^x-1}}=\lim\limits_{x\to 0}{\cfrac{x(1-b)}{x}}=5\quad\Rightarrow\quad b=-4$    
```
极限判断的时候，若分子已为0，整体极限却已知为一常数，则使分母也趋于0
```


-------

扩展4：    
例题：计算$\lim\limits_{n\to\infty}{\sqrt[n]{1+2^n+3^n}}$    

方法一：    
$$
\begin{align}
 & \lim\limits_{n\to\infty}{\sqrt[n]{1+2^n+3^n}} \nonumber\\
=& \lim\limits_{n\to\infty}{\sqrt[n]{\frac{3^n(1+2^n+3^n)}{3^n}}} \nonumber\\
=& 3\times\lim\limits_{n\to\infty}{\sqrt[n]{1+\Big(\frac{1}{3}\Big)^n+\Big(\frac{2}{3}\Big)^n}}\nonumber\\
=& 3\times (1^0)=3 \nonumber\\
\end{align}
$$

方法二：夹逼定理    
$$
\begin{array}{c}
\sqrt[n]{0+0+3^n}\le \sqrt[n]{1+2^n+3^n}\le \sqrt[n]{3^n+3^n+3^n} \\
\sqrt[n]{3^n}\le \sqrt[n]{1+2^n+3^n}\le \sqrt[n]{3\times 3^n} \\
\lim\limits_{n\to\infty}{\sqrt[n]{3^n}}\le \lim\limits_{n\to\infty}{\sqrt[n]{1+2^n+3^n}}\le \lim\limits_{n\to\infty}{\sqrt[n]{3\times 3^n}} \\
\text{Left }=\text{Right }=3 \\
\lim\limits_{n\to\infty}{\sqrt[n]{1+2^n+3^n}}=3
\end{array}
$$


-------

扩展5：    
例题：计算$\lim\limits_{x\to 0}{\Big(\cfrac{\mathrm{e}^x+x\mathrm{e}^x}{\mathrm{e}^x-1}-\cfrac{1}{x}\Big)}$  
解答：
$$
\begin{align}
 & \lim\limits_{x\to 0}{\Big(\cfrac{\mathrm{e}^x+x\mathrm{e}^x}{\mathrm{e}^x-1}-\cfrac{1}{x}\Big)} \nonumber \\
=& \lim\limits_{x\to 0}{\cfrac{x\mathrm{e}^x(x+1)-\mathrm{e}^x+1}{x(\mathrm{e}^x-1)}} \tag{*} \\
=& \lim\limits_{x\to 0}{\cfrac{1-\mathrm{e}^x+x\mathrm{e}^x+x^2\mathrm{e}^x}{x^2}} \nonumber \\
\end{align}
$$

由于$\mathrm{e}^x=1+x+\cfrac{x^2}{2}+o(x^2)$  
所以分子中$1-\mathrm{e}^x+x\mathrm{e}^x+x^2\mathrm{e}^x$这四项，可以直接按次数展开，即
$$
\left\{
\begin{array}{rcr}
1-\mathrm{e}^x   &=&  -x   & -\cfrac{1}{2}x^2 & +o(x^2)\\
x\mathrm{e}^x    &=&   x   & +x^2             & +o(x^2)  \\
x^2\mathrm{e}^x  &=&       &  x^2             & +o(x^2)  \\
\end{array}\right.
$$
加和，得到分子为$\cfrac{3x^2}{2}+o(x^2)$，所以$\lim\limits_{x\to 0}{\Big(\cfrac{\mathrm{e}^x+x\mathrm{e}^x}{\mathrm{e}^x-1}-\cfrac{1}{x}\Big)}=\cfrac{3}{2}$
注意步骤中(*)这一步，不可以直接带入分子中$\ \mathrm{e}^x\ $在$x\to 0\ $时的值，因为会破坏分子这一”块”的完整性。    


-------
扩展6：  
例题：计算$\lim\limits_{n\to\infty}{\big[\sqrt{n}(\sqrt{n+1}-\sqrt{n})+\cfrac{1}{2}\big]^{8n}}$

本题在于**辨别形式**，是$\ \lim{u^v}\ $形，但凡能算出常数，那么只有可能是$\ 0^\infty\ $或$\ 1^\infty\ $形。  
又因为底数$\ u\ $中含有$\ +\cfrac{1}{2}\ $，因此可以顺便**直接推断**出$\lim\limits_{n\to\infty}{\sqrt{n}(\sqrt{n+1}-\sqrt{n})}=\cfrac{1}{2}$  

利用$\ 1^\infty\ $公式$\lim{u^v}=\mathrm{e}^{\lim{(u-1)v}}$，所以原式$=\mathrm{e}^{\,\lim\limits_{n\to\infty}{8n\big[\sqrt{n}(\sqrt{n+1}-\sqrt{n})-\frac{1}{2}\big]}}$  


计算$\lim\limits_{n\to\infty}{8n\big[\sqrt{n}(\sqrt{n+1}-\sqrt{n})-\cfrac{1}{2}\big]}=$

Taylor公式  
$\begin{aligned}(1+x)^k &=1+\sum\limits_{n=1}^{\infty}{\cfrac{k(k-1)\cdots(k-n+1)} {n!}x^n}=1+\sum\limits_{n=1}^{\infty}{\cfrac{\mathrm{A}_n^k}{n!}}x^n\\&=1+kx+\cfrac{k(k-1)}{2!}x^2+o(x^2)\end{aligned}$

使用Taylor公式，$8n\big[\sqrt{n}(\sqrt{n+1}-\sqrt{n})-\cfrac{1}{2}\big]$中出现$(\sqrt{n}\sqrt{n+1}-n-\cfrac{1}{2})$，如果直接套用$\ (1+x)^k\ $的公式对$\sqrt{n^2+n}$进行拼凑，那么提出$\sqrt{n}$显然是没有意义的，因为化简前$\sqrt{n}\ $就在括号前。所以考虑提出$\sqrt{n^2}$使得这一式子变为$\sqrt{1+\frac{1}{n}}$更为合理。  
所以$(\sqrt{n}\sqrt{n+1}-n-\cfrac{1}{2})=n(\sqrt{1+\frac{1}{n}}-1-\cfrac{1}{2n})$，此时利用Taylor公式$[1+f(x)]^k$，展开时考虑整个式子外边有一个$8n^2$，即$8n^2(\sqrt{1+\frac{1}{n}}-1-\cfrac{1}{2n})$，所以展开时内部展开到$\cfrac{1}{n^2}$为止。
$\begin{aligned}&\lim\limits_{n\to\infty}{8n\big[\sqrt{n}(\sqrt{n+1}-\sqrt{n})-\cfrac{1}{2}\big]}=\lim\limits_{n\to\infty}{8n^2(\sqrt{1+\frac{1}{n}}-1-\cfrac{1}{2n})}\\=&\lim\limits_{n\to\infty}{8n^2\big[(1+2n+\cfrac{\frac{1}{2}(\frac{1}{2}-1)}{2}\cdot\cfrac{1}{n^2}+o(\cfrac{1}{n^2}))-1-\cfrac{1}{2n}\big]}\\=&\lim\limits_{n\to\infty}{8n^2[-\cfrac{1}{8n^2}+o(\cfrac{1}{n^2})]}=-1\end{aligned}$  
所以原式答案$\lim\limits_{n\to\infty}{\big[\sqrt{n}(\sqrt{n+1}-\sqrt{n})+\cfrac{1}{2}\big]^{8n}}=\mathrm{e}^{-1}$


-------

通过扩展3~扩展6，需要注意两点：
1. 极限计算的第一步应该是<u>代入法进行试计算</u>，得到结果如果是常数，就直接得到极限计算结果；如果出现七种未定式，则继续根据情况解题。
2. 因为出题基本上只会出不定式，所以反而可以根据不定式的极限为常数反推是哪一种不定式(扩展6)
3. 遇到未定式时，不可以随意破坏式子的完整性。



### 未定式的计算  
注意$\infty^0$与$1^\infty$的不同解法  
- $\infty^0$  

$$
\lim{u^v}=\mathrm{e}^{\lim{v\ln{u}}}
$$

解释证明：
$$
\begin{aligned}
u^v  &= \mathrm{e}^{\ln{u^v}} \\
     &= \mathrm{e}^{v\ln u}\\
\end{aligned}
$$

例题：$\lim\limits_{x\to +\infty}{(x+\sqrt{1+x^2})^\frac{1}{x}}$   
提示：$\ln{(x+\sqrt{1+x^2})}=\ln{(1+\sqrt{\cfrac{1+x^2}{x^2}})}$  
答案：$1$  

- $1^\infty$  
$$
\lim{u^v}=\mathrm{e}^{\lim{(u-1)v}}
$$

解释证明：

$$
\begin{aligned}
u^v  &= [1+(u-1)]^v \\
     &= [[1+(u-1)]^{\frac{1}{u-1}}]^{(u-1)v} \\
     &= \mathrm{e}^{\ln{[[1+(u-1)]^{\frac{1}{u-1}}]^{(u-1)v}}} \\
     &= \mathrm{e}^{(u-1)v\ln{[[1+(u-1)]^{\frac{1}{u-1}}]}} \\
\lim\limits_{x\to\infty}{(1+\frac{1}{x})^x}=\mathrm{e}\quad &\Rightarrow \quad \lim\limits_{(u-1)\to\ 0}{[1+(u-1)]^{\frac{1}{u-1}}} =\mathrm{e} \\
\ln\mathrm{e}=1\quad&\Rightarrow\quad\lim\limits_{(u-1)\to 0}{\mathrm{e}^{(u-1)v\ln{[[1+(u-1)]^{\frac{1}{u-1}}]}}}  \\
&=\lim\limits_{(u-1) \to 0}{\mathrm{e}^{(u-1)v}}  \\
&=\mathrm{e}^{\lim{(u-1)v}}
\end{aligned}
$$

注：$\ 1^\infty\ $这类计算，之所以可以使用$\ \mathrm{e}^{\lim{(u-1)v}}\ $这个公式，正是因为其中的$(u-1)\to 0$才成立，即$\ u^v\ $中的$\ u\ $是$\ 1^\infty\ $的$\ 1\ $，这样$\ u-1\ $自然趋于$\ 0\ $  

例题：设$\lim\limits_{x\to \infty}{\big(\cfrac{x+2a}{x-a}\big)^x}=8$，求$a$    

答案：$\ln 2$


-------

扩展：$\ 1^\infty-1^\infty\ $  

转换为$\quad\mathrm{e}^f-\mathrm{e}^g=\mathrm{e}^g(\mathrm{e}^{f-g}-1)$


### 连续与间断   
```
注意绝对值的处理。
```
### 第三讲特辑
#### 忘掉技巧  
例题： $\lim\limits_{x\to -\infty}{\cfrac{\sqrt{4x^2+x-1}+x+1}{\sqrt{x^2+\sin x}}}$  
解答：
$$
\begin{align}
\lim\limits_{x\to -\infty}{\cfrac{\sqrt{4x^2+x-1}+x+1}{\sqrt{x^2+\sin x}}} &= \lim\limits_{t\to +\infty}{\cfrac{\sqrt{4t^2-t-1}-t+1}{\sqrt{t^2-\sin t}}} \nonumber\\
 &= \lim\limits_{t\to +\infty}{\cfrac{3t^2+t-2}{\sqrt{t^2-\sin t}(\sqrt{4t^2-t-1}+t-1)}} \tag{1}\\
 &= \lim\limits_{t\to +\infty}{\cfrac{3+\cfrac{1}{t}-\cfrac{2}{t^2}}{\sqrt{1-\cfrac{\sin t}{t^2}}\Big(\sqrt{4-\cfrac{1}{t}-\cfrac{1}{t^2}}+1-\cfrac{1}{t}\Big)}} \tag{2}\\
 &= 1  \nonumber\\
\end{align}
$$
注意：(1)到(2)这一步，的确是分母除了$t^2$，例如
$$
\begin{align}
\cfrac{3t^2}{\sqrt{t^2+1}(t+1)} &= \cfrac{3}{\cfrac{1}{t^2}(\sqrt{t^2+1})(t+1)} \nonumber\\
&= \cfrac{3}{\cfrac{\sqrt{t^2+1}}{t}\cdot\cfrac{t+1}{t}} \tag{correct}\\
&= \cfrac{3}{\sqrt{\cfrac{t^2+1}{t^4}}\cdot(t+1)} \tag{correct}\\
&= \cfrac{3}{\sqrt{\cfrac{t^2+1}{t^4}}\cdot\cfrac{t+1}{t^2}} \tag{WRONG}\\
\end{align}
$$

```
不要陷入思维定势，有的题目不一定非要用泰勒公式或者洛必达！
另外，不要被根式搞糊涂了，上下同除注意别多除！
```
#### 有趣的例子
例1：$\lim\limits_{n\to\infty}{(1+x)(1+x^2)(1+x^4)\cdots(1+x^{2^n})}\quad |x|<1$  
解答：
$$
\begin{aligned}
  & \lim\limits_{n\to\infty}{(1+x)(1+x^2)(1+x^4)\cdots(1+x^{2^n})}\quad |x|<1 \\
= & \lim\limits_{n\to\infty}{\cfrac{(1-x)(1+x)(1+x^2)(1+x^4)\cdots(1+x^{2^n})}{1-x}}\\
= & \lim\limits_{n\to\infty}{\cfrac{(1-x^2)(1+x^2)(1+x^4)\cdots(1+x^{2^n})}{1-x}}\\
= & \cdots  \\
= & \lim\limits_{n\to\infty}{\cfrac{1-(x^{2^n})^2}{1-x}} \\
= & \cfrac{1}{1-x}  \quad |x|<1 
\end{aligned}
$$

-------

例2：$\quad n\in\mathbb{N}_+,\ a\in\mathbb{R},\ a\ne 0,\ \lim\limits_{x\to +\infty}{\cfrac{x^{30}}{x^n-(x-2)^n}}=\cfrac{1}{a}\quad n=\quad a=$    

答案：$\quad n=31\quad a=-\mathrm{C}_{31}^{30}x^{30}(-2)^1=60$ 

-------

例3：已知$\lim\limits_{x\to\infty}{f(x)}=2$，求$\lim\limits_{x\to\infty}{\displaystyle\int_{x}^{x+2}{f(t)\cdot t\sin\cfrac{3}{t}}\mathrm{d}t}$  
解答：$\lim\limits_{t\to\infty}{t\sin\cfrac{3}{t}}=\lim\limits_{u\to 0}{\cfrac{\sin 3u}{u}}=3\lim\limits_{u\to 0}{\cfrac{\sin 3u}{3u}}=3$  
又由于$\lim\limits_{x\to\infty}{f(x)}=2$，所以$\lim\limits_{t\to\infty}{f(t)\cdot t\sin\cfrac{3}{t}}=6$  
根据定积分的面积性质，则原式$=6\times 2=12$

-------

例4：关于$x^n$、$\sin (x^n)$、$(\sin x)^n$的大小比较  
$$
\begin{array}{ll|l}
& \lim\limits_{x\to 0}{\cfrac{(\sin x)^n}{x^n}}=\lim\limits_{x\to 0}{\Big(\cfrac{\sin x}{x}\Big)^n}=1 & x^n>(\sin x)^n \quad [x>0]\\
& \lim\limits_{x\to 0}{\cfrac{\sin (x^n)}{x^n}}=1 & \text{Taylor Series }\sin x=x-\cfrac{x^3}{6}+\cdots\\
\Rightarrow & \lim\limits_{x\to 0}{\cfrac{(\sin x)^n}{\sin (x^n)}}=1\\
\end{array}
$$

## 第四讲 一元函数微分学的概念和计算
### 导数的定义
$$
\begin{array}{l}
f^\prime(x)=\lim\limits_{\Delta x\to 0}{\cfrac{f(x+\Delta x)-f(x)}{\Delta x}}\\
f^\prime(x)=\lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{x-x_0}}\\
\end{array}
$$

#### 除乘技巧
- 由导数存在证明函数连续   
函数连续：$\lim\limits_{\Delta x\to 0}{f(x+\Delta x)}=f(x)$  
导数存在：$f^\prime(x)=\lim\limits_{\Delta x\to 0}{\cfrac{f(x+\Delta x)-f(x)}{\Delta x}}=A$  
证明： 
$$
\begin{array}{ll}
& \lim\limits_{\Delta x\to 0}{\cfrac{f(x+\Delta x)-f(x)}{\Delta x}}=A \\
& \lim\limits_{\Delta x\to 0}{\Delta x\cdot \Big(\cfrac{f(x+\Delta x)-f(x)}{\Delta x}\Big)}=A\cdot 0=0 \\
\Rightarrow & \lim\limits_{\Delta x\to 0}{\big[f(x+\Delta x)-f(x)\big]}=0 \\
\Rightarrow & \lim\limits_{\Delta x\to 0}{f(x+\Delta x)}=f(x)
\end{array}
$$
- 一个扩展结论**（重要！）**   
若$f(x)$在$x=x_0$连续，且$\lim\limits_{x\to x_0}{\cfrac{f(x)}{x-x_0}}=A$，则$f(x_0)=0,\quad f^\prime(x)=A$  
证明： 
$$
\begin{array}{}
            & \lim\limits_{x\to x_0}{\cfrac{f(x)}{x-x_0}}=A \\
\Rightarrow & \lim\limits_{x\to x_0}{\big[\cfrac{f(x)}{x-x_0}\cdot (x-x_0)\big]}=A\cdot 0=f(x_0)=0\\
\Rightarrow & \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{x-x_0}}=\lim\limits_{x\to x_0}{\cfrac{f(x)}{x-x_0}}=f^\prime(x_0)=A
\end{array}
$$
- 除乘技巧例题  
例题1：设$\ \delta>0,f(x)\ $在$\ [-\delta,\delta]\ $上有定义，$f(0)=1\ $，且满足
$$
\lim\limits_{x\to 0}{\cfrac{\ln{(1-2x)+2xf(x)}}{x^2}}=0
$$
证明：$f(x)$在$\ x=0\ $处可导，并求出$f^\prime(0)$     
证明：     
直接法
$$
\begin{aligned}
0= & \lim\limits_{x\to 0}{\cfrac{\ln{(1-2x)+2xf(x)}}{x^2}} \\
0=& \lim\limits_{x\to 0}{\cfrac{(-2x)-\cfrac{1}{2}(-2x)^2+o(x^2)+2xf(x)}{x^2}} \\
0=& \lim\limits_{x\to 0}{\cfrac{(-2x)-\cfrac{1}{2}(-2x)^2+o(x^2)+2xf(x)}{x^2}} \\
0=& \lim\limits_{x\to 0}{\cfrac{2f(x)-2-2x}{x}} \\
0=& 2\lim\limits_{x\to 0}{\cfrac{f(x)-1}{x-0}}-2 \\
\Rightarrow & \lim\limits_{x\to 0}{\cfrac{f(x)-1}{x-0}}=1 \\ 
\end{aligned}
$$
凑法
$$
\begin{array}{rcl}
f^\prime(0) & = & \lim\limits_{x\to 0}{\cfrac{f(x)-f(0)}{x-0}}
=\lim\limits_{x\to 0}{\cfrac{f(x)-1}{x}} \\
            & = & \lim\limits_{x\to 0}{\cfrac{2xf(x)-2x}{2x^2}}
              =   \cfrac{1}{2}\lim\limits_{x\to 0}{\cfrac{2xf(x)-2x}{x^2}} \\
\ln{(1-2x)} & = & (-2x)-\cfrac{(-2x)^2}{2}+o(x^2)   \\
-2x         & = & \ln{(1-2x)}+2x^2+o(x^2)   \\
f^\prime(0) & = & \cfrac{1}{2}\lim\limits_{x\to 0}{\cfrac{\ln{(1-2x)}+2xf(x)+2x^2+o(x^2)}{x^2}} \\
            & = & \cfrac{1}{2}(0+2+0)=1
\end{array}
$$

例题2：设$\ f(x)\ $满足$\ f(0)=0\ $，且$\ f^\prime(0)\ $存在，求$\lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})}{\ln{(1-x\sin x)}}}$    

答案：
$$
\begin{array}{rcl}
f^\prime(0) &=& \lim\limits_{x\to 0}{\cfrac{f(x)-f(x)}{x-0}}
             =  \lim\limits_{x\to 0}{\cfrac{f(x)}{x}}   \\
            &=& \lim\limits_{1-\sqrt{\cos x}\to 0}{\cfrac{f(1-\sqrt{\cos x})}{1-\sqrt{\cos x}}}
             =  \lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})}{1-\sqrt{\cos x}}} \\
            &=& \lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})(1+\sqrt{\cos x})}{(1-\sqrt{\cos x})(1+\sqrt{\cos x})}}
             =  \lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})(1+\sqrt{\cos x})}{1-\cos x}}    \\
            &=& \lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})\cdot 2}{\frac{1}{2}x^2}}     
             =  4\lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})}{x^2}} \\
\end{array}\\
$$
由于已知
$$
\lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})}{\ln{(1-x\sin x)}}}
        =\lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})}{-x^2}}\\
$$
对比两式
$$
\begin{array}{rcl}
\lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})}{\ln{(1-x\sin x)}}}
        &=&\lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})}{-x^2}}\\
f^\prime(0)&=&4\lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})}{x^2}}\\
\Rightarrow\quad\lim\limits_{x\to 0}{\cfrac{f(1-\sqrt{\cos x})}{\ln{(1-x\sin x)}}}&=&-\cfrac{1}{4}f^\prime(0)
\end{array}
$$

### 一元函数的微分
#### 微分的概念
三个基本式子  
$$
\begin{align}
\Delta x    &=\mathrm{d}x \nonumber \\
\Delta y    &=y^\prime(x)\Delta x+o(\Delta x) \nonumber \\
\mathrm{d}y &=y^\prime(x)\mathrm{d}x \nonumber \\
\end{align}
$$
其中，$\Delta y=y^\prime(x)\Delta x+o(\Delta x)$中的$[y^\prime(x)\Delta x]$又称为<u>**线性主部**</u>      
另外，$\Delta y \ne \mathrm{d}y$，中间差了关于$\Delta x$的高阶无穷小$o(\Delta x)$

通过函数图像理解一元函数可微：

![](media/Differentiation.jpg)

例题：设函数$f(u)$可导，且$y=f(x^2)$，当自变量$\ x\ $在$\ x=-1\ $处取得增量$\Delta x=-0.1$时，相应的函数增量$\ \Delta y\ $的线性主部为$\ 0.1$，则$f^\prime(1)=$   
答案：$0.5$    
分析：
$$
\begin{array}{rrcl}
&\Delta y    &=&y^\prime(x)\Delta x+o(\Delta x) \\
\Rightarrow & \quad 0.1 &=&y^\prime(-1)(-0.1) \\
\Rightarrow & \quad y^\prime(-1)  &=&-1  \\
& y^\prime(x)&=&[f(x^2)]^\prime\quad =\quad 2xf^\prime(x^2) \\
\Rightarrow & y^\prime(-1)&=&-2f^\prime(1) \\
\Rightarrow & f^\prime(1)&=&-\frac{1}{2}y^\prime(-1)\quad =\quad \frac{1}{2}
\end{array}
$$
注意$\ [f(x^2)]^\prime\ $与$\ f^\prime(x^2)\ $的区别：
例如，设$\ f(x)=\mathrm{e}^{2x}-x\ $
$$
\begin{array}{l}
f^\prime(x)     &=  2\mathrm{e}^{2x}-1          \\
f(x^2)          &=   \mathrm{e}^{2x^2}-x^2      \\
[f(x^2)]^\prime &= 4x\mathrm{e}^{2x^2}-2x       \\
f^\prime(x^2)   &=  2\mathrm{e}^{2(x^2)}-1      \\
\end{array}
$$
注：其中$\ f^\prime(x^2)\ $就是把$\ f^\prime(x)\ $中的$\ x\ $替换为了$\ x^2\ $
### Chain rule (链式法则)
$$
\cfrac{\mathrm{d}}{\mathrm{d}x}[f(g)]=\cfrac{\mathrm{d}}{\mathrm{d}g}[f(g)]\times\cfrac{\mathrm{d}}{\mathrm{d}x}g(x)
$$
推广
$$
\big(f(g[h(x)])\big)^\prime=f^\prime(g[h(x)])\cdot g^\prime[h(x)]\cdot h^\prime(x)
$$
### 一阶微分形式的不变性
$$
\begin{align}
\big(f[g(x)]\big)^\prime &=f^\prime[g(x)]\cdot g^\prime(x) \nonumber\\
\cfrac{\mathrm{d}f[g(x)]}{\mathrm{d}x} &=f^\prime[g(x)]\cdot g^\prime(x) \nonumber\\
\mathrm{d}f[g(x)] &=f^\prime[g(x)]\cdot g^\prime(x)\mathrm{d}x \nonumber\\
g^\prime(x)\mathrm{d}x &=\mathrm{d}g(x) \nonumber\\
\end{align}
$$

<u>**一阶微分**</u>形式的不变性：

$$
\mathrm{d}g(x)=g^\prime(x)\mathrm{d}x \\
\mathrm{d}f(x)=f^\prime(x)\mathrm{d}x \\
\mathrm{d}f(\square)=f^\prime(\square)\mathrm{d}\square \\
$$

### 常用导数公式
$$
\begin{array}{l}
(\tan x)^\prime = \sec^2x & (\sec x)^\prime = \sec x \tan x \\
(\arcsin x)^\prime = \cfrac{1}{\sqrt{1-x^2}} & (\arctan x)^\prime =  \cfrac{1}{1+x^2} \\
(\arccos x)^\prime = \cfrac{-1}{\sqrt{1-x^2}} & [\ln{(x+\sqrt{x^2\pm a^2})}]^\prime = \cfrac{1}{\sqrt{x^2\pm a^2}} \\
(\ln{|x|})^\prime=\cfrac{1}{x} & (\ln{|u(x)|})^\prime=\cfrac{u^\prime(x)}{u(x)} \\
(\sqrt{x})^\prime = \cfrac{1}{2\sqrt{x}} & (x^{-1})^\prime = \cfrac{-1}{x^2} \\
\end{array}
$$

#### 一个特殊的求导
$$
\begin{aligned}
\cfrac{\mathrm{d}}{\mathrm{d}x}\left[f(x)^{g(x)}\right]&=\cfrac{\mathrm{d}}{\mathrm{d}x}\left[\mathrm{e}^{g(x)\ln{f(x)}}\right]\\
&=(g\ln{f})^\prime\cdot\mathrm{e}^{g\ln{f}}\\
&=\big(g^\prime\ln{f}+\cfrac{g}{f}f^\prime\big)f^g\\
\end{aligned}
$$

>例题：$\cfrac{\partial}{\partial y}(1+xy)^y$

### 变限积分求导公式      
结论：
$$
\cfrac{\mathrm{d}}{\mathrm{d}x}\int_{\varphi_1(x)}^{\varphi_2(x)}{f(t)\mathrm{d}t}=f[\varphi_2(x)]\varphi_2^\prime(x)-f[\varphi_1(x)]\varphi_1^\prime(x)
$$
证明： 
设$\ f(x)\ $原函数为$\ F(x)+C\ $，则$\ F^\prime(x)=f(x)\ \Rightarrow\ F^\prime[g(x)]=f[g(x)]$
$$
\begin{align}
  & \cfrac{\mathrm{d}}{\mathrm{d}x}\int_{\varphi_1(x)}^{\varphi_2(x)}{f(t)\mathrm{d}t} \nonumber\\
= & \cfrac{\mathrm{d}}{\mathrm{d}x}\big(F[\varphi_2(x)]+C-F[\varphi_1(x)]-C\big) \nonumber\\
= & F^\prime[\varphi_2(x)]\varphi_2^\prime(x)-F^\prime[\varphi_1(x)]\varphi_1^\prime(x) \nonumber\\
= & f[\varphi_2(x)]\varphi_2^\prime(x)-f[\varphi_1(x)]\varphi_1^\prime(x) \nonumber\\
\end{align}
$$

### 反函数求导
反函数求导及<u>**反函数的二阶导**</u>    

- 反函数求一阶导   

**注意：**反函数可以求导的<u>**条件是**</u>$\ y=f(x)\ $<u>**可导**</u>且$\ f^\prime(x)\ne 0\ $

设函数$\ y = f(x)\ $与它的反函数$\ x = f^{-1}(y)=\varphi(y)\ $    

则导数$\cfrac{\mathrm{d}y}{\mathrm{d}x}=\cfrac{1}{\cfrac{\mathrm{d}x}{\mathrm{d}y}}$，则有$\ \varphi^\prime(y)=\cfrac{1}{f^\prime(x)}\ $   

应用举例：

求$\ \sin x\ $反函数$\ \arcsin x\ $的导数

$\varphi^\prime(y)=\cfrac{1}{f^\prime(x)}=\cfrac{1}{\cos x}=\cfrac{1}{\sqrt{1-\sin^2 x}}=\cfrac{1}{\sqrt{1-y^2}}$

求$\ \tan x\ $反函数$\ \arctan x\ $的导数

$\varphi^\prime(y)=\cfrac{1}{f^\prime(x)}=\cfrac{1}{\sec^2 x}=\cfrac{1}{1+\tan^2 x}=\cfrac{1}{1+y^2}$

- 反函数求<u>**二阶导**</u>

符号表示：函数$\ y=f(x)\ $，反函数$\ x=f^{-1}(y)=\varphi(y)\ $

首先正向写出$\ f^{\prime\prime}(x)\ $即$\ y_{xx}^{\prime\prime}\ $
$y_{xx}^{\prime\prime}=\cfrac{\mathrm{d}^2y}{\mathrm{d}x^2}=\cfrac{\mathrm{d}\Big(\cfrac{\mathrm{d}y}{\mathrm{d}x}\Big)}{\mathrm{d}x}=\cfrac{\mathrm{d}\Big(\cfrac{1}{x_y^\prime}\Big)}{\mathrm{d}x}$   

由于$\ \big(\cfrac{1}{u(x)}\big)^\prime=\cfrac{-u^\prime(x)}{[u(x)]^2}\ $，则$\ y_{xx}^{\prime\prime}=\cfrac{\mathrm{d}\Big(\cfrac{1}{x_y^\prime}\Big)}{\mathrm{d}x}=\cfrac{-x_{yy}^{\prime\prime}}{(x_y^\prime)^2}\cdot\cfrac{1}{x_y^\prime}=\cfrac{-x_{yy}^{\prime\prime}}{(x_y^\prime)^3} \ $

交换$\ x,y\ $的位置，可以得到
$$
x_{yy}^{\prime\prime}=\varphi^{\prime\prime}(y)=\cfrac{-y_{xx}^{\prime\prime}}{(y_x^\prime)^3}
$$

-------

综上，例题：设$\ y=f(x)\ $的反函数是$\ x=\varphi(y)\ $，且$\ f(x)=\displaystyle\int_{1}^{2x}{\mathrm{e}^{t^2}\mathrm{d}t}+1$，则$\varphi^{\prime\prime}(1)=\quad$

解答： 
根据公式可知
$$
x_{yy}^{\prime\prime}=\varphi^{\prime\prime}(y)=\cfrac{-y_{xx}^{\prime\prime}}{(y_x^\prime)^3}
$$
对$\ f(x)\ $求导，得
$$
\begin{array}{l}
f^\prime(x)         =2\mathrm{e}^{(2x)^2}=2\mathrm{e}^{4x^2} \\
f^{\prime\prime}(x) =16x\mathrm{e}^{4x^2} \\
\end{array}
$$
所以得到$\varphi^{\prime\prime}(y)=\cfrac{-f^{\prime\prime}(x)}{[f^\prime(x)]^3}=\cfrac{-2x}{\mathrm{e}^{8x^2}}$，注意到这个式子中$\varphi^{\prime\prime}(y)$的<u>**自变量**</u>应该是$\ y\ $，则$\varphi^{\prime\prime}(1)$的计算式中的$\ x\ $应取在$\ y=1\ $时的$\ x\ $的值，为$\ x=0.5\ $，所以式子答案应代入$\ x=0.5\ $计算。    

最终计算式：$\varphi^{\prime\prime}(1)=\cfrac{-f^{\prime\prime}(0.5)}{[f^\prime(0.5)]^3}=\cfrac{-2(0.5)}{\mathrm{e}^{8(0.5)^2}}=\cfrac{-1}{\mathrm{e}^2}$

### 参数方程的求导
#### 参数方程求导(一阶导数)
参数方程：
$$
y=y(x)\left\{\begin{array}{l}
x=x(t)\\
y=y(t)
\end{array}\right.\\
\\
\cfrac{\mathrm{d}y}{\mathrm{d}x}=\cfrac{\mathrm{d}y/\mathrm{d}t}{\mathrm{d}x/\mathrm{d}t}
$$

#### 参数方程求导(二阶导数)
在一阶导数的基础上再求一阶导
$$
y=y(x)\left\{\begin{array}{l}
x=x(t)\\
y=y(t)
\end{array}\right.\\
\\
\cfrac{\mathrm{d}^2y}{\mathrm{d}x^2}=\cfrac{\mathrm{d}\Big(\cfrac{\mathrm{d}y}{\mathrm{d}x}\Big)}{\mathrm{d}x}=\cfrac{\mathrm{d}\Big(\cfrac{\mathrm{d}y}{\mathrm{d}x}\Big)/\mathrm{d}t}{\mathrm{d}x/\mathrm{d}t}
$$

-------

注意一个很蠢的错误：
$$
y=y(x)\left\{\begin{array}{l}
x=x(t)\\
y=y(t)
\end{array}\right.\\
$$
参数方程里，$\ x=x(t)\ $在上面，但是求$\ \cfrac{\mathrm{d}y/\mathrm{d}t}{\mathrm{d}x/\mathrm{d}t}\ $的时候，$\ \mathrm{d}y/\mathrm{d}t\ $在上面，不要求倒了！

### 隐函数求导
相当于把等式两边同时对$\ x\ $求导，此时将$\ y\ $看作$\ f(x)\ $

例子：$\ y\ln y\ $的求导与$\ x\ln x\ $的求导的不同
$$
\begin{array}{l}
(x\ln x)^\prime=\ln x+1\\
(y\ln y)^\prime=y^\prime \ln y+y^\prime\\
\end{array}
$$
注意事项
1. 注意看题目是求的导数还是微分，微分要加上$\ \cdot\mathrm{d}x\ $
2. 如果遇到形如$\ u^v\ $形式，利用$\ u^v=\mathrm{e}^{v\ln u}\ $进行替换之后，最后写结果的时候，别忘了把含有$\ u^v=\mathrm{e}^{v\ln u}\ $的部分还原回$\ u^v\ $

-------
简单来说，求导结束后，需要仔细检查两件事：**是求的<u>导数</u>还是<u>微分</u>、是否可以<u>继续化简</u>**

### 对数求导法
放心去绝对值符号：对数求导公式
$$
\begin{array}{l}
(\ln{|x|})^\prime=\cfrac{1}{x} & (\ln{|u(x)|})^\prime=\cfrac{u^\prime(x)}{u(x)}
\end{array}
$$

### 高阶导数
#### 归纳法
#### 高阶求导公式
类似于二项式定理$\ (a+b)^n=\sum\limits_{k=0}^{n}{\mathrm{C}_{n}^{k}{a^{n-k}b^{k}}}$   

高阶求导公式$\ (uv)^{(n)}=\sum\limits_{k=0}^{n}{\mathrm{C}_{n}^{k}{u^{(n-k)}v^{(k)}}}$   

#### 利用泰勒公式求高阶导数
泰勒公式的通式：
$$
\begin{array}{l}
y=f(x)=\sum\limits_{n=0}^{\infty}{\cfrac{f^{(n)}(x_0)}{n!}(x-x_0)^n} \\
y=f(x)=\sum\limits_{n=0}^{\infty}{\cfrac{f^{(n)}(0)}{n!}x^n} & (x_0=0)
\end{array}
$$
注意两个特殊的Taylor Series    
$$
\begin{array}{l}
\cfrac{1}{1-x} = \sum\limits_{n=0}^{\infty}{x^n}
\left|\begin{array}{l}
a_n=a_1q^{n-1} & \Rightarrow \sum a_n=\cfrac{a_1(1-q^n)}{1-q}\\
b_n=x^n     & \Rightarrow \sum b_n=\cfrac{1-x^n}{1-x}
\end{array}\right.
\\
(1+x)^k=1+kx+\cfrac{k(k-1)}{2!}x^2+\cfrac{k(k-1)(k-2)}{3!}x^3+\cdots,
\left\{\begin{array}{l}
x\in (-1,1) ,k\le -1 \\
x\in (-1,1] ,-1<k<0 \\
x\in [-1,1] ,k>0 \\
\end{array}\right.
\end{array}
$$

-------

例题：设$\ y=x^3\sin x\ $，求$\ y^{(6)}(0)\ $     

解答： 
第一步，写出通式    
$$
y=\sum\limits_{n=0}^{\infty}{\cfrac{x^n}{n!}f^{(n)}(0)}=\cdots+\cfrac{x^6}{6!}f^{(6)}(0)+\cdots
$$
第二步，写原函数Taylor展开    
$$
y=x^3\sin x=x^3\big(x-\cfrac{x^3}{6}+\cdots\big)=\cdots+\cfrac{-1}{6}x^6+\cdots
$$
第三步，因为Taylor展开具有唯一性，第一步与第二步的式子相等，所以对比系数
$$
\cfrac{f^{(6)}(0)}{6!}=\cfrac{-1}{6}\\
f^{(6)}(0)=-5!=-120
$$

#### 高阶导数重要公式
$$
\begin{array}{l}
(\sin kx)^{(n)}= k^n\sin{\big(kx+\cfrac{n\pi}{2}\big)} & (\cos kx)^{(n)}= k^n\cos{\big(kx+\cfrac{n\pi}{2}\big)} \\
(\ln x)^{(n)}= (-1)^{n+1}\cfrac{(n-1)!}{x^n} & (x^{-1})^{(n)}=(-1)^n\cfrac{n!}{x^{n+1}}\\
\big(\cfrac{1}{x+a}\big)^{(n)}= \cfrac{(-1)^nn!}{(x+a)^{n+1}} & \big(\cfrac{1}{kx+b}\big)^{(n)}= \cfrac{(-1)^nk^nn!}{(x+b)^{n+1}}\\
\end{array}
$$
记忆技巧：
1. $(x^{-1})^{(n)}=(\ln x)^{(n+1)}$，记住$(\ln x)^{(n)}$之后，将$\ n\ $替换为$\ n+1\ $即为$(x^{-1})^{(n)}$
2. $\sin x\ $每求一次导，相当于向左平移$\ \cfrac{\pi}{2}\ $个单位


### 导数题目技巧
观察特殊项：  

例题：设$\ f(x)=\prod\limits_{n=1}^{100}{\big(\tan\cfrac{\pi x^n}{4}-n\big)}\ $，则$\ f^\prime(1)=\qquad $答案：$-\cfrac{\pi\cdot 99!}{2}$

解答：
$$
f(x)=\big(\tan\cfrac{\pi x^1}{4}-1\big)\big(\tan\cfrac{\pi x^2}{4}-2\big)\cdots\big(\tan\cfrac{\pi x^{100}}{4}-100\big) \\
\begin{align}
f^\prime(x) &=\big(\tan\cfrac{\pi x^1}{4}-1\big)^\prime\big(\tan\cfrac{\pi x^2}{4}-2\big)\cdots\big(\tan\cfrac{\pi x^{100}}{4}-100\big)\nonumber\\
&+\big(\tan\cfrac{\pi x^1}{4}-1\big)\big(\tan\cfrac{\pi x^2}{4}-2\big)^\prime\cdots\big(\tan\cfrac{\pi x^{100}}{4}-100\big)\nonumber\\
&+\quad \cdots \nonumber\\
&+\big(\tan\cfrac{\pi x^1}{4}-1\big)\big(\tan\cfrac{\pi x^2}{4}-2\big)\cdots\big(\tan\cfrac{\pi x^{100}}{4}-100\big)^\prime \nonumber\\
\end{align}
$$
注意到$\ x=1\ $时，$\big(\tan\cfrac{\pi x^1}{4}-1\big)=0$，所以在计算$\ f^\prime(1)\ $中，除了第一项，后面$\ 99\ $项全为$\ 0\ $，所以可以将$\ f^\prime(x)\ $改写为$\ f(x)=\big(\tan\cfrac{\pi x^1}{4}-1\big)\cdot g(x)\ $此时有

$$
\begin{align}
f^\prime(x) &= \big(\tan\cfrac{\pi x^1}{4}-1\big)^\prime\cdot g(x)+\big(\tan\cfrac{\pi x^1}{4}-1\big)\cdot g^\prime(x) \nonumber\\
f^\prime(1) &= \big(\tan\cfrac{\pi x}{4}-1\big)^\prime\Big|_{x=1}\cdot g(1)+0\cdot g^\prime(x) \nonumber\\
            &= \Big[\big(\cfrac{2}{\sqrt{2}}\big)^2\cdot\cfrac{\pi}{4}\Big]\cdot (-1)(-2)\cdots(-99) \nonumber\\
            &=-\cfrac{\pi\cdot 99!}{2} \nonumber\\
\end{align}
$$



## 第五讲 一元函数微分学的几何应用
### 极值点与拐点
极值点与拐点的判别   
- 极值点
$$
\begin{array}{l}
f^\prime(x_0)=0     &   f^{\prime\prime}(x_0)\ne 0   \\
f^{\prime\prime\prime}(x_0)=0     &   f^{(4)}(x_0)\ne 0   \\
\end{array}
$$
```
极值点是个数x=a
```
```
极值点需要左右邻域，就是说端点不行！最值点不需要邻域！
```


- 拐点
$$
\begin{array}{l}
f^{\prime\prime}(x_0)=0 & f^{\prime\prime\prime}(x_0)\ne 0   \\
f^{(4)}(x_0)=0     &   f^{(5)}(x_0)\ne 0   \\
\end{array}
$$
```
拐点从二阶导开始，与一阶导数无关！
```
```
拐点是个点，是(a,f(a))
```


- $(x-x_0)^n\ $求$\ n\ $阶导  
$\ n\ $阶导$\ \Rightarrow\ n!$    

$\ n+1\ $阶导$\ \Rightarrow\ 0$

- perfect example


![](media/extreme point and inflection point.jpg)



### 极值点与拐点判别的证明★
#### 极值点辨别的证明

-------

**极值辨别的第一充分条件**  
前提：$\ f(x)\ $在$\ x=x_0\ $处连续，且在$\ x=x_0\ $处的某去心邻域$\ \mathring{U}(x_0,\delta)\ $内可导。  
若$\ f^\prime(x)\ $在$\ x\in (x_0-\delta,x_0)\ $到$\ x\in (x_0,x_0+\delta)\ $由正变负，则在$\ x=x_0\ $取极大值；由负变正，则取极小值；不变号，则$\ x=x_0\ $非极值点。


**极值辨别的第二充分条件**
$$
\begin{array}{l}
f^\prime(x_0)=0     &   f^{\prime\prime}(x_0)\ne 0   \\
\end{array}
$$

**极值辨别的第三充分条件**   
$$
\begin{array}{l}
f^{(1)}(x_0)=f^{(2)}(x_0)=\cdots=f^{(2k-1)}(x_0)=0  & \quad &   f^{(2k)}(x_0)\ne 0 & \quad k\in N_+  \\
\end{array}
$$

-------
- <u>**第二充分条件**</u>的证明 

**证明方法一**：   

已知$\ f^\prime(x_0)=0\ $和$\ f^{\prime\prime}(x_0)\ne 0\ $，证$\ x=x_0\ $为极值点。

证明：已知条件可写为
$$
\begin{array}{rclllr}
f^\prime(x_0) & = & \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{x-x_0}} & = & 0 & \qquad(1) \\
f^{\prime\prime}(x_0) & = & \lim\limits_{x\to x_0}{\cfrac{f^\prime (x)-f^\prime (x_0)}{x-x_0}} & \ne & 0 & \qquad (2) \\
\end{array}
$$
由$\ (2)\ $式，通过局部保号性得到结论$\ \cfrac{f^\prime (x)-f^\prime (x_0)}{x-x_0}\gtrless 0\ $  
当$\ x>x_0\ $(右邻域)$\ \Rightarrow x-x_0>0\ $，不变号，即$\ f^\prime (x)-f^\prime (x_0)\gtrless 0\ $  
当$\ x<x_0\ $(左邻域)$\ \Rightarrow x-x_0>0\ $，变号，即$\ f^\prime (x)-f^\prime (x_0)\lessgtr 0\ $  
综上可得，变为第一充分条件，证明完毕。

**证明方法二**：   
证明：已知条件可写为
$$
\begin{array}{rclllr}
f^\prime(x_0) & = & \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{x-x_0}} & = & 0 & \qquad(1) \\
f^{\prime\prime}(x_0) & = & \lim\limits_{x\to x_0}{\cfrac{f^\prime (x)-f^\prime (x_0)}{x-x_0}} & \ne & 0 & \qquad (2) \\
\end{array}
$$

构造极限$\ \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)^2}}=\cfrac{1}{2}\lim\limits_{x\to x_0}{\cfrac{f^\prime(x)-f^\prime(x_0)}{(x-x_0)}}\ne 0\ $  (注：应用洛必达)

由局部保号性，$\ \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)^2}}\ne 0\ $，可得在去心邻域内，$\ \cfrac{f(x)-f(x_0)}{(x-x_0)^2}\gtrless 0$  

由于分子为正，$\ f(x)-f(x_0)\gtrless 0\ $保持符号一致，得到在去心邻域内$\ f(x)\gtrless f(x_0)\ $，即在邻域内取得极大/小值

**证明方法三**：   

不妨设$\ f^{\prime\prime}(x_0)<0\ $  

将$\ f(x)\ $在$\ x=x_0\ $处展开，则有$\ f(x)=f(x_0)+f^\prime(x_0)(x-x_0)+\cfrac{f^{\prime\prime}(x_0)}{2}(x-x_0)+o[(x-x_0)^2]\ $   

由于$\ f^\prime(x_0)=0,\quad f^{\prime\prime}(x_0)<0\ $，则有$\ f(x)=f(x_0)+\cfrac{f^{\prime\prime}(x_0)}{2}(x-x_0)+o[(x-x_0)^2]\le f(x_0)\ $   

则$\ f(x)\ $在$\ x=x_0\ $处取得极大值。

-------


- <u>**第三充分条件**</u>的证明

构造极限$\ \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)^{2k}}}=\cfrac{1}{(2k)!}\lim\limits_{x\to x_0}{\cfrac{f^{(2k-1)}(x)-f^{(2k-1)}(x_0)}{(x-x_0)}}\ne 0\ $  
**[注1]**应用洛必达   
**[注2]**对$\ x^n\ $求$\ n-1\ $阶导和求$\ n\ $阶导的系数一致   

由局部保号性，$\ \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)^{2k}}}\ne 0\ $，可得在去心邻域内，$\ \cfrac{f(x)-f(x_0)}{(x-x_0)^{2k}}\gtrless 0$  

由于分子为正，$\ f(x)-f(x_0)\gtrless 0\ $保持符号一致，得到在去心邻域内$\ f(x)\gtrless f(x_0)\ $，即在邻域内取得极大/小值
**[注3]**为什么$\ \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)}}=0$，反而$\ \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)^{2k}}}\ne 0$  
解释：例如$\ \lim\limits_{x\to 0}{\cfrac{x^2}{x}}=0\ $，而$\ \lim\limits_{x\to 0}{\cfrac{x^2}{x^2}}=1\ne 0\ $

```
第二充分条件的证明一，将条件落脚到第一充分条件，完成证明。
而第二充分条件的证明二，和第三充分条件的证明，
则直接将条件落脚到了极值的定义来证明。
```
```
通过第三充分条件的证明，更能加深对极值点判别的理解，
因为这时的分母(x-x0)^(2k)恒为正，
所以才可以得到f(x)与f(x0)在邻域内满足恒严格大于/小于，
进而从极值的定义得到判别结论。
```
```
拐点的判别直接把极值的判别全部多加一阶导即可。
需要指出的是，同样是第三充分条件对证明，
正是因为拐点辨别的时候分母为(x-x0)^(2k+1)正负不定，
所以才使得拐点辨别式的2k阶导左右变号。
```


#### 拐点辨别的证明

-------

**拐点辨别的第一充分条件**  
前提：$\ f(x)\ $在$\ x=x_0\ $处连续，且在$\ x=x_0\ $处的某去心邻域$\ \mathring{U}(x_0,\delta)\ $内**二阶**可导。  
若$\ f^{\prime\prime}(x)\ $在$\ x\in (x_0-\delta,x_0)\ $到$\ x\in (x_0,x_0+\delta)\ $由正变负，则在$\ x=x_0\ $由凹变凸；由负变正，则凸变凹；不变号，则$\ x=x_0\ $非拐点。



**拐点辨别的第二充分条件**  
$$
\begin{array}{l}
f^{\prime\prime}(x_0)=0  & f^{\prime\prime\prime}(x_0)\ne 0   \\
\end{array}
$$


**拐点辨别的第三充分条件**   
$$
\begin{array}{l}
f^{(1)}(x_0)=f^{(2)}(x_0)=\cdots=f^{(2k)}(x_0)=0  & \quad &   f^{(2k+1)}(x_0)\ne 0 & \quad k\in N_+  \\
\end{array}
$$

-------

- <u>**第二充分条件**</u>的证明 

已知$\ f^\prime(x_0)=0\ $和$\ f^{\prime\prime}(x_0)\ne 0\ $，证$\ x=x_0\ $为极值点。

证明：已知条件可写为
$$
\begin{array}{rclllr}
f^{\prime\prime}(x_0) & = & \lim\limits_{x\to x_0}{\cfrac{f^\prime (x)-f^\prime (x_0)}{x-x_0}} & = & 0 & \qquad(1) \\
f^{\prime\prime\prime}(x_0) & = & \lim\limits_{x\to x_0}{\cfrac{f^{\prime\prime}(x)-f^{\prime\prime}(x_0)}{x-x_0}} & \ne & 0 & \qquad (2) \\
\end{array}
$$
由$\ (2)\ $式，通过局部保号性得到结论$\ \cfrac{f^{\prime\prime}(x)-f^{\prime\prime}(x_0)}{x-x_0}\gtrless 0\ $  
当$\ x>x_0\ $(右邻域)$\ \Rightarrow x-x_0>0\ $，不变号，即$\ f^{\prime\prime}(x)-f^{\prime\prime}(x_0)\gtrless 0\ $  
当$\ x<x_0\ $(左邻域)$\ \Rightarrow x-x_0>0\ $，变号，即$\ f^{\prime\prime}(x)-f^{\prime\prime}(x_0)\lessgtr 0\ $  
综上可得，变为第一充分条件，证明完毕。


### 概念例题
>例题1  
已知$\ f(x)\ $在$\ x=0\ $的某个邻域内连续，且$\ \lim\limits_{x\to 0}{\cfrac{f(x)}{1-\cos x}}=2\ $，则在点$\ x=0\ $处$\ f(x)\ $（？D）
A.不可导   B.可导且$\ f^\prime(0)=0\ $  C.取极大值  D.取极小值

-------

>例题2     
若$\ f(x)\ $在$\ x_0\ $至少二阶可导，且$\ \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)^2}}=-1\ $，则函数$\ f(x)\ $在点$\ x=x_0\ $处（？B）     
A.取极大值  B.取极小值  C.无极值  D.不确定

-------

例题1与例题2本质上一样，以例题2为例，给出两种方法，正是对应了两种不同的思路。  

**方法一(<u>除乘技巧</u>)**：  
由于$\ \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)^2}}=-1\ $   
则有$\ f^\prime(x_0)=\lim\limits_{x\to x_0}{\big[\cfrac{f(x)-f(x_0)}{(x-x_0)^2}(x-x_0)\big]}=\lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)}}=0\ $   
由于$\ \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)^2}}=-1<0\ $  
根据局部保号性，$\cfrac{f(x)-f(x_0)}{(x-x_0)^2}<0\ \Rightarrow\ f(x)<f(x_0)$，所以为极大值。   

**方法二(<u>类似第三充分条件思路、洛必达</u>)**：     
由题目已知$\ \lim\limits_{x\to x_0}{\cfrac{f(x)-f(x_0)}{(x-x_0)^2}}=-1\ $     
直接洛必达，$\ \lim\limits_{x\to x_0}{\cfrac{f^\prime(x)}{2(x-x_0)}}=-1<0 \qquad $**[注]**常数$\ f(x_0)\ $的导数为$\ 0$   
根据局部保号性，$\ \cfrac{f^\prime(x)}{x-x_0}<0\ $  
所以得到$\ f^\prime(x)\ $右邻域$\ f^\prime(x)<0\ $，左邻域$\ f^\prime(x)>0\ $，为极大值。




### 求渐近线
#### 步骤
1. 找无定义点
2. 找$\ \lim\limits_{x\to\infty}{f(x)}$，注意$\ x\to +\infty/-\infty/\infty$
3. 求$\ k=\lim\limits_{x\to\infty}{\cfrac{f(x)}{x}}\ $，如果$\ k\ne 0\ $则求$\ b=\lim\limits_{x\to\infty}{[f(x)-kx]}$



## 第六讲 中值定理
### 涉及函数的中值定理(4个)与积分中值定理
### 涉及导数的中值定理(5个)

### 达布定理
>达布定理
>定义在$\ [a,b]\ $上的$\ f^\prime(x)\ $满足介质性质。

对比介值定理

>连续函数的介值定理（张宇2022基础30讲-第六讲-定理2）
>定义在$\ [a,b]\ $上的连续函数$\ f(x)\ $满足介质性质。

定理2可看作达布定理的推论，因为任何定义在$\ [a,b]\ $上的连续函数$\ f(x)\ $都可看作是某个$\ F(x)\ $的导数。认为$\ f(x)=F^\prime(x)\ $即可。


>达布定理推论
>定义在$\ [a,b]\ $上的$\ f^\prime(x)\ $满足介质性质。
>- - - -
>1.在定义域$\ [a,b]\ $内$\ f^\prime(x)\ $没有跳跃间断点。
>2.若在定义域$\ [a,b]\ $内$\ f^\prime(x)\ne 0\ $，则$\ f^\prime(x)\ $保号。
>3.导数零点定理

注意：
函数零点定理与导数零点定理的区别   
<u>**函数**</u>零点定理：  
若$\ f(x)\ $在$\ [a,b]\ $上<u>**连续**</u>，则当$\ f(a)\cdot f(b)<0\ $时，存在$\  \xi\in (a,b)\ $使得$\ f(\xi)=0\ $   

<u>**导数**</u>零点定理：  
若$\ f^\prime(x)\ $在$\ [a,b]\ $上<u>**存在**</u>(不必连续)，则当$\ f_+^\prime(a)\cdot f_-^\prime(b)<0\ $时，存在$\  \xi\in (a,b)\ $使得$\ f^\prime(\xi)=0\ $   

-------

<u>**导数**</u>零点定理的证明：<u>**脱帽法（严格大/小于）**</u>   
$$
\begin{array}{c}
f_+^\prime(a)=\lim\limits_{x\to a^+}{\cfrac{f(x)-f(a)}{x-a}}\gtrless 0 &\Rightarrow & \exists\xi_1\gtrless 0,\quad (a,a+\xi_1),\quad f(x)\gtrless f(a)   \\
f_-^\prime(b)=\lim\limits_{x\to b^-}{\cfrac{f(x)-f(b)}{x-b}}\lessgtr 0 &\Rightarrow & \exists\xi_2\gtrless 0,\quad (b-\xi_2,b),\quad f(x)\gtrless f(b)
\end{array}
$$
所以$\ f(a),f(b)\ $均非$\ f(x)\ $在$\ [a,b]\ $的最大/小值，根据费马定理，存在$\ \xi\in (a,b)\ $，使得$\ f^\prime(\xi)=0\ $。(极大值+可导$\Rightarrow f^\prime(\xi)=0\ $)

```
脱帽法脱掉极限的lim的帽子，是由极限推不等。
```


-------

<u>**达布定理**</u>的证明：    

>设$\ f(x)\ $在$\ [a,b]\ $上可导，若$\ f_+^\prime(a)\ne f_-^\prime(b)\ $，证明对于任意的介于$\ f_+^\prime(a)\ $与$\ f_-^\prime(b)\ $之间的$\ \mu\ $，存在$\ \xi\in (a,b)\ $，使得$\ f^\prime(\xi)=\mu\ $    

设$\ f_+^\prime(a)\gtrless f_-^\prime(b)\ $，由于$\ \mu\ $介于$\ f_+^\prime(a)\ $与$\ f_-^\prime(b)\ $之间，则$\ f_-^\prime(b)\lessgtr \mu\lessgtr f_+^\prime(a)\ $   

令$\ F(x)=f(x)-\mu x\ $，则$\ F^\prime(x)=f^\prime(x)-\mu\ $

$$
f_-^\prime(b)\lessgtr \mu\lessgtr f_+^\prime(a)\Rightarrow
\left\{\begin{array}{l}
F_+^\prime(a)=f_+^\prime(a)-\mu > 0 \\
F_-^\prime(b)=f_+^\prime(b)-\mu < 0 \\
\end{array}\right.
\Rightarrow
\left\{\begin{array}{l}
F_+^\prime(a)=\lim\limits_{x\to a^+}{\cfrac{F(x)-F(a)}{x-a}} > 0 \\
F_-^\prime(b)=\lim\limits_{x\to b^-}{\cfrac{F(x)-F(b)}{x-b}} < 0 \\
\end{array}\right.
$$
由函数极限的局部保号性，
$$
\left\{\begin{array}{c}
F(x)-F(a) > 0 \\
F(x)-F(b) > 0
\end{array}\right.\Rightarrow
\left\{\begin{array}{c}
F(x)>F(a) \\
F(x)>F(b)
\end{array}\right.
$$
则$\ F(a),\quad F(b)\ $均非$\ F(x)\ $在$\ [a,b]\ $的最值，
设$\ F(x)\ $在$\ [a,b]\ $的最值为$\ F(\xi)\ ,\xi\in (a,b)\ \Rightarrow\ F^\prime(\xi)=0\ \Rightarrow\ f^\prime(\xi)=\mu $

-------

费马定理的证明：<u>**戴帽法（可取等号）**</u>   
假设$\ f(x)\ $在$\ x_0\ $处取得极大值，则存在$\ x_0\ $的邻域$\ \mathring{U}(x_0)\ $，对任意的$\ x\in\mathring{U}(x_0)\ $，有$\ f(x)-f(x_0)\le 0\ $，则有
$$
\begin{array}{c}
f_+^\prime(x_0)=\lim\limits_{x\to x_0^+}{\cfrac{f(x)-f(x_0)}{x-x_0}}\ge 0\\
f_-^\prime(x_0)=\lim\limits_{x\to x_0^-}{\cfrac{f(x)-f(x_0)}{x-x_0}}\le 0
\end{array}
$$
由于$\ f(x)\ $在$\ x=x_0\ $可导，所以$\ f_-^\prime(x_0)=f_+^\prime(x_0)=0\ $，即$\ f^\prime(x_0)=0\ $

```
戴帽法是连续函数局部保号推论，由函数局部不等关系得到极限lim关系式。
```

-------

如果$\ f(x)\ $在$\ x_0\ $处的导数$\ f^\prime(x_0)> 0\ $，那么$\ f(x)\ $不一定在$\ x_0\ $的一个邻域单增。   
反例：$\ f(x)=\cfrac{x}{2}+x^2\sin\cfrac{1}{x}\quad [\text{ let }f(0)=0\ ]\ $  
$\ f^\prime(0)=\lim\limits_{x\to 0}{\cfrac{f(x)-f(0)}{x-0}}=\cfrac{1}{2}\ $，而$\ f^\prime(x)=\cfrac{1}{2}+2x\sin\cfrac{1}{x}-\cos\cfrac{1}{x}\ $，任取$\ \{x_n\}=\cfrac{1}{2n\pi}\ $，则$\ f^\prime(x_n)\ne 0$

### 拉格朗日中值定理-以例题说明要注意事项
- $\ f^\prime(\xi)\ $不可以看成常数   

>设$\ f(x)\ $在$\ [0,1]\ $上有一阶连续导数，$\ f(0)=0\ $   
>证明：$\exists\xi\in (0,1),\quad f^\prime(\xi)=\displaystyle 2\int_{0}^{1}{f(x)\mathrm{d}x}$

由拉格朗日中值定理，$\ f(x)-f(0)=f^\prime(\mu)(x-0)\ $   
化简得到$\ f(x)=f^\prime(\mu)x\ ,\mu\in (0,x)\quad x\in(0,1)$   
同取积分，则有$\ \displaystyle 2\int_{0}^{1}{f(x)\mathrm{d}x}=2\int_{0}^{1}{f^\prime(\mu)x\mathrm{d}x}\ $
$$
\begin{array}{cl}
m\le f^\prime(x) \le M          & x\in (0,1) \\
m\le f^\prime(\xi)\le M         & \xi\in(0,1)   \\
m\le f^\prime(\mu) \le M     & \mu\in (0,x)\subseteq (0,1) \\
mx\le xf^\prime(\mu) \le Mx              \\
\displaystyle\int_{0}^{1}{mx\mathrm{d}x}\le \int_{0}^{1}{xf^\prime(\mu)\mathrm{d}x} \le \int_{0}^{1}{Mx\mathrm{d}x} \\
m\le \displaystyle 2\int_{0}^{1}{xf^\prime(\mu)\mathrm{d}x} \le M \\
m\le \displaystyle 2\int_{0}^{1}{f(x)\mathrm{d}x} \le M
\end{array}
$$
则有$\ f^\prime(\xi)=\displaystyle 2\int_{0}^{1}{f(x)\mathrm{d}x}\ $

```
拉格朗日中值定理f(x)-f(a)=f’(ξ)(x-a)时，f’(ξ)不可看成常数！
```
```
介值定理大杀四方！
```

- 出现两个$\ \xi\ $时，**分割区间**

>设$\ f(x)\ $在$\ [0,1]\ $上连续，在$\ (0,1)\ $可导，且$\ f(0)=0,f(1)=1$  
>证明：$\exists\xi_1,\xi_2\in(0,1),\xi_1\ne\xi_2,\cfrac{1}{f^\prime(\xi_1)}+\cfrac{1}{f^\prime(\xi_2)}=2$   

将区间分为$\ [0,\tau],[\tau,1]\ $，分别应用拉格朗日中值定理：
$$
\begin{array}{l}
f(\tau)-f(0)=f^\prime(\xi_1)(\xi-0)  & \Rightarrow & \cfrac{1}{f^\prime(\xi_1)}=\cfrac{\tau}{f(\tau)} & \xi_1\in (0,\tau)\\
f(1)-f(\tau)=f^\prime(\xi_2)(1-\tau) & \Rightarrow & \cfrac{1}{f^\prime(\xi_2)}=\cfrac{1-\tau}{1-f(\tau)} &\xi_2\in (\tau,1)\\
\end{array}
$$
使题设等式成立，需要$\ \cfrac{\tau}{f(\tau)}+\cfrac{1-\tau}{1-f(\tau)}=2\ $，则取$\ f(\tau)=\cfrac{1}{2}\ $

```
f(τ)=0.5成立的原因在于介值定理，f(x)可取0~1任何值。
```







## 第十一讲 多元函数微分学
### 极限


-------

### 多元函数隐函数
#### 隐函数存在定理
>例题(2005年考研数学一 10)：
>设有三元方程$\ xy-z\ln{y}+\mathrm{e}^{xz}=1\ $，根据隐函数存在定理，存在点$\ (0,1,1)\ $的一个邻域，在此邻域内该方程（ D ）
>$A.$只能确定一个具有连续偏导数的隐函数$\ z=z(x,y)\ $   
>$B.$可能确定两个具有连续偏导数的隐函数$\ y=y(x,z)\ $和$\ z=z(x,y)\ $   
>$C.$可能确定两个具有连续偏导数的隐函数$\ x=x(y,z)\ $和$\ z=z(x,y)\ $   
>$D.$可能确定两个具有连续偏导数的隐函数$\ x=x(y,z)\ $和$\ y=y(x,z)\ $

#### 求多元函数隐函数


-------

### 可微
- 全微分   
函数$\ z=f(x,y)\ $在点$\ (x,y)\ $处的**<u>全增量</u>**$\ \Delta z=f(x+\Delta x,y+\Delta y)-f(x,y)\ $可以表示为
$$
\Delta z=A\Delta x+B\Delta y+o(\rho) \qquad \rho =\sqrt{(\Delta x)^2+(\Delta y)^2}
$$
其中，$\ A\Delta x+B\Delta y\ $是**<u>线性主部</u>**，称作**<u>全微分</u>**，记作$\ \mathrm{d}z=A\Delta x+B\Delta y\ $，或
$$
\mathrm{d}z=\cfrac{\partial z}{\partial x}\mathrm{d}x+\cfrac{\partial z}{\partial y}\mathrm{d}y
$$
而$\ \rho= \sqrt{(\Delta x)^2+(\Delta y)^2}\ $是**<u>误差项</u>**，$\ \Delta x\Delta y\ $是$\ \rho\ $的高阶无穷小，$\ \rho\ $是$\ A\Delta x+B\Delta y\ $的高阶无穷小。全增量$-$线性增量=误差。

-------

- 函数$\ z=f(x,y)\ $在点$\ (x_0,y_0)\ $可微的判断
①写**全增量**$\ \Delta z=f(x_0+\Delta x,y_0+\Delta y)-f(x_0,y_0)\ $   
②写**线性增量**$\ A\Delta x+B\Delta y=f_x^\prime(x_0,y_0)\Delta x+f_y^\prime(x_0,y_0)\Delta y\ $   
③作极限$\ \lim\limits_{\Delta x\to 0\\\Delta y\to 0}{\cfrac{\Delta z-(A\Delta x+B\Delta y)}{\sqrt{(\Delta x)^2+(\Delta y)^2}}}\left\{\begin{array}{lr}=0&\text{Differentiable.}\\ \ne 0 & \text{Non-differentiable.}\end{array}\right.$

-------

- 对比一元函数可微的辨别
①写**~~（全）~~增量**$\ \Delta y=f(x_0+\Delta x)-f(x_0)\ $   
②写**线性增量**$\ A\Delta x=f^\prime(x_0)\Delta x$   
③作极限$\ \lim\limits_{\Delta x\to 0}{\cfrac{\Delta y-(A\Delta x)}{\Delta x}}\left\{\begin{array}{lr}=0&\text{Differentiable.}\\ \ne 0 & \text{Non-differentiable.}\end{array}\right.$

```
其实相当于判断：误差项是否为线性主部的高阶无穷小。
```

-------

### 偏导数的连续性
判断函数$\ z=f(x,y)\ $在某点$\ (x_0,y_0)\ $的**偏导数**是否连续：  
①用<u>**定义**</u>求$\ f_x^\prime(x_0,y_0),f_y^\prime(x_0,y_0)\ $   
②用<u>**公式**</u>求$\ f_x^\prime(x,y),f_y^\prime(x,y)\ $，即$\cfrac{\partial z}{\partial x},\cfrac{\partial z}{\partial y}$   
③计算$\ \lim\limits_{x\to x_0\\y\to y_0}{f_x^\prime(x,y)},\lim\limits_{x\to x_0\\y\to y_0}{f_y^\prime(x,y)}\ $   
④判断$\left\{\begin{array}{l}\lim\limits_{x\to x_0\\y\to y_0}{f_x^\prime(x,y)}=f_x^\prime(x_0,y_0)\\\lim\limits_{x\to x_0\\y\to y_0}{f_y^\prime(x,y)}=f_y^\prime(x_0,y_0)\end{array}\right.$是否成立，如果成立，则函数$\ z=f(x,y)\ $在某点$\ (x_0,y_0)\ $的偏导数连续。

-------

### 偏导数的链式求导Chain Rule
- 链式求导图解    
$$
\begin{array}{ccccc}
  &   \nearrow &  u  &\longrightarrow  &  x \\
z &            &     & \huge\times               \\
  &   \searrow &  v  &\longrightarrow  &  y \\
\end{array}
$$

- 例题说明使用方法
>$z=f(\mathrm{e}^x\sin y,x^2+y^2)\qquad \cfrac{\partial ^2z}{\partial x\partial y}=\ $
>第一部分，写出四个基础偏导$\left|\begin{array}{ll}u_x^\prime & u_y^\prime\\v_x^\prime & v_y^\prime\end{array}\right|$和$\ \cfrac{\partial z}{\partial x}$   
$$
\begin{array}{rl}
\left.\begin{array}{l|l}
\cfrac{\partial u}{\partial x}=\sin y\mathrm{e}^x & \cfrac{\partial u}{\partial y}=\mathrm{e}^x\cos y\\
\cfrac{\partial v}{\partial x}=2x & \cfrac{\partial v}{\partial y}=2y\\
\end{array}\right|
&\begin{array}{ccccc}
  &   \nearrow &  ^1u  &\longrightarrow  &  x \\
z &            &     & \nearrow             \\
  &   \searrow &  ^2v  &                 &  y \\
\end{array}\\
\Rightarrow\cfrac{\partial z}{\partial x}=(\mathrm{e}^x\sin y)f_1^\prime+2xf_2^\prime\\
\end{array}
$$
第二部分，根据$\ \cfrac{\partial z}{\partial x}$，复合求导写出$\ \cfrac{\partial}{\partial y}\Big(\cfrac{\partial z}{\partial x}\Big)\ $，并由导线路得到$\ \cfrac{\partial f_{k}^\prime}{\partial y}\ $
$$
\begin{array}{l}
\left.\begin{aligned}
\cfrac{\partial ^2z}{\partial x\partial y}=\cfrac{\partial}{\partial y}\Big(\cfrac{\partial z}{\partial x}\Big) &=
(\mathrm{e}^x\cos y)f_1^\prime+\mathrm{e}^x\sin y\cfrac{\partial f_1^\prime}{\partial y}\\
&+2x\cfrac{\partial f_2^\prime}{\partial y}\\
\end{aligned}\right|
\begin{array}{ccccc}
  &   \nearrow &  ^1u  &                &  x \\
f_{1/2}^\prime &   &   & \searrow            \\
  &   \searrow &  ^2v  &\longrightarrow &  y \\
\end{array}\\
\qquad\qquad\qquad\ \ \Rightarrow\cfrac{\partial f_{k}^\prime}{\partial y}=(\mathrm{e}^x\cos y)f_{k1}^{\prime\prime}+2yf_{k2}^{\prime\prime}\qquad(k=1/2)
\end{array}
$$
第三部分，根据第二部分的结果写出答案
$$
\begin{aligned}
\cfrac{\partial ^2z}{\partial x\partial y}
&=(\mathrm{e}^x\cos y)f_1^\prime+\mathrm{e}^x\sin y(\mathrm{e}^x\cos yf_{11}^{\prime\prime}+2yf_{12}^{\prime\prime})+2x(\mathrm{e}^x\cos yf_{21}^{\prime\prime}+2yf_{22}^{\prime\prime})\\
&=(\mathrm{e}^x\cos y)f_1^\prime+\mathrm{e}^{2x}\sin y\cos yf_{11}^{\prime\prime}+4xyf_{22}^{\prime\prime}+2\mathrm{e}^x(y\sin y+x\cos y)f_{12}^{\prime\prime}
\end{aligned}
$$

```
z=f(x,y)，f具有二阶连续偏导数-> f12’’=f21’’ 充分不必要！
```

### 多元函数的极值和最值
可疑点$(x_0,y_0)\left\{\begin{array}{l}f_x^\prime(x_0,y_0)=0\\f_y^\prime(x_0,y_0)=0\end{array}\right.$  

记$\left\{\begin{array}{l}f_{xx}^{\prime\prime}(x_0,y_0)=A\\f_{xy}^{\prime\prime}(x_0,y_0)=B\\f_{yy}^{\prime\prime}(x_0,y_0)=C\end{array}\right.$，则$\ \Delta=B^2-AC\left\{\begin{array}{l}<0\Rightarrow\text{极值}\left\{\begin{array}{l}A<0\Rightarrow\text{极大值}\\A>0\Rightarrow\text{极小值}\end{array}\right.\\>0\Rightarrow\text{非极值}\\=0\Rightarrow\text{Undefined.}\end{array}\right.$

#### 无条件极值1/2-隐函数

#### 无条件极值2/2-显函数

#### 闭区域边界最值

#### 闭区域最值

