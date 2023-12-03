---
title: Introduce
---

# General methodology of modern ecnomic research
## Data collection
- survey
- field studies
- experimental economics
- **Big data**

In most time,we get so-called stylized facts by summarizing from observed economic data.

🌰：Engel Curve,Phillips Curve,Okun's Law,volatility clustering in finance,etc.

So the empirical research is the first step of economic research which is so-called **economical intuition**.But for more further understanding,we need to build a model to explain the stylized facts by using the statistic tools.

## Development of economic theories and models
With the emprical stylized facts,we can build a model to explain the facts and make predictions.This process is called **mathematical modeling of economic theroy**.

🌰: An example is the Euler equation for rational expectations in macroeconomics.

Moreover, the objective of economic modeling is not merely to explain the stylized facts but also to understand the economic mechanism behind the facts.

## Empriical validation/inference of economic theories and models

The last step is to test the model by using the observed data and make inference about the model.The key is to transform the model into a **textable empirical econometric model**.

## Applications

After an econometric model passes the empirical
evaluation, it can then be used to:
- Explain important empirical stylized facts
- Test economic theory and/or hypotheses
- Forecast future evolution of the economy
- Policy evaluation and other application

# Roles of Econometrics

Modern economy is essentially built by upon the following three fundamental axioms:

- Any economy can be viewed as a stochastic process governed by some probability laws.
- Economic phenomenon, often summarized in form of data, can be reviewed as a realization of this stochastic data generating process.

So we establish the econometrics to infer the probability laws from the observed data that reflect the stochastic economic system, and then use the inferred probability laws for economic application e.g. to make predictions and conduct policy analysis.


# Illustrative Examples

## The simple keynesian consumption function Modle

For keynesian consumption function, we have the following model:

$$
Y_t = C_t + I_t + G_t\\
C_t = \alpha + \beta Y_t + \epsilon_t
$$

Where $Y_t$ is the aggregate income,$C_t$ is the private consumption,$I_t$ is the private investment,$G_t$ is the government expenditure,$\epsilon_t$ is the random error term.

**The parameters $\alpha$ and $\beta$ can have appealing economic interpretations:**

- $\alpha$ is the survival level consumption even if income is zero.
- $\beta$ is the marginal propensity to consume (MPC), i.e. the amount of additional consumption for each additional unit of income.

**Multiplier of income with respect to govenrnment spending**

$$
\frac{\partial Y_t}{\partial G_t} = \frac{1}{1-\beta}
$$

which depends on the maginal propensity to consume $\beta$.So when assess the effect of fiscal policy, it is important to know the magnitude of $\beta$.
## Rational Expectations and Dynamic Asset Pricing Models

The rational expectations hypothesis (REH) is a key assumption in modern macroeconomics and finance. It states that agents’ expectations about the future value of an economic variable are not systematically wrong. In other words, agents’ expectations are not biased.

Suppose a representative agent has a constant relative risk aversion utility function:

$$
U =\sum_{t=0}^{n} \beta^{t} 
\\ u(C_t) =\sum_{t=0}^{n} \beta^t \frac{C_t^{\gamma} - 1}{\gamma}
$$

where $\beta \ge 0$ is the discount factor and $\gamma \ge 0$ is the coefficient of relative risk aversion.$\mu(\cdot )$ is the agent’s utility function in each time period.$C_t$ is consumption in period $t$.

So, obviously the agent's optimization problem is: choosing a sequence of consumption $\{C_t\}_{t=0}^{\infty}$ to maximize the expected utility 
$$
\max_{\{ C_t \}} E(u)
$$
subject to the budget constraint:

$$
C_t + P_t q_t \le W_t + P_t q_{t-1}
$$

where $P_t$ is the price of the consumption good in period $t$, $q_t$ is the quantity of the asset held at the end of period $t$, and $W_t$ is the wage income in period $t$.

So we can define this marginal rate of intertemporal substitution (MRIS) as:
$$
MRS_{t+1}(\theta) = \frac { \frac { \partial u ( C _ { t + 1 } ) } { \partial C _ { t + 1 } } } {\frac { \partial u ( C _ { t } ) } { \partial C _ { t } } } = (\frac{C_{t+1}}{C_t})^{\gamma-1}
$$

where model parameter vector $\theta = (\beta,\gamma)^{'}$.

So the First order condition is:
$$
E[\beta MRS_{t+1}(\theta)R_{t+1}|I_t] = 1
$$

where $R_{t+1}$ is the gross return on the asset in period $t+1$ and $I_t$ is the information set available at the beginning of period $t$.And the FOC is usually called the Euler equation.And we can estimate this model by using the generalized method of moments (GMM) method.

### Production Function and Hypothsis on constant returns to scale
Production function：
$$
Y_t = \exp(\epsilon_t)F(L_t,K_t)
$$

where $Y_t$ is the output,$L_t$ is the labor input,$K_t$ is the capital input,$\epsilon_t$ is the random error term.

So we can get the constant return to scale hypothesis:

$$
\lambda F(L_i,K_i) = F(\lambda L_i,\lambda K_i)\ for\ all \lambda > 0
$$

**CRS** is a necessary condition for the existence of a long-run equilibrium in a competitive market.If CRS does not hold, and the technology displays the increasing returns to scale, then the market will lead to natural monopoly.

In practical, a conventional approach to estimate the production function is to use the Cobb-Douglas production function:
$$
Y_i = F(L_i,k_i) = A \exp(\epsilon_i) L_i^{\alpha}K_i^{\beta} = 
$$

Then CRS becomes a mathematical restriction on the parameters $\alpha$ and $\beta$:
$$\mathbb{H}_0 : \alpha + \beta  = 1$$

So if $\alpha + \beta > 1$, the production function displays increasing returns to scale; if $\alpha + \beta < 1$, the production function displays decreasing returns to scale.

In statistics, we can use the **F-test** to test the null hypothesis $\mathbb{H}_0$ (one dimensional restriction).

unfortunately, this test is not suitable for many cross-sectional economic data, which usually display conditional heteroskedasticity.One needs to use a robust, heteroskedasticity-consistent test procedure, such as the **White test**. 



# Roles of Probability and Statistics
