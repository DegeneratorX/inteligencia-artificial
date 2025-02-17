## Questão 1

Deseja-se obter o modelo de regessão linear para os seguintes dados:

| x_1  | x_2 | y |
|---|---|---|
| 0 | 1 | 3 |
| 1 | 2 | 6 |
| 2 | 2 | 7 |
| 3 | 1 | 8 |
| 4 | 2 | 11 |

Calcule os coeficientes da regessão.

### Resposta

$$
Y = \begin{bmatrix}
3 \\
6 \\
7 \\
8 \\
11
\end{bmatrix}
$$

$$
X = \begin{bmatrix}
1 & 0 & 1 \\
1 & 1 & 2 \\
1 & 2 & 2 \\
1 & 3 & 1 \\
1 & 4 & 2
\end{bmatrix}
$$

$$w = (X^T X)^{-1} X^T Y$$

Bora calcular $X^TX$.

$$
X^T X = \begin{bmatrix}
5 & 10 & 8 \\
10 & 30 & 17 \\
8 & 17 & 14
\end{bmatrix}
$$

Calculo a inversa disso:

$$
(X^T X)^{-1} = \begin{bmatrix}
\frac{131}{11} & \frac{-3}{22} & \frac{-4}{11} \\
\frac{-4}{55} & \frac{23}{220} & \frac{-1}{11} \\
\frac{-14}{11} & \frac{-1}{22} & \frac{10}{11}
\end{bmatrix}
$$

Agora calculo $X^T Y$

$$
X^T Y = \begin{bmatrix}
1 & 1 & 1 & 1 & 1 \\
0 & 1 & 2 & 3 & 4 \\
1 & 2 & 2 & 1 & 2
\end{bmatrix} \cdot 
\begin{bmatrix}
3 \\
6 \\
7 \\
8 \\
11
\end{bmatrix} =
Y = \begin{bmatrix}
35 \\
88 \\
59 
\end{bmatrix}
$$

E por fim faço o w, já que tenho $X^T X$ e $X^T Y$

$$
w = \begin{bmatrix}
35 \cdot \frac{131}{11} & 88 \cdot \frac{-3}{22} & 59 \cdot \frac{-4}{11} \\
35 \cdot \frac{-4}{55} & 88 \cdot \frac{23}{220} & 59 \cdot \frac{-1}{11} \\
35 \cdot \frac{-14}{11} & 88 \cdot \frac{-1}{22} & 59 \cdot \frac{10}{11}
\end{bmatrix}
$$

Portanto

$$
w = \begin{bmatrix}
\frac{4217}{11} \\
\frac{284}{220} \\
\frac{56}{11} 
\end{bmatrix}
$$

