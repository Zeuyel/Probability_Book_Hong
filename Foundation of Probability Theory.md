# Foundation of Probability Theory

## Random Experiments

**\[💬 Definition 1. Random Experiment\]** A random experiment is an experiment whose outcome is not known in advance.

there are two essential elements of a random experiment:

::: callout-important
the set of all possible outcomes

the likelihood of each outcome
:::

we need to know the sample space and the probability of each outcome in the sample space.

● The purpose of mathematical statistics is to provide mathematical models for random experiments ofinterest.\
● Once a model for such an experiment is provided and the theory worked out in detail, the statistician may,within this framework, make inference about the probability law of the random experiment.

## Basic Concepts of Probability

**\[💬 Definition 2. Sample Space\]** The possible outconmes of a random experiment are called the sample space and is denoted by $S$.

When an experiment is performed, the realization of the experiment will be one **(and only one)** outcome in thesample space.(Mutually exclusive)

If the experiment is performed a number of times, a different outcome may occur each time or some outcomes may repeat.

a sample space $S$ can be countable or uncountable.

**\[💬 Definition 3. Event\]** An event $A$ is a collection of basic outcomes from the sample space S that share certain common features or equivalently obey certain restrictions.

The event is the **subset** of the sample space.

::: callout-important
-   $Basic outconme \subseteq Event \subseteq Sample\ space$
:::

## Review of Set Theory

✅Use Venn Diagram to represent the relationship between sets(or sample point,event, all the related concepts).

**\[💬 Definition 4. Intersection\]** Intersection of $A$ and B, denoted $A \cap B$， is the set of basic outcomes in S that belong to both $A$ and B.The intersection of $A$ and B is the event that both $A$ and B occur. is also called the **logicall product** of $A$ and B.

**\[💬 Definition 5. Exclusiveness\]** If $A$ and B have no common basic outcomes, they are called mutually exclusive and their intersection is empty set $\emptyset$, i.e., $A \cap B = \emptyset$ where $\emptyset$ denotes an empty set that contains nothing.

-   mutually exclusive events are also called disjoint events.

**\[💬 Definition 6. Union\]** The union of $A$ and B, denoted $A \cup B$, is the set of basic outcomes in S that belong to either A or B or both. The union of A and B is the event that either A or B or both occur. is also called the **logical sum** of $A$ and $B$.

**\[💬 Definition 7. Collective Exhaustiveness\]** Suppose that $A_1, A_2, A_3, \cdots$ are events in S. If $A_1 \cup A_2 \cup A_3 \cup \cdots = S$, then the events $A_1, A_2, A_3, \cdots$ are collectively exhaustive.

**\[💬 Definition 8. Complement\]** The complement of A, denoted $A^c$, is the set of basic outcomes in S that do not belong to A. The complement of A is the event that A does not occur.

-   $A \cap A^{c} = \emptyset \ and \ A \cup A^{c} = S$

**\[💬 Definition 9. Difference\]** The difference of A and B, denoted $A - B = A \cap B^{c}$, is the set of basic outcomes in S that belong to A but not to B. The difference of A and B is the event that A occurs but B does not occur.

🧮Distributivity Laws :

$$
A \cap (B \cup C) = (A \cap B) \cup (A \cap C)\\
A \cup (B \cap C) = (A \cup B) \cap (A \cup C)
$$

In more general, we have $$
B \cap \left( \bigcup_{i=1}^{n} A_i \right)= \bigcup_{i=1}^{n} (B \cap A_i) \\
B \cup \left( \bigcap_{i=1}^{n} A_i \right)= \bigcap_{i=1}^{n} (B \cup A_i)
$$

🧮 De Morgan's Laws

$$
\left( A \cup  B \right)^{c} =A^{c} \cap B^{c}
\left( A \cap  B  \right)^{c} = A^{c} \cup B^{c}
$$

In more general, we have $$
\left( \bigcup_{i=1}^{n} A_i \right)^{c} = \bigcap_{i=1}^{n} A_i^{c} \\
\left( \bigcap_{i=1}^{n} A_i \right)^{c} = \bigcup_{i=1}^{n} A_i^{c}
$$

------------------------------------------------------------------------

🌰: Suppose the events A and B are disjoint.Under what condition are $A^{c}$ and $B^{c}$ also disjoint?

👉: $A^{c}$ and $B^{c}$ are disjoint if and only if $A \cup B = S$.That is say $A$ and $B$ is exhaustive.

🌰: • Are $A \cap B$ and $A^{c} \cap B$ mutually exclusive?

• Is $\left( A \cap B \right) \cup \left( A^{c} \cap B \right) = B$?

• Are $A$ and $A^{c} \cap B$ mutually exclusive?

• Is $A \cup \left( A^{c} \cap B \right) = A \cap B$?

👉：Yes, Yes, Yes, No

🌰: Let the set of events $\{ A_i = 1 , \ldots ,n \}$ be mutually exclusive and collectively exhaustive, and let A be an event in S - Are $A_1 \cap A, \ldots ,A_n \cap A$ mutually exclusive? - Is the union of $A_i \cap A, i = 1, \ldots ,n$, equal to A? That is, do we have: $$
\bigcup_{i=1}^{n} \left( A_i \cap A \right) = A
$$

👉: Yes, Yes

> In the linear algebra, we can use the projection matrix to understand this.The $\{ A_1,A_2, \ldots ,A_n \}$ is the orthogonal bases of the specific space, and the $A$ is the vector in this space. The $A_i \cap A$ is the projection of $A$ on the $A_i$ direction.
>
> -   A sequence of collective and mutually exclusive events forms a partition of sample space S.
>
> -   A set of collectively exhaustive and mutually exclusive events can be viewed as a complete set of orthogonal bases.
>
> -   The projection of a vector on a subspace is the sum of the projections of the vector on the orthogonal bases of the subspace.
>
> -   A complete set of orthogonal bases can represent any event A in the sample space S, and 𝐴𝑖 ∩ 𝐴 could be viewed as the projection of event A on the base $A_i$.

------------------------------------------------------------------------

## Fundamental Probability Laws

✅ To assign a probability to an event $A \in S$, we shall introduce a **probability function**, which is a function or a mapping from an event to a real number (0,1).

✅ To assign probabilities to events, complements of events,unions and intersections of events, we want our collection of events to include all these combinations of events.

✅Such a collection of events is called an $\sigma$-field($\sigma$ algaebra) of subsets of the sample space S,which constitude the domain of the probability function.

![image.png](https://img10.360buyimg.com/ddimg/jfs/t1/209581/28/38739/6451/656b139eF3f92090d/e8ba1188e7d747ec.jpg)

**\[💬 Definition 10. Sigma Algebra\]** A $sigma(\sigma) algebra$,denoted by $\mathbb{B}$ , is a collection of subsets(events) of S that satisfies the following three conditions:

1.  $\emptyset \in \mathbb{B}$i.e., the empty set is in $\mathbb{B}$.
2.  If $A \in \mathbb{B}$, then $A^{c} \in \mathbb{B}$.(i.e., $\mathbb{B}$ is closed under complements)
3.  If $A_1,A_2, \ldots \in \mathbb{B}$, then $\bigcup_{i=1}^{\infty} A_i \in \mathbb{B}$.(i.e., $\mathbb{B}$ is closed under countable unions)

::: callout-important
-   $\sigma$-algebra is a collection of events in $S$(subset) that satisfies certain properties and constitutes the domain of a probability function.
-   A $\sigma$ -field is a collection of subsets in $S$ , but itself is not a subset of $S$ . In contrast, the sample space $S$ is **only an element of a** $\sigma$ -field.
-   The pair $(S,\mathbb{B})$ is called a measurable space.So for a specific sample space $S$, we can have different $\sigma$-algebra $\mathbb{B}$.
:::

**\[💬 Definition 11. Probability Function\]** Suppose a random experiment has a sample space $S$ and an associated $\sigma$ -field $\mathbb{B}$ . A probability function $$
P:\mathbb{B} \to [0,1]
$$

is defined as a mapping that satisfies the following three conditions:

(1) $0 \le P(A) \le 1 for all A \in \mathbb{B}$ .

(2) $P(S) = 1$.

(3) If $A_1,A_2, \ldots \in \mathbb{B}$ are mutually exclusive, then $P\left( \bigcup_{i=1}^{\infty} A_i \right) = \sum_{i=1}^{\infty} P(A_i)$.🚩The probability of the union of mutually exclusive events is the sum of the probabilities of the individual events.

::: callout-important
-   A probability function tell how the probability of occurrence is distributed over the set of events $\mathbb{B}$.In this sense we speak of a distribution of probability.

![](https://img12.360buyimg.com/ddimg/jfs/t1/232346/23/5558/25512/656c2680F5d41484e/4bbc3248c4c4ad99.jpg){width="50%" fig-align="center"}

-   For a given measurable space $(S,\mathbb{B})$, many different probability functions can be defined. The goal of econometrics and statistics is to find a probability function that **most accurately describes the underlying DGP**. This probability function is usually called the **true probability function** or true probability distribution model.
:::

✅So how to interpret the probability target to an event?

### Approach 1:Relative frequency interpretation

The probability of an event can be viewed as the limit of the " relative frequency" of occurrence of the event in a large number of repeated independent experiments under essentially the same conditions.

The relative frequency interpretation is valid under the assumption of a large number of repeated experiments under the same condition. In statistics, such an assumption is formally termed as **"independence and identical distribution (IID)"**.

> ⁉️ When the weather forecast bureau predicts that there is a 30% chance for raining, it means that under the same weather conditions it will rain 30% of the times. We cannot guarantee what will happen on any particular occasion, but if we keep records over a long period of time, we should find that the proportion of "raining" is very close to 0.30 for the days with the same weather condition.
>
> But in practical applications, we cannot repeat the same experiment a large number of times under the same conditions. Therefore, the relative frequency interpretation is not very useful in practice. We introduce the **subjective interpretation** of probability.

### Approach 2:Subjective Probability interpretation

The subjective method views probability as a **belief** in the chance of an event occurring.But a personal or subjective assessment is made of theprobability of an event which is difficult or impossible to estimate in any way.So is that means the subjective probability is not useful?

🌰: Subjective probability is the foundation of Bayesian statistics, which is a rival to classical statistics.

🌰: Rational Expectations

Rational expectations (Muth 1961) hypothesizes that the **subjective expectation** of an economic agent (i.e., the expectation under the subjective probability belief of the economic agent) **coincides with the mathematical expectation** (i.e., the expectation under the objective probability distribution).

For example, we eager to have a wage $S$, but we don't know the exact value of $S$. We can only estimate the probability distribution of $S$ based on our subjective probability belief. The rational expectation hypothesis states that the subjective expectation of $S$ is equal to the mathematical expectation of wage :the $E(S)$.

🌰: Professional Forecast

The U.S. central bank—Fed issues professional forecasts for important macroeconomic indicators such as GDP growth rate, inflation rate and unemployment rate.

In each quarter, they send surveys to professional forecasters, asking their views on probability distributions of these important macroeconomic indicators.

Specifically, each forecaster will be asked what is his/her forecast of the probability that the inflation rate lies in various intervals.

🌰: Risk Neutral Probability

During the 1997-1998 Asian financial crisis, many investors were very concerned with the collapse of the Hong Kong peg exchange rate system with U.S. dollars and devaluations of Hong Kong dollars.

![](https://img11.360buyimg.com/ddimg/jfs/t1/228856/24/5468/42874/656c39c7Fd1972412/7bdaf3e6562136fd.jpg){width="50%" fig-align="center"}

In other words, their subjective probabilities of Hong Kong dollar devaluation were higher than the objective probabilities of the Hong Kong dollar movements. The former are called risk-neutral probability distributions and the latter are called objective or physical probability distributions in finance.

![](https://img14.360buyimg.com/ddimg/jfs/t1/236374/40/5377/11113/656c3a44Fd120b79c/6d287fddf41db3f9.jpg){width="50%" fig-align="center"}

The gap between these two distributions reflects the risk attitude of market investors. The risk-neutral probability distribution is a financial instrument in derivative pricing.

![](https://img10.360buyimg.com/ddimg/jfs/t1/236100/21/5419/27681/656c3ef3Fced1a70c/8ec3cf9e73ffb875.jpg){width="50%" fig-align="center"}

**\[💬 Definition 12. Probability Space\]** A probability space is a triple $(S,\mathbb{B},P)$, where $S$ is a sample space, $\mathbb{B}$ is a $\sigma$-field of subsets of $S$, and $P:\mathbb{b} \to [0,1]$ is a probability function defined on $\mathbb{B}$.

> Because the probability function $P(\cdot )$ is defined on $\mathbb{B}$, the collection of sets (i.e., events), it is also called a set function.

**⚖️ Theorem 1** If $\emptyset$ denotes the empty set, then $P(\emptyset) = 0$.

📑 Proof: Given that 𝑆 = 𝑆 ∪ ∅, and 𝑆 and ∅ are
mutually exclusive, we have $P(S) = P(S \cup \emptyset) = P(S) + P(\emptyset)$.It follows that $P(\emptyset) = 0$.

::: {.callout-warning}

$$
P(A) = 0 \text{**does not**} \Rightarrow A = \emptyset
$$

:::

**⚖️ Theorem 3** $P(A) = 1 - P(A)^{c}$

📑 Proof: Oberve $A \cup A^{c} = S$. Then 
$$
P(S) = P(A \cup A^{c}) = P(A) + P(A^{c})
$$
Because $P(S)=1$,$A \text{and} A^{c}$ are mutually exclusive, we have $P(A) = 1 - P(A^{c})$.

::: {.callout-important}

The ratio of the probability of an event $A$ to the probability of its complement,
$$
\frac{P(S)}{P(A^{c}) }  =\frac{P(A)}{1- P(A)}
$$
is called the **ratio odds** of $A$.

:::

**⚖️ Theorem 4** If $A$ and $B$ are two events in $\mathbb{B}$, and $A \subseteq B$, then 
$$
P(A) \le P(B)
$$

**⚖️ Theorem 5** For any two events $A$ and $B$ in $\mathbb{B}$,
$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$
Keep in mind that the probability of an event is equal to the area it occupies in the sample space.

Since $A \cap B \subseteq S$, we have $P(A \cap B) \le P(S) = 1$ by Theorem 4. It follows from the theorem 5 that

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B) \ge P(A) + P(B) - 1
$$

It also called the **Bonferroni's inequality**.

**⚖️️ Theorem 6 [Rule of total probability]** If $A_1,A_2, \ldots \in \mathbb{B}$ are mutually exclusive and collectively exhaustive, and A is an event in $S$, then
$$
P(A) = \sum_{i=1}^{\infty} P(A \cup A_i)
$$

![](https://img13.360buyimg.com/ddimg/jfs/t1/232051/6/5770/25277/656c6018F97a717a5/e76558484123985a.jpg){width="50%" fig-align="center"}

So if 
$$
A = \{ \text{students whose scores > 90 points} \},\\
A_i = \{ \text{students from country i} \} 
$$

then $A \cap A_i = \{ \text{students from country i whose scores are > 90 points} \}$

**⚖️ Theorem 7 [Subadditivity:Boole'inequality]** For any sequence of events $\{ A_i \in \mathbb{B}, i =1,2, \ldots  \}$,
$$
P \left(  \bigcup_{i=1}^{\infty}A_i  \right)  \le \sum_{i=1}^{\infty} P(A_i)
$$

## Methods of Counting
✅How to calculate the probability of event A?

Suppose event $A$ includes $k$ basic outcomes in the sample space $S$. Then the probability of $A$ is given by
$$
P(A) = \sum_{i=1}^{k}P(A_i)
$$

If in addition $S$ consists of $n$ equally likely basic outcomes $\{ A_1, \ldots ,A_n\}$, and event $A$ consists of $k$ basic outcomes, then 


## Conditional Probability

## Bayes' Theorem

## Independence

## Conclusion