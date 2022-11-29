# Study-of-Equations-in-Bounded-Decimal-Set
In the real life problem, people may need a number that round to some decimal place, when analytical solution is not available. For example, there are no analytical solution for general six-degree equations. In this case, we may try to have numerical value by other means. But whatever a value we have, it is a 10-based rational number. Therfore, I would like to formulate the theory of solution of equations here. 


Definition of Decimal Space: $D_l$ is defined to be all decimals to $l$-decimal space. \
For example, $-0.1 \in \mathbb{D} _1$ but $0.11 \notin \mathbb{D} _1$  \

Manifestly, if the solution space is bounded, we could have finite solutions.



# Equations that solutions are located in decimal set
Example:
$-0.0001 \leq e^{x_1} + x_1^3 - 7 \leq 0.0001$, \
$x_1 \in \mathbb{D} _2$, \
The solution is $1.42$.


Example 2:

$$
\begin{cases}x_1 \in \mathbb{D}_4  \\
-0.0001 \leq e^{x_1} + x_1^3 - 7 \leq 0.0001
\end{cases} 
$$


The solution is $1.42$ , $1.4199$

Example 3:
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

What conclusion can we draw from example 2 and 3? Indeed, sometimes there could be no solutions in decimal space for strictly equality. This is because the solution may be an irrational number and therefore you could never represent it as a decimal. Also, if the solution is something like 1/3, you cannot interpret it as a decimal as well. Both of the cases prompt us to relax our restriction of equalities. \\

For example, when you are trying to find the solution of $e^x = 5$, it is impossible for you to find a decimal solution. You may argue that we can do that by binary search and some other methods, which gives the value $1.6094379124341$. But you should think carefully, whether it is a solution? It seems not, as e^1.6094379124341 = 4.999999999......, rather than exactly 5. So analytically, this is not a solution. \\

DO NOT BE UPSET! If you insist on looking for a solution in decimal space, it must be impossible as the solution must be an irrational number. You have two choice for now: 1. Try to construct an analytical solution, based on the existing theory or new-created one. 2. Relax the equality to have solutions in decimal space. \\

We only discuss about the second one. For example, although $e^x = 5$ has no solution, but $\epsilon_1 \leq e^x -5 \leq \epsilon_2$ could has solution, where $\epsilon_1$ and $\epsilon_2$ are given relaxation, according to your requirement. Then you could have some solutions for new-formulated problem. \

But you should be very careful here, as the solution set of original non-relaxed problem is still empty. Only the relaxed problem has solution. Essentially, the new problem and original problem are two different problems. You need to be careful here.

# More application in solving transcendental equation

$$
\begin{cases}
x_1 \in \mathbb{D} _4 \\
abs(sin(x) + x) - 2 = 0\\
-5 \leq x_1 \leq 5 \\
-5 \leq x_2 \leq 5 \\
\end{cases}
$$

Indeed, there are no solution for this problem, even if you extend 4 to 5,6... and even 1000000.
Although binary search method yields result -1.1061, this is still not a solution as abs(sin(x) + x) - 2 = 5.769838102720470e-05 $\neq$ 0.
But if you relax and formulate another problem:

$$
\begin{cases}
x_1 \in \mathbb{D} _4 \\
-0.0001 \leq abs(sin(x) + x) - 2 \leq 0.0001 \\
-5 \leq x_1 \leq 5 \\
-5 \leq x_2 \leq 5 \\
\end{cases}
$$

Then in this case, the result -1.1061 given by binary search is a solution. 
