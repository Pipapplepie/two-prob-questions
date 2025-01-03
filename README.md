# two-prob-questions

## Q1:
There is a Ben and Jerry's ice cream machine at UTown that charges $1 to play. Given that the price of a small tub is around $6, what is the distribution that best models the expected number of tries before successfully grabbing one of the tubs and how would you derive and compute the parameter(s) for this distribution from actual data? Bonus points for you if you try this in person and provide a GitHub repository to show case your work. *

## Ans:
Consider geometric distribution X; a distribution often used to model the the number of trials until the occurrence of a discrete event (here, getting the ice-cream tub). 

The distribution X has only 1 parameter; p. (here the probability of getting the tub)

$$Pr(X = n) = (1-p)^{n-1}p$$

To derive $p$ from actual data, consider Law of Large Numbers;

It says if we perform an enough large amount of experiments, the number of tubs got will be close to the actual mean $\mu = np$.

Here, play the machine for n times, (spending $n) then count the number of tubs got, $M_n$.

We can approximate parameter p as $M_n/n$.

## Q2:
m&m candies are manufactured at two different plants in the US with the following color distribution

Cleveland : Red=0.131, Orange=0.205, Yellow=0.135, Green=0.198, Blue=0.207, and Brown=0.124.

Hackettstown : Red=0.125, Orange=0.25, Yellow=0.125, Green=0.125, Blue=0.25, and Brown=0.125.

Suppose you bought many packets of m&m, how can you determine which plant these packets came with statistical testing?

Bonus: The methodology in this article is flawed. Can you explain why?

## Ans: 

By hypothesis testing, 

our Hypothesis 0 $H_0$: the packets came from Cleveland; Hypothesis 1 $H_1$: they are from Hackettstown.

$$ Pr(data | H_0) =  [C_n^r (0.131)^r] [C_{n-r}^o (0.205)^o] [C_{n-r-o}^y(0.135)^y] [C_{n-r-o-y}^g (0.198)^g] [C_{n-r-o-y-g}^b (0.207)^b] [C_{n-r-o-y-g-b}^br (0.124)^{br}]$$

where n denotes the number of m&m candies in all packets, and $r$ denotes the number of red candies in them, same for $o,y,g,b,br$. $Pr(data | H_0)$ is the probability of the situation under Hypothesis 0.

Set significance level $\alpha$ as 0.05. Reject $H_0$ if; $$Pr(data | H_0) < 0.05$$, i.e., Not enough evidence for "the packets are from Cleveland".

Otherwise, accept Hypothesis 0.
