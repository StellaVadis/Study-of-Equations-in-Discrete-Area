# Study-of-Equations-in-Bounded-Decimal-Set
In the real life problem, people may need a number that round to some decimal place, when analytical solution is not available. For example, there are no analytical solution for general six-degree equations. In this case, we may try to have numerical value by other means. But whatever a value we have, it is a 10-based rational number. Therfore, I would like to formulate the theory of solution of equations here. 


Definition of Decimal Space: $D_l$ is defined to be all decimals to $l$-decimal space. \
For example, $-0.1 \in \mathbb{D} _1$ but $0.11 \notin \mathbb{D} _1$  \

Manifestly, if the solution space is bounded, we could have finite solutions.

# Definition and Symbols

 If r is a real number, then r_{(n)} means round to n-th decimal place.  \
 For example, if r is $\pi$ , then $r_{(4)} = 3.1416$. This gives us a clear definition when refering to some numbers. \
 Based on the given example $\pi$: \
 $r$ is defined to be symbol of this real number. \
 $r_{(4)}$ is defined to be the round symbol of this real number. \
 $\pi$ is defined to be analytical value of this real number. \
 $3.1416$ is defined to be the decimal rounding value of this real number. \
 Therefore, we can say that the 4-th decimal rounding value of $r$ is $3.1416$.
 

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


Example: $x_1, x_2 \in \mathbb{D} _1$, \
$x_1^2 + x_2^2 = 1$, \
$x_1 \geq 0 $, \
$x_2 \geq 0$, \
The solutions are $(1,0),(0,1),(0.8,0.6),(0.6,0.8)$

Example: $x_1, x_2 \in \mathbb{D} _4$, \
$0.7999 \leq \int_{t = 0}^{t = x_1} e^{-t^2}dt \leq 0.8$, \
$0 \leq x_1 \leq 2 $, \

Solution: $x_1 = 1.1721, 1.1722,1.1723,1.1724$.

Example: 

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
-0.0001 \leq abs(sin(x_1) + x_1) - 2 \leq 0.0001 \\
-5 \leq x_1 \leq 5 \\
\end{cases}
$$

Then in this case, the result -1.1061 given by binary search is a solution. This is a good method of relaxing equations: Solve with binary search and add some relaxtion based on the searched results. To see whether you could accept it. But this does not always works, as something can not be relax on both sides. For example, the height of a person, the mass of an object. In this case, although some numerical method like binary search yields a solution. For example, it yields that the mass of a box is $-0.00000001$. Although theoretically you can relax the $x > 0$ to be $x > -0.00001$, to formulate a new problem. But in reality, this relaxation is not understandable. And therefore, your numerical method does not work.


# Bisection Method application in searching for one-variable-relaxed function
If the equation is strict, then that is the same as the original method. But we cannot make sure that the exact solution can be found. \
If that is not equation but inequality, we can find a solution by implementing bisection method to any value (rational or irrational are both acceptable), in the given interval. Then the solution may be acceptable. 

$$
\begin{cases}
x_1 \in \mathbb{D} _4 \\
-0.0001 \leq abs(sin(x_1) + x_1) - 2 \leq 0.0001 \\
-5 \leq x_1 \leq 5 \\
\end{cases}
$$

For example, you can choose $abs(sin(x_1) + x_1) - 2 = 0$, such that the solution will be $x_1 = -1.1061$, and $abs(sin(x) + x) - 2 = 5.769838102720470e-05$, and $-0.0001 \leq 5.769838102720470e-05 \leq 0.0001$. Therefore,  $x_1 = -1.1061$ is a solution of this equations.  \
You can also choose $abs(sin(x_1) + x_1) - 2 = 0.00005$, such that the solution will be $x_1 = -1.1061$, and $abs(sin(x) + x) - 2 = 5.769838102720470e-05$, and $-0.0001 \leq 5.769838102720470e-05 \leq 0.0001$. Therefore,  $x_1 = -1.1061$ is a solution of this equations.  \
But this does not guarantee that for all selected value $\lambda$ between $(-0.0001,0.0001)$ can yield a possible solution. But this can be guaranteed when $l$ in $D_l$ can be as large as you want(not infinity). Since $\lambda < 0.0001$, then the value obtained by bisection method can be closer and closer to the $\lambda$ when iteration continues. And therefore, the function value would finally drop in the interval $(-0.0001,0.0001)$. I will prove it rigorously when I have time. \
For any $\lambda$ between $(-0.0001,0.0001)$ chosen and be applied to the bisection method can yield a possible solution when $l$ is adequately large. But since $l$ is pre-specified, some of the generated $x_1$ may not be a solution. If you really want to secure all possible values, you should use grid search method instead. 

Example:


$$
\begin{cases}
x_1 \in \mathbb{D} _2 \\
-0.0001 \leq 2^x - 3 \leq 0.0001 \\
0 \leq x_1 \leq 2 \\
\end{cases}
$$

Denote $f(x) = 2^x - 3$: \
Step 0: \
f(0) = -3 < 0 \
f(2) = 1 > 0\
Step 1: \
f(1) = -1 < 0 \
Step 2: \
f(1.5) = 2^1.5 - 3 < 0 \
Step 3: \
f(1.75) = 2^1.75 - 3 > 0\
Step 4: \
f(1.625) = 2^1.625 -3 >0 \
Step 5: \
f(1.5625) = 2^1.5625 - 3 < 0\
Step 6: \
f(1.59375) = 2^1.59375 - 3 > 0\
Step 7: \
f(1.578125) = 2^1.578125 - 3 < 0\
Step 8: \
f(1.5859375) = 2^1.5859375 - 3 > 0\
Step 9: \
f(1.58203125) = 2^1.58203125 -3 <0 \
Step 10: \
f(1.580078125) = 2^1.580078125 -3 <0 \
We can stop here , as the second decimal place does not change anymore. The candidate solution is located in $[1.580078125,1.5859375]$. \
But what we need is a solution in $\mathbb{D} _2$. We may use $1.58$ as a candidate. \
But $abs(2^1.58 - 3) = 0.010301502730123 > 0.0001$, this is not a solution. You need to test $f(x) = 2^x - 3 + \epsilon$, this may yields a solution. \
Or it can have no solutions at all.

# Solution for polynomials in Decimal Space

$$
\begin{cases}
x_1 \in \mathbb{D} _{3} \\
-0.0001 \leq x_1(x_1-1)(x_1-2) \leq 0.0001 \\
-1 \leq x_1 \leq 3 \\
\end{cases}
$$

Since you do not have analytical solution for high-order polynomial, so we do not use formula for quadratic equations here. We propose a more general method. \
Take $f(x) = x_1(x_1-1)(x_1-2) - 0$, you may use differential analysis to tackle to problem. \
At first, we can take difference until the end. \
$f^{(1)} = 3x^2-6x + 2$ \
$f^{(2)} = 6x - 6$ \
$f^{(3)} = 6 $.

Then we can trace back and figure out the positivity and negativity of these difference. \
Step 1: \
Since $f^{(3)} = 6 >0 $, therefore, $f^{(2)}$ is increasing in the interval $[-1,3]$. \
$f^{(2)}(-1) = -12$ and $f^{(2)}(3) = 12$. \
Since it is monotonically increasing in the interval [-1,3], and there are altervative sign at the bound, there must be exactly one solution in $[-1,3]$. \
We can use the bisection method or other numerical method to locate the value. Here, we can find that it is $r_0$, $1.0000000000$ or $0.99999999$ or so on. You can choose the decimal however long you want, because this is not the final descision solution of x, just a temporary value. 
