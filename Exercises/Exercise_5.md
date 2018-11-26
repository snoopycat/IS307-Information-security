# Exercise_5

#### 1.

$$
\begin{eqnarray}
ab &=& x(2^n+1) + y\\
&=& x*2^n + x + y\\
\end{eqnarray}
\\|y| < 2^n+1
$$

so there are two  situations:

1) y $ \geq $ 0
$$
\begin{eqnarray}
ab \mod 2^n+1 &=& y\\
ab \mod 2^n+1 &=& ab\mod 2^n - ab \vert 2^n \\
&=& x+y-x\\
&=& y
\end{eqnarray}
$$

Proved.

2) y  < 0
$$
\begin{eqnarray}
ab \mod 2^n+1 &=& (x-1)(2^n+1) + 2^n+1-y \mod 2^n+1\\
&=& 2^n+1 -y\\
ab \mod 2^n+1 &=& ab \mod 2^n - ab\vert2^n + 2^n+1\\
&=& x+y-x+2^n+1\\
&=& 2^n+1-y

\end{eqnarray}
$$
Proved.

#### 2.

The input is $X_1, X_2, X_3, X_4$, and the output is $Y_1, Y_2, Y_3, Y_4$.

We have to prove that 
$$
X_1, X_2, X_3, X_4 = In(Y_1, Y_2, Y_3, Y_4)
$$
We have
$$
\begin{equation}
\left\{
    \begin{array}{lr}
    Y_1 = X_1\oplus X_5 &  \\
    Y_2 = X_2\oplus X_6\\
    Y_3 = X_3\oplus X_5\\
    Y_4 = X_4\oplus X_6\\
    X_5,X_6 = MA(X_1\oplus X_3, X_2 \oplus X_4)
    \end{array}
\right.
\end{equation}
$$
So
$$
Y_1 \oplus Y_3 = X_1 \oplus X_3, Y_2 \oplus Y_4 = X_2 \oplus X_3\\ X^{'}_5,X^{'}_6 = MA(Y_1 \oplus Y_3, Y_2 \oplus Y_4)\\
\Rightarrow X^{'}_5,X^{'}_6 = X_5, X_6
$$

$$
Y^{'}_1 = Y_1 \oplus X^{'}_5 = X_1 \oplus X_5 \oplus X_5 = X_1
$$

Similarly, $Y^{'}_2 = X_2$, $Y^{'}_3 = X_3$, $Y^{'}_4 = X_4$

Finally
$$
X_1, X_2, X_3, X_4 = In(Y_1, Y_2, Y_3, Y_4)\\
X_1, X_2, X_3, X_4 = In(In(X_1, X_2, X_3, X_4))
$$
