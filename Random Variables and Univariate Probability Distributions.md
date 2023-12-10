# Random Variables and Univariate Probability Distributions

## Random Variables
✅ It is inconvenient to work with different sample spaces. To develop a **unified** probability theory, we consider a **mapping** $X$ from the original sample space $S$ to a new sample space $\Omega$ which consists of **a set of real numbers**.This transformation $X:S \to \Omega$ is called a random variable.
> The nature of random variable is a function or a map

✅ In many applications, we may be interested only in some particular aspect of the outcomes of an experiment, rather than the outcomes themselves. $A$ suitably defined random variable $X$ will better serve for our purpose.

### Defination of Random Variable
**[💬 Definition 1. Random Varible]**  A random variable,$X(\cdot )$, is a $\mathbb{B}$-measurable mapping (or point function) from the sample space $S$ to the real line $\mathbb{R}$ such that for each outcome $s \in S$, there exists a corresponding unique real number, $X(s)$. The collection of all possible values that the random variable $X$ can take, also called the range of $X(\cdot )$,constitutes a new sample space, denoted as $\Omega$.

::: {.callout-important}

$$
X:S \to \Omega \text{ need not be 1-1 mapping. \\
It is possible that }X(s_1) = X(s_2)
$$

Convention:A capital letter $x$ denotes a random variable,and a lowercase letter $x$ denotes its realization,i.e., a possible value that random variable $X$ can take (i.e., $x =X(s)$for $a$ given $s \in S$).

:::

🌰:When we throw a coin, the sample space $S = \{ H,T \}$. Define a random variable $X(\cdot )$ by $X(H) =1 $ and $X(T) = 0$. Then we obtain a new sample space $\Omega = \{ 1,0 \}$ 

For the election of a candidate, the sample sapces $S = \{ Win,Fail \}$. Define a random variable $X(\cdot )$ by $X(Win) =1 $ and $X(Fail) = 0$. Then we obtain a new sample space $\Omega = \{ 1,0 \}$

So it is not necessary to have the same number of basic outcomes for both $S\text{ and } \Omega$ 

Suppose we throw three fair coins.Then the space sample $S=\{TTT,TTH,THT,HTT,HHT,HTH,THH,HHH\}$ Let $X(\cdot)$ be the number of heads shown up.Then $X(TTT)= 0,$$X(TTH)=1,$$X(THT)=1,$$X(HTT)=1,$$X(HHT)= 2,$$X(HTH)=2,$$X(THH)2,$$X(HHH)=3$.We have $\Omega = \{ 0,1,2,3 \}$.

Suppose $S = \{ s:-\infty < s < +\infty \}$. Define $X(s) = 1$ if $s > 0$ and $X(s) = 0$ if $s \le 0$

> Here $X$ is called binary random variable because there are only two possible values $X$ can take.The binary variable has wide applications in economics.


There are many other examples of random variables, including
- subjective well-being
- sentiment index of investoers
- economic policy uncertainty(EPU) index

These indices are usually constructed based on *text data* from social media platforms (e.g.,WeChat,Facebook)and news media.Text data are an unstructured form of *Big data*.

---

### Probability Function of the new sample space $\Omega$

The probability function defined on the original sanple space $S$ can be uesd to obtain the probability function of the new sample space $\Omega$.

First suppose space $S$ has a finite number of basic outcomes 

$$
S = \{ s_1,s_2, \ldots ,s_n \}
$$

with a probability function $P:\mathbb{B} \to [0,1]$, where $\mathbb{B}$ is a $\sigma$-field associated with $S$. Define a random variable $X(\cdot ) : S \to \mathbb{R}$ by $X(s_i) = x_i$ for $i = 1,2,\ldots ,n$ Then the new sample space $\Omega$ is given by

$$
\Omega \{ x_1, \ldots ,x_m \}
$$

where $m$ may not be the same as $n$. 

Then the probability function $P_{X}:\Omega \to \mathbb{R}$ for $X$ can be obtained as 

$$
P_{X}(x_i) \equiv P(X = x_i) = P(C_i)
$$

where $C_i$ is an event in $S$ such that:

$$
C_i = \{ s \in S : X(s) = x_i \}
$$

$P_{X}(\cdot )$ is **induced** probability function on the new sample space $\Omega$, obtained from the original probability function $P(\cdot )$

More formally, for any set $A \in \mathbb{B}_{\Omega}$,where $\mathbb{B}_{\Omega}$ is a $\sigma$-field generated from $\Omega$, we can define a probability function $P_{X}(\cdot ): \mathbb{B}_{\Omega} \to \mathbb{R}$ on $\Omega$ as follows:
$$
P_{X}(A) = P(C_{A}) = P[s \in S : X(s) \in A]
$$

where $C_{A} = \{ s \in S:X(s) \in A \}$, which is an equivalent event in $S$.

Now we complete the transformation from the original measurable space $(S,\mathbb{B},P)$ to the new space $(\Omega,\mathbb{B}_{\Omega},P_X)$.

**💬 Definition 3.2 Measurable Function** A function $X:S \to \mathbb{R}$ is $\mathbb{B}$-measurable(or measurable with respect to the $\sigma$-field $\mathbb{B} $ generated from $S$) if for every real number $a$, the set $\{ s \in S : X(s) \ge a \} \in B$ 

- A $\mathbb{B}$-measurable function is simply called a measurable function.(if it dose not cause any confusion)
- A measurable function ensures that $P(X \in A)$ is always well-defined for all subsets $A$ in $\mathbb{B}_{\Omega}$
- If $X(\cdot )$ is not measurable, then there exist subsets in the $\sigma$-field in $\mathbb{R}$ for which probability are not defined .
- In this doc, the term "random variable" is restricted to being a $\mathbb{B}$-measurable function from $S$ to $\mathbb{R}$

**⚖️Theorem 3.1** Let $\mathbb{B}$ be a $\sigma$-algebra associated with sample spaces $S$.Let $f(\cdot )$ and $g(\cdot )$ be $\mathbb{B}$-measurable real valued functions, and $c$ be a real number.Then the function $f(\cdot ) + g(\cdot )$,$cf(\cdot )$,$f( \cdot )\cdot g( \cdot  )$,$\left\vert f( \cdot  ) \right\vert$are also $\mathbb{B}$-measurable.

> if function $X( s )$ and $Y( s )$ are measurable mappings from $S$ to $\Omega$, then the ordinary algebraic operations on $X( s )$ and $Y( s )$ will produce new measurable mappings.
> - $aX( s )$
> - $X( s ) + Y( s )$
> - $X( s )Y( s )$ and $\frac{X( s )}{ Y( s )}$

⁉️️ The induced probability function $P_{x}( \cdot  )$ satisfies the three axioms of the probability function?

::: {.callout-tip}

- Condition ( 1 )
$$
1 \ge P_{X}(x_i) = P(X = x_i) = P(C_i) \ge 0
$$

given $0 \le P( C_{A} ) \le 1$ for any $C_{A} \in \mathbb{B}$, where $\mathbb{B}$ is a $\sigma$-field associated with $S$.

- Condition ( 2 )
$$
P_{X}( \Omega ) = P( S ) = 1
$$

- Condition ( 3 )

consider two mutually exclusive events $A_1$ and $A_2$ in $\mathbb{B}_{\Omega}$, a $\sigma$-field generated from $\Omega$. Here, the induced probability of $A_1 \cap A_2$ is given by
$$
P_{X}( A_1 \cap  A_2 ) = P( C )
$$

where $C = \{ s\in S: X( s ) \in A_1 \cap A_2 \}$

However, we can also write 
$$
C = \{ s \in S : X( s ) \in A_1 \} \cap \{ s \in S : X( s ) \in A_2 \} \\
= C_1 \cap C_2
$$

The fact that $A_1$ and $A_2$ are disjoint implies that $C_1$ and $C_2$ are also disjoint. It follows that

$$
P_{x}( A_1 \cap A_2  ) = P( C_1 ) + P( C_2 ) \\
= P_{x}( A_1 ) + P_{X}( A_2 )
$$
:::

In the rest, we will abuse the notations for the original probability function $P( \cdot  )$ and the induced probability function $P_{X}( \cdot  )$; we will denote both probability functions as $P( \cdot  )$


🌰: Suppose we throw three coins. Then the sample space 
$$
S = \{ HHH,HTH,HHT,THH,THT,TTH,HTT,TTT \}
$$

Define a random variable $X( \cdot  )$ to be the number of the heads obtained from the experiment. Then the new sample space, or the range of $X$, is given by 

$$
\Omega = \{ 0,1,2,3 \}
$$

Now, suppose we are interested in calculating the probability that $P( 0 \le X \le 1 )$.Denote 

$$
C = \{ s \in S: 0 \le X( s ) \le 1\}\\
= \{ TTT,TTH,THT,HTT\}
$$

It follows that:
$$
P(0 \le X \le 1 ) = P( C )\\
= \frac{1}{2 }
$$
 

## Cumulative Distribution Function

✅ How to characterize a random variable $X$?

**💬 Definition 3.3 cumulative Distribution Function (CDF)** The cumulative distribution function (CDF) of a random variable $X$ is defined as
$$
F_{X}(x) = P( X \le x ) \text{ for all } x \in \mathbb{R}
$$

**⚖️Theorem 3.2 Properties of $F_{X}( \cdot  )$** Suppose $F_{X}( \cdot  )$ is the CDF of some random variable $X$.

- $\lim_{x \to -\infty}F_{X}( x ) = 0,\lim_{x \to +\infty}F_{X}( x )=1$.
- $F_{X}( x )$ is non-decreasing 
- $F_{X}( x )$ is right-continuous, i.e., for all $x$ and $\delta>0$ ,

$$
\lim_{\delta \to 0^{+}}[F_{X}(x+\delta-F_{X}( x )] = 0
$$

**⚖️ Theorem 3.3** Let $a<b$.Then
$$
P(a<X \le b) = F_{X}( b ) - F_{X}( a )
$$

**⚖️ Theorem 3.4** $P( X > b ) = 1 - F_{X}( b )$

🌰: Suppose $F_1( x )$ and $F_2(x)$ are two CDF's. Is the linear combination $F( x ) = pF_1( x ) +(1-p)F_2(x)$ a CDF?Here p is a constant 

IIF the $0 \le p\le 1$

::: {.callout-tip}
# Mixture of two distributions 

- A mixture of two distributions can provide a great deal of flexibility such as capturing skewness and heavy tails.
- One possibility for a mixed distribution to arise is that in an observed data, some observations are generated from one distribution, and the remaining observations are generated from another distribution.
- Another possibility for a mixed distribution is that there exist two mutually exclusive states,state 1 and state 2 which arise with probabilities p and 1 -p respectively.The random variable $X$ will follow the distribution $F(x)$ when state 1 occurs and will follow distribution $F_2(x)$ when state 2 occurs.Then the distribution $F(x)$of $X$ is
a mixture of distributions $F_1(x)$and $F_2(x)$.
- A well-known example in econometrics is the so-called Markov regime-switching model, which is widely used in macroeconomics and finance, in which $p$ depands on a state variable characterizing the business cycles 

> In practice, $p$ may depend on some economic variables $Z$. An example of $p = p( Z )$ is  
> $$
> p( Z ) = \frac{1}{1 + \exp( - \alpha^{'} Z )}
> $$
:::

**💬 Definition 3.4 Identical Distributions** Two random variables $X$ and $Y$ are identically distributed if for every set $A$ in $\mathbb{B}_{\Omega}$, where $\mathbb{B}_{\Omega}$ is the smallest $\sigma$-field containing all the the intervals of real numbers of the form $( a,b ),[a,b),(a,b],$ and $[a,b]$, one has 
$$
P( X \in A ) = P( Y \in A )
$$

- it is important to note that the identically distribution does not imply $X = Y$, although $X = Y$ implies that $X$ and $Y$ have the same distribution 
- it is not necessary that $X$ and $Y$ are defined on the same sampele space. Only their distributions functions have to coincide.

**⚖️ Theorem 3.5** Let $X$ and $Y$ be two random variables defined on the same sample space $S$.Then $X$ and $Y$ are identically distributed if and only if their CDF's are identical, i.e., $F_{X}( x ) = F_{Y}( x )$ for all $x \in \mathbb{R}$


🌰:the Income distribution, Lorenz Curve and Gini Coefficient

In economics, the Lorenz curve and Gini coefficient are two popular measures of income income inequality.

$$
\text{Gini coefficient} = \frac{A}{A+B}
$$

![Lorenz Curve.png](https://img12.360buyimg.com/ddimg/jfs/t1/237696/1/6774/16003/65732a55F1af7c3da/a83a50b88169c168.jpg){width="50%" fig-align="center"}

It graphically shows that for the bottom $x%$ of households, what percentage $y%$ of the total income they share. Every point on the Lorenz curve represents a statement like "the bottom $20%$ of all households have $10%$ of the total income"

A perfectly equal income distribution would be one in which every household has the same income. In this case, the bottom $x%$ of society would always have $x%$ of the income for all $x \in [0,100]$. This can be depicted by the 45-degree straight line $y=x$, called the "line of the perfect equality"

> In economics, the Gini coefficient is the most commonly used measurement of inequality. It was developed by the Italian statistician and sociologist Corrado Gini in 1912.
> The Gini coefficient is defined based on the Lorenz Curve.The Gini coeffcient can then be thought of as the ratio of the area that lies between the line of equality and the Lorenz curve over the total area under the line of equality
> If all people have non-negative income ( or wealth ), the Gini coefficient can theoretically range from 0( complete equality ) to 1( complete inequality ); it is sometimes expressed as a percentage ranging between 0 and 100
> If negative values are possible ( such as the negative wealth of people with debts ), then the Gini coefficient could theoretically be more than 1.
> Noting that two countries with different income distributions can have the same Gini coefficient

🌰: First Order Stochastic dominance

If two distribution $F( \cdot  )$ and $G( \cdot  )$ satisfy $F( x ) \le G( x )$ for all $x$ on the real line, with strict inequality at least for some $x$, then we say that the distribution $F( \cdot  )$ has first order stochastic dominance over dsitribution $G( \cdot  )$

![First-order Stochastic dominance.png](https://img14.360buyimg.com/ddimg/jfs/t1/237207/11/6550/9586/6573d43bF940d7718/df74dae4a24a35f7.jpg){width="50%" fig-align="center"}

> the first order stochastic dominance is widely used in decision analysis, welfare economics, and finance
> An application of stochastic dominance is to the analysis of income distributions. If $x$ denotes an income level, then the inequality means that the proportion of individuals in distribuion $F( \cdot  )$ with the income less than $x$ is smaller than the proportion of such individuals in $G( \cdot  )$. In other words, there is a higher proportion of poorer people in $G( \cdot  )$ than in $F( \cdot  )$
> Another application:if portfolio $F( \cdot  )$has first order stochastic dominate over portfolio $G( \cdot  )$,then $P_{F}( X > x ) \ge P_{G}( X > x )$ for all $x$;that is,the probability that high returns of portfolio $F( \cdot  )$ is higher than the probability that high returns of portfolio $G( \cdot  )$.

🌰: Second order stochastic Dominance 
A probability distribution $F( \cdot  )$ stochastically domiance another probability distribution $G( \cdot  )$ to second order if, for all $x \in ( -\infty,+\infty )$, 
$$
\int_{-\infty}^{x}F( y )dy \le \int_{-\infty}^{x}G( y )dy,
$$

with strict inequality for at least some $x$. This defination requires the dominant distribution $F( \cdot  )$ to have a smaller area beneath the distribution function for all $x$.

![Second-order stochastic dominance.png](https://img12.360buyimg.com/ddimg/jfs/t1/230010/11/6983/12281/6573d9f7Ff4cd40cb/63960355d61d5e4e.jpg){width="50%" fig-align="center"}

> Risk-averse economic agents will always prefer distribution $F( \cdot  )$ because for any increasing and **concave utility function** $u( \cdot  )$, we have
$$
\int_{-\infty}^{\infty}u( x )dF(x) \ge \int_{-\infty}^{\infty} u( x )dG( x )
$$

if and only if $F( \cdot  )$ has second order stochatic dominance over $G( \cdot  )$

::: {.callout-tip}

Intuitively,economic agents whom prefer more will prefer a first order stochastic dominating distribution,and economic agents who prefer more but are risk-adverse will prefer a second order stochastic dominating distribution.

Higher order stochastic dominance can be defined in a similar way.

The concepts of various stochastic dominances are very useful in characterizing risk behavior of economic agents.There exists a dual relationship between stochastic dominances and classes of utility functions.

Probability theory is a rather useful analytic tool in behavior economics and behavior finance.

:::


## Discrete Random Variables(DRV)
**💬 Definition 3.5 Discrete Random Variable(DRV)** If a random variable $X$ can only take a countable number of values, then $X$ is called a discrete random variable $DRV$.

::: {.callout-tip}
For a discrete random variable $X$, the associate sample space $\Omega$ must countain only a countable number for real number. For example, $\Omega = \{ 1,,2,3,4,5,6 \}$ or $\Omega = \{ 0,1,2, \ldots  \}$
:::

**💬 Definition 3.6 Probability Mass Function(PMF)** The PMF of a DRV is defined as 
$$
f_{X}( x ) = P( X = x ) \\text{for all x } \in \mathbb{R}
$$

**⚖️ Theorem 3.6 Properties of PMF** 
- $0\le f_{X}( x ) \le 1$ for all $x \in \mathbb{R}$
- $\sum_{x \in \Omega}f_{X}( x ) = 1$ 

**💬 Definition 3.7 Support**The collection of the points on the real line $\mathbb{R}$ at which a DRV $X$ has a positive probability is called the support of $X$,denoted as
$$
Support( X ) = \{ x \in \mathbb{R}:f_{X}( x ) > 0 \}
$$
Therefore,we have
$$
Support( X ) = \Omega
$$

We pay attention to the point with the PMF greater than zero. 

> The support of $X$ is the set of all possible values that $X$ can take with strictly positive probability.
> Although $f_{X}( x )$is defined on the entire real line $\mathbb{R}$,it suffices to know the support of a DRV $X$ and the probabilities of all points in the support.
> The PMF fx(x)can be represented graphically via a so-called probability historgram.

**💬 Definition Probability Histogram** A probability histogram is a plot to represent a discrete probability distribution where rectangles are constructed so that their bases of equal width are centered at each value $x$ and their heights are equal to the corresponding probabilities given by the PMF.The bases are constructed so as to have no space between the rectangles.

![probability Histogram.png](https://img12.360buyimg.com/ddimg/jfs/t1/226487/24/6082/10315/6573f47aFba41af59/1f124d39be90b961.jpg){width="50%" fig-align="center"}

**⚖️ Theorem 3.7** Suppose $f_{X}( x )$ is the PMF of the DRV $X$. Then CDF of a DRV $X$
$$
F_{X}( x ) = p( X \le x ) = \sum_{y \le x}f_{X}( y ) \text{ for any x } \in \mathbb{R}
$$

where the summation is over all values $y$ in $\Omega$that are less than or equal to $x$.

::: {.callout-important}

- $F_{X}( x )$ is defined not only in over the Support of $X$, but on the whole real line.

:::
🌰: Suppose a random variable $X$ has the following PMF,
$$
f_{X}( x ) = 
\begin{cases} \frac{1}{N },& x =1,2, \ldots N  \\ 0, &  \text{otherwise}\end{cases}
$$
Find its CDF $F_{X}( x )$

👉🏻: To compute the CDF $F_{X}( x )$,where $x$ ranges from $-\infty \text{to } +\infty$, we divide the real line $\mathbb{R}$ into $N + 1$ intervals:

case 1 : $x <1$. Then the event $\{ X \le x \}$ is an empty set $\emptyset$ and 
$$
F_{X}( x ) = \sum_{x_i \le x}f_{X}( x_i ) = 0
$$

case 2 : $1 \le x < 2$. Then the event $\{ X \le x \} = \{ 1 \}$, and so 
$$
F_{X}( x ) = \sum_{x_i \le x}f_{X}( x_i ) = f_{X}( 1 ) = \frac{1}{N } 
$$

case j :$j-1 \le x < j, 2 \le j\le N$. Then the event $\{ X \le x\} = \{ 1, \ldots ,j-1 \}$, and 
$$
F_{X}( x ) = \frac{j-1}{N }
$$

case N+1 :$x\ge N$ Then the event $\{ X\le x \} = \{ 1, \ldots ,N \}$, and so
$$
F_{X}( x ) = 1
$$

To sumup, we have 

$$
F_{X}( x ) = 
\begin{cases} 0, & x<1 \\ \frac{j}{N }, &  j \le x < j+1, 1 \le j < N \\ 1, & x \ge N \end{cases}
$$

> This function is a step function, where jumps occur ar the points with strictly positive probabilities that is , when jumps occur at the points contained in the support of $X$

**⚖️ Theorem 3.8 ** Suppose $X$ is a DRV with CDP $F_{X}( x )$, and its support contains a squence of points $\{ x_1 <x_2<\cdots \}$ Then its PMF
$$
f_{X}( x_i ) = \begin{cases} F_{X}( x_i ), &  i=1\\ F_{X}( x ) - F_{X}( x_{i-1} ), & i<1  \end{cases}
$$

## Continuous Random Variables
**💬 Definition 3.9 Continuous Random Variable** A random variable $X$ is called contiuous if its distribuiton function $F_{X}( x )$ is continuous for all $x$ in the real line. In contrast, a random variable $X$ is discrete if $F_{X}( x )$ is a step funciton of $x$

![Random Variable.png](https://img10.360buyimg.com/ddimg/jfs/t1/229039/11/6901/12432/6573f75cFe9ff2e00/68ab87742717bfea.jpg){width = "50%" fig-align = "center"}

✅ can we define a PMF $f_{X}( x )$ for a CRV $X$

For any constant $\epsilon > 0 $, $\{ X =x \} \subset \{ x-\frac{\epsilon}{2 }< X \le x + \frac{\epsilon}{2 } \}$

$$
\begin{aligned}
0 &\le P(X = x) \\
&\le P(x-\frac{\epsilon}{2 }< X \le x + \frac{\epsilon}{2 }) \\
&= F_{x}( x+ \frac{\epsilon}{2 } ) - F_{X}( x - \frac{\epsilon}{2 } ) \\
&\to 0 \text{ as } \epsilon \to 0 \\
\end{aligned}
$$
by continuity of $F_{X}( \cdot  )$ Thus 
$$
P( X=x ) = 0 \text{for all} x
$$

- for a CRV $X$, the probability that $X$ takes **a single point is zero**
- Intuition: consider an analogous example of a satellite flying over Mainland China.Suppose it takes one hour for the satellite to fly over Mainland,2 minutes to fly over Fujian,and 0.1 second to fly over Xiamen.It is conceivable that it takes almost zero second for the satellite to
fly over Economic Building at XMU.
- The result that $P(X=x)=0$ for all $x$  for a CRV $X$ has
important implications.For example,
$$
P( a < X \le b) =P( a \le X< b ) \\
= P(a \le X \le B)
$$

**💬 Definition Absolute Continuity(AC)** A function $F: \mathbb{R} \to \mathbb{R}$ is called absolutely continuous with respect to the Lebesgue measure if $F( x )$ is continuous on $\mathbb{R}$ and is differentiable almost everywhere

> What is meant by "almost everywhere" 
> Intuitively,in any finite interval of $\mathbb{R}$,there are a finite number of points or an infinite but countable number of points where $F_{X}( x )$is not differentiable.
> A continuously differentiable function is absolutely continuous.

**💬 Definition 3.10 Probability Density Function(PDF)** Let $X$ be a CRV with absolutely continuous CDF $F_{X}( x )$. If there exists a function $f_{X}( x )$ such that

$$
F_{X}( x ) = \int_{-\infty}^{x}f_{X}( y )dy \text{ for all } x \in \mathbb{R}
$$

The function $f_{X}( x ) :\mathbb{R} \to \mathbb{R}$ is called a probability density function (PDF) of $X$.

In other words, we have 

$$
F^{'}_{X}( x ) = f_{X}( x ) \text{ for almost all } x \in \mathbb{R}
$$

For interpretation of the PDF $f_{X}( x )$, we have,for any small constant $\epsilon > 0$,
$$
\begin{aligned}
&P( x-\frac{\epsilon}{2 }<X \le x + \frac{\epsilon}{2 } ) \\
=& F_{X}( x + \frac{\epsilon}{2 } ) - F_{X}( x - \frac{\epsilon}{2 } ) \\
=& \int_{x-\frac{\epsilon}{2 }}^{x+\frac{\epsilon}{2 }}f_{X}( y )dy \\
=& f_{X}( \bar{x}  ) \epsilon
\end{aligned}
$$

for some $\bar{x } \in (x-\frac{\epsilon}{2 }, x + \frac{\epsilon}{2 }]$

- Although $f_{X}( x )$is not a **probability measure**(i.e., the probability mass function for DRV),it is proportional to the probability that x takes values in a small interval centered at point $x$ .Thus,$f_{X}( x )$characterizes the **relative magnitude** of the probability that $X$ takes values in a small interval centered at $x$.

- The plot of $f_{X}( x )$describes the shape of the probability distribution of a CRV $X$.

⁉️️ Is $f_{X}( x )$ a unique function for a given $F_{X}( x )$

- Given a CDF $F_{X}( x )$, we can obtain the PDF function $f_{X}( x ) = F_{X}^{'}( x )$ at the points where $F_{X}( x )$ is differentiable. When $F_{X}( x )$ differentiable on the entire real line, the PDF $f_{X}( x )$ is unique.
- However, when $F_{X}( x )$ is not differentiable at some points, $f_{X}( X )$ is not defined at those points.

✅ So how to define the values of PDF $f_{X}( x )$ at the points where $F^{'}( x )$ does not exit 

- we can define $f_{X}( x )$ arbitrarily at those points, but smooth as possible for compute convenience.
- Example: consider two PDFs 

$$
\begin{aligned}
f_{X}( x ) = \begin{cases} e^{-x}, & for 0 <x < \infty \\0 , &  elsewhere\end{cases} \\
\text{and}\\
f_{X}( x ) = \begin{cases} e^{-x}, & for 0 \le x <\infty  \\ 0, & f \end{cases}
\end{aligned}
$$

**⚖️ Theorem 3.9 Properties of PDF** A function $f_{X}( x )$ is a PDF of a CRV $X$ **if and only if** it satisfies the following properties:

- $f_{X}( x ) \ge 0$ for all  $x \in \mathbb{R}$
- $\int_{-\infty}^{\infty}f_{X}( x )dx = 1$

**⚖️ Theorem 3.12 Support of a CRV** The support of a CRV $X$ is the set of all points $x$ in $\mathbb{R}$ such that $f_{X}( x ) > 0$. That is,
$$
support( X ) = \{ x \in \mathbb{R}:f_{X}( x ) > 0 \}
$$
where $f_{X}( x )$ is the PDF of $X$, but it is important that the $P(X = x) , x \in Support(x)$.

- The support of a CRV $X$ is the set of all possible points
on $\mathbb{R}$ with strictly positive PDF $f_{X}( X )$.
- The probability that a CRV $X$ takes values in a small neighborhood of any point in its support is always positive.
- In contrast,the probability that X takes values in some small neighborhood of any point outside the support will be zero.
- It suffices to focus on the support of $X$ when calculating the probabilities of a CRV.

🌰: Location_Scale Family 
Let $f( x )$ be a PDF, and let $\mu$ and $\sigma>0$ be any given constants.Then the funciton

$$
g( x ) = \frac{1}{\sigma}f( \frac{x-\mu}{\sigma} )
$$

is a PDF

> The family of f(x-u),indexed by parameter u,is called
the location family with standard PDF f(x),where pa-
rameter u is called the location parameter.
The family of if（）,indexed by parameter o,is called
the scale family with standard PDF f(x),where param-
eter o is called the scale parameter.
The family of If（）,indexed by parameters (u,o),
is called the location-scale family with standard PDF ,where u and o are called the location and scale parameters respectively.


## Functions of a Random Variable
## Mathematical Expectation
## Moments
## Quantiles
## Moment Generating Function (MGF)
## Characteristic Function
## Conclusion