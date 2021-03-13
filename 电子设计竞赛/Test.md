# 高数笔记
## 第一讲 预备知识
### 题目01
> 已知$f(x)=\ln{(x+\sqrt {x^2+1})}$，求$f^{-1}(x)$及其定义域

#### 扩展1:
公式扩展
$$
\sqrt a-\sqrt b=\cfrac{a-b}{\sqrt a+\sqrt b}
$$
证明$f(x)=\ln{(x+\sqrt {x^2+1})}$为奇函数
$$
f(-x)=\ln {(-x+\sqrt{x^2+1})}=\ln{\cfrac{1}{x+\sqrt{x^2+1}}}=-f(x)
$$
#### 扩展2:
反双曲正弦函数
$$
\sinh{^{-1}x}=f(x)=\ln{(x+\sqrt{x^2+1})}
$$
导数
$$
f^\prime(x)=\cfrac{1}{\sqrt{x^2+1}}
$$
导数的原函数
$$
\int_{}^{}\cfrac{1}{\sqrt{x^2+a^2}}\,dx=\ln{(x+\sqrt{x^2+a^2})+C}
$$
双曲正弦函数
$$
\sinh x=\cfrac{e^x-e^{-x}}{2}
$$
#### 扩展3:
双曲余弦函数(**悬链线**)
$$
\cosh x=\cfrac{e^x+e^{-x}}{2}
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
 a^3-b^3=(a-b)(a^2+ab+b^2) 
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
#### 定义
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

#### 推论(戴帽法)

$$
\left.\begin{array}{r}
a_n>0  \\ 
\exists n>N,\lim\limits_{n\to\infty}{a_n}=a 
\end{array}\right\} \Rightarrow a\ge 0
$$
```
戴帽法有等号(a>=0)！脱帽法没有等号！
```

###  运算规则
```
只需注意极限必须先存在才可以进行运算！
```
### 夹逼准则
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

>求极限$$
\lim_{n\to\infty}{\left(\cfrac{1}{n^2+n+1}+\cfrac{2}{n^2+n+2}+\cdots+\cfrac{n}{n^2+n+n}\right)}
$$
### 单调有界准则
单调有界数列必有极限。即若数列$\{x_n\}$单调递增(递减)，且有上界(下界)，则$\lim\limits_{n\to\infty}{x_n}$存在  
