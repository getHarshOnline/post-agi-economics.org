Title: The time between frontiers

[Read HTML](https://post-agi-economics.org/blog/one-clock-many-frontiers/)

Author: Harsh Joshi

<a id="the-time-between-frontiers"></a>

# The time between frontiers

Two frontiers each have a ten percent chance of being crossed in the next period. One keeps that chance in every later period; the other rises to fifty percent after the first. Their present probabilities agree. Their expected waiting times do not.

That small distinction carries a large question about AI's economic transition. A model of a task can improve, a firm can gain access, a deployment can become reliable and an institution can permit a new arrangement. Each movement can change the conditions for another. A clock needs to follow those processes closely enough to make the waiting meaningful. Its apparent precision is worth little if the rule governing tomorrow's transitions remains hidden.

**Note**

**Assumed transition laws.** The constructions below use stipulated transition laws, not fitted adoption data. They isolate what a waiting-time calculation depends on before asking which process observations would support.

<a id="the-future-transition-rule-matters"></a>

## The future transition rule matters

For a finite, fixed absorbing Markov chain, the transient matrix $Q$ describes movement among states before the terminal event. If its spectral radius is less than one, the fundamental matrix and expected steps to absorption are:

$$
N=(I-Q)^{-1},\qquad \boldsymbol{t}=N\boldsymbol{1}.
$$

Here $\boldsymbol{1}$ is a column of ones; the row sums of $N$ count expected periods before the crossing. [Grinstead and Snell's probability text](https://chance.dartmouth.edu/teaching_aids/books_articles/probability_book/Chapter11.pdf) develops the fixed-process result.

Consider a frontier with a 10 percent chance of being crossed in each period, independently while it remains uncrossed. Its expected waiting time is ten periods. Now let the probability be 10 percent in the first period and 50 percent in every later period. One period passes in all cases. With probability 0.9 the frontier remains uncrossed, and the remaining expectation is two periods:

$$
\mathbb{E}[T]=1+0.9\times2=2.8\text{ periods}.
$$

![Raising later crossing probabilities from 0.1 to 0.5 shortens the survival tail and expected wait from ten to 2.8 periods, despite the shared first-period probability of 0.1.](https://post-agi-economics.org/blog/one-clock-many-frontiers/survival-and-waiting.svg)

The top panel shows the probability of still waiting after each period; the lower panel shows the probability of the first crossing in that period. The curves continue beyond the displayed sixteen periods; each mean summarises the whole waiting-time distribution.

The two paths have the same current crossing probability and different waiting times. Today's probability becomes a countdown only after we specify how the rule behaves in the future.

With changing transient matrices and initial row distribution $\alpha$, survival after $k$ periods is:

$$
\Pr(T>k)=\alpha Q_0Q_1\cdots Q_{k-1}\boldsymbol{1}.
$$

At $k=0$ the product is the identity and survival is one. Summing these survival probabilities gives the expected waiting time when the sum is finite. Freezing the current matrix answers a different conditional question: how long would the transition take if today's rule persisted?

<a id="a-clock-with-two-transient-states"></a>

## A clock with two transient states

Take a process with states “awaiting setup”, “ready” and “crossed”. In each period, the awaiting state stays put with probability one half, reaches readiness with probability one quarter and crosses directly with probability one quarter. The ready state either stays or crosses, each with probability one half. Once crossed, the process stays crossed:

$$
P=
\begin{pmatrix}
0.5&0.25&0.25\\
0&0.5&0.5\\
0&0&1
\end{pmatrix},
\qquad
Q=
\begin{pmatrix}
0.5&0.25\\
0&0.5
\end{pmatrix}.
$$

Consequently:

$$
N=
\begin{pmatrix}
2&1\\
0&2
\end{pmatrix},
\qquad
\boldsymbol{t}=
\begin{pmatrix}
3\\
2
\end{pmatrix}.
$$

Starting before setup gives an expectation of three periods; starting ready gives two. The difference comes from the transition law, not from the names assigned to the states.

<a id="states-transitions-and-uncertainty"></a>

## States, transitions and uncertainty

Each row of a transition matrix is a probability distribution: its entries are non-negative and sum to one. Independently fitted logistic curves need not satisfy that joint condition. If their probabilities sum above one, assigning a remainder to the final state gives a negative probability. The transition construction has to preserve the row before its uncertainty is sampled.

The starting distribution also needs a meaning. A filtered distribution expresses what observations imply about the current state. A scenario distribution specifies an assumed starting point. A quasi-stationary distribution describes the state conditional on not yet being absorbed. The transient block loses probability through absorption; an ordinary stationary probability distribution is not interchangeable with these choices. Uncertainty bands inherit those choices. They can describe uncertainty in fitted parameters under a specified process without covering a different process, a changed observation rule or a new institutional arrangement.

<a id="elapsed-time-is-part-of-the-state"></a>

## Elapsed time is part of the state

In a fixed absorbing chain with initial row vector $\alpha$, the probability of remaining transient after $k$ steps is $\alpha Q^k\boldsymbol{1}$. The waiting time has a discrete phase-type distribution. A negative-binomial approximation would need its own conditions and an account of approximation error; adding more states does not supply either.

Some crossings depend on the time already spent waiting. A project awaiting permission for a day may face different prospects from one awaiting it for a year. For a Weibull survival function $S(u)=\exp(-\lambda u^\kappa)$, with $\lambda,\kappa>0$, the probability of surviving a further $t$ after already surviving $s$ is:

$$
\Pr(T>s+t\mid T>s)
=\frac{S(s+t)}{S(s)}
=\exp\left[-\lambda\big((s+t)^\kappa-s^\kappa\big)\right].
$$

Elapsed duration affects conditional survival; when $\kappa=1$, this expression reduces to the memoryless exponential case. A clock whose state omits relevant duration can confuse these different waiting situations.

<a id="what-crossing-the-frontier-means"></a>

## What crossing the frontier means

Absorption is a strong mathematical condition: the process cannot leave its terminal state. Economic persistence can be weaker. A technology may become entrenched through integration and switching costs while remaining vulnerable to restrictions, changed prices or a better alternative. One firm's lock-in need not be another firm's lack of choice.

The measured event also matters. A share of firms using assistants describes something different from a share of valuable work executed autonomously. A benchmark score describes capability under a test; deployed coverage includes operating conditions. A revised survey question can move the reported adoption series without changing any workflow on that date. These definitions determine the frontier the clock would time.

<a id="local-clocks-in-a-changing-economy"></a>

## Local clocks in a changing economy

The economy-wide clock in [One Yardstick](https://post-agi-economics.org/one-yardstick/) proposes following regimes towards agent-dominant execution, with different destinations according to whether households retain purchasing power. That ambition remains part of the inquiry. A local clock asks which task or sector frontier can be timed, through which transition process, and with which observations locating the system within it. The relationship between these scales has to be established rather than assumed.

Such a model could compare conditional signal paths, describe heterogeneous diffusion or estimate a waiting time under a stated process. Its forecast would then have to [meet observed outcomes](https://post-agi-economics.org/collections/thinking-gets-cheap/models-and-measures/a-forecast-meets-its-outcome/) under a fixed event definition and information cutoff. Crossing one frontier can change another frontier's conditions. The useful question is which crossing we can describe, what moves it, and what work remains on the other side. The economy does not need to keep one appointment for those local questions to matter.
