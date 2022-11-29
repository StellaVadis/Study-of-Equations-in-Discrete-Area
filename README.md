# Study-of-Equations-in-Bounded-Decimal-Set
In the real life problem, people may need a number that round to some decimal place, when analytical solution is not available. For example, there are no analytical solution for general six-degree equations. In this case, we may try to have numerical value by other means. But whatever a value we have, it is a 10-based rational number. Therfore, I would like to formulate the theory of solution of equations here. \


Definition of Decimal Set: $D_l$ is defined to be all decimals to l-decimal place. \
For example, $-0.1 \in \mathbb{D} _1$ but $0.11 \notin \mathbb{D} _1$

# Equations that solutions are located in decimal set
Example:
$-0.0001 \leq e^{x_1} + x_1^3 - 7 \leq 0.0001$, \
$x_1 \in \mathbb{D} _2$, \
The solution is $1.42$.


Example:

$$
\begin{cases}x_1 \in \mathbb{D}_4  \\
-0.0001 \leq e^{x_1} + x_1^3 - 7 \leq 0.0001
\end{cases} 
$$


The solution is $1.42$ , $1.4199$

Example:
$e^{x_1} + x_1^3 - 7 = 0$, \
$x_1 \in \mathbb{D} _4$, 
There are no solutions.

Example:

$$
\begin{cases}
x_1, x_2 \in \mathbb{D} _1 \\
x_1 + x_2 = 4 \\
2x_1 + 3x_2 = 6 \\
\end{cases}
$$


Example:

$$
\begin{cases}
x_1,x_2 \in \mathbb{D} _1 \\
x_1 =  x_2 \\
0 \leq x_1 \leq 1 \\
0 \leq x_2 \leq 1
\end{cases}
$$

The solutions are: $(0,0),(0.1,0.1),(0.2,0.2),(0.3,0.3),(0.4,0.4),(0.5,0.5),(0.6,0.6),(0.7,0.7),(0.8,0.8),(0.9,0.9),(1,1)$



Example: $x_1, x_2 \in \mathbb{D} _1$, \
$x_1^2 + x_2^2 = 1$, \
$x_1 \geq 0 $, \
$x_2 \geq 0$, \
The solutions are $(1,0),(0,1),(0.8,0.6),(0.6,0.8)$


Example:

$$
\begin{cases}x_1 \in \mathbb{B}_{12}  \\
-0.001 \leq e^{x_1} + x_1^3 - 7 \leq 0.001 \\
0 \leq x_1 \leq 2
\end{cases} 
$$


Solution:  $x_1 = 1.42001953125$
