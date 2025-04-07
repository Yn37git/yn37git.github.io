---
layout: post
title: Partitions functions 
date: 2015-10-20 11:12:00-0400
description: a concise introduction
---

## Partitions
 ---
A partition of a positive integer \(n\) is a finite nonincreasing
sequence of positive integers : 
$$ (\lambda_1,\lambda_2,\dots,\lambda_r) \text{ such that } 
\sum_{i=1}^r \lambda_i =  n.$$
where \( \lambda_i\)'s  are called the parts of the partition 

 
The partition function \( p(n) \) is the number of partitions
of \( n \)
for example: 
\[
\begin{align*}
p(1) &= 1: 1=(1);\\
p(2) &= 2: 2 = (2), 1 + 1 = (1^ 2 );\\
p(3) &= 3: 3 = (3), 2 + 1 =(12), 1 + 1 + 1 = (1^3);\\
p(4) &= 5: 4 = (4), 3 + 1 =(13), 2 + 2 = (2^2),2 + 1 + 1 = (12^2), 1 + 1 + 1 + 1 = (1^4 );\\ 
\end{align*} 
\]

The partition function \(p(n)\) increases quite rapidly with \(n\). For example, p(10) =
42, p(20) = 627, p(50) = 204226, p(100) = 190569292, and p(200) =
3972999029388.

---
## Basic q series representations
---
- we define \((a;q)_n=(1-a)(1-aq)\dots (1-aq^{n-1})\)
this it is a type of Pochhammer notation of shifted factorial extended to base '\(q\)'
- also \((q;q)_n=(1-a)(1-aq)\dots (1-q^{n})\) which is a very tipical notation 
- if \(f_k=(q^k;q^k)_\infty=(1-q^k)(1-q^{2k})\dots(1-q^{nk})\dots\)
---
now from partition theory we have:
-  if \(p(n)\) reprents the number of integer partitions of a non negative integer n then :

$$
\begin{align*}
\sum_{n=0}^\infty p(n)q^n &= \frac{1}{(q;q)_\infty}=\frac{1}{f_1}\\
\qquad &=(1-q)^{-1}(1-q^2)^{-1}\dots(1-q^n)^{-1}\dots \\ 
\qquad &= (1+q+q^2+q^3+\dots+q^n+\dots)(1+q^2+q^4+q^6+\dots+q^2n+\dots)\\
&\quad \dots(1+q^n+q^{2n}+q^{3n}+\dots)\dots
\end{align*}
$$ 

  ( these expansions holds for \(|q|<1\) )
- when this last equation is restricted to say \(q^m\) terms and no more, we can then expand and find coefficients of the terms to get \(p(m)\) or other less terms (\(<m\)) 
---
## restricted partitions  
---

- a \(\; l-regular\) partition of n is partition of n in which no part is a multiple of \(l\) (a positive integer)
- which in \(q\) series can be represented as:
- if \(p_l(n)\) reprents the number of integer partitions of a non negative integer n in which no part is divisible by \(l\) then we have :   

$$
\begin{align*}
\sum_{n=0}^\infty p_l(n)q^n &= \frac{(q^l;q^l)_\infty}{(q;q)_\infty}=\frac{f_l}{f_1}\\
\qquad &=(1-q)^{-1}(1-q^2)^{-1}\dots(1-q^{l-1})^{-1}(1-q^{l+1})^{-1}\\
&\quad \dots (1-q^{2l-1})^{-1}(1-q^{2l+1})^{-1}\dots\\ 
\qquad &= (1+q+q^2+\dots)(1+q^2+q^4+\dots)\dots\\
&\quad (1+q^{l-1}+q^{2(l-1)}+\dots)(1+q^{l+1}+q^{2(l+1)}+\dots)\dots
\end{align*}
$$

---
- a \((l,j)-regular\) partition of n is partition of n in which no part is a multiple of \(l\) or \(j\)  
(which are  positive integer and co-prime i.e \(gcd(l,j)=1\))
- which in \(q\) series can be represented as:
- if \(p_{l,j}(n)\) reprents the number of integer partitions of a non negative integer n in which no part is divisible by \(l\) or \(j\) , \(gcd(l,j)=1\) then we have 

$$\begin{align*}
\sum_{n=0}^\infty p_{l,j}(n)q^n &= \frac{(q^l;q^l)_\infty (q^j;q^j)_\infty}{(q;q)_\infty (q^{jk};q^{jk})_\infty}
\qquad = \frac{f_l f_j}{f_1 f_{lj}}\\
\qquad &= (1-q)^{-1}(1-q^2)^{-1}\dots(1-q^{l-1})^{-1}(1-q^{l+1})^{-1}\dots (1-q^{j-1})^{-1}(1-q^{j+1})^{-1}\dots\\
\qquad &= (1+q+q^2+\dots)(1+q^2+q^4+\dots)\dots(1+q^{l-1}+q^{2(l-1)}+\dots)\\
&\quad(1+q^{l+1}+q^{2(l+1)}+\dots)\dots
     (1+q^{j-1}+q^{2(j-1)}+\dots)(1+q^{j+1}+q^{2(j+1)}+\dots)\dots
\end{align*}
$$ 

---
## Colored paartitions
---
- Now clearly to create a partition of \(n\) parts \((\lambda_i)\) are chosen from \(N\) (set of natural numbers = 1,2,3,...)
let this set of parts to be chosen represented by \(S\) then:
  - for  partition of \(n\) \(S=N\)
  - for \(l-regular\) partition of \(n\) \(\; S = N - l \; N = \{1,\dots ,l-1,l+1,\dots,2l-1,2l+1,\dots\} 
  - for \((l,m)-regular\) partition of \(n\) \(\; S = N - l \; N - m \; = \{1,\dots ,l-1,l+1,\dots,m-1,m+1,\dots\}\)
- Now if \(S=N^s=\{1,1,\dots,2,2,\dots\}\) i.e. each part is repeated s times and each part is disrtinct from other 
- for our convinivence and without loss of generality! we give each of this distinct part a color like 
\(1_r\) is 1 with red color, \(1_b\) is one with blue color etc
- from above we have \(N^s={1_r,1_b,\dots,2_r,2_b,\dots} \) i.e.each part has \(s\) distinct colors and is unique.

  
  
  
  
  

