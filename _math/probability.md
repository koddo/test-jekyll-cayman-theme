---
title:  "Probability"
layout: default

---

# probability density function

Pdf of sum of two random variables:
<https://en.wikipedia.org/wiki/Probability_density_function#Sums_of_independent_random_variables>
<https://www.statlect.com/fundamentals-of-probability/sums-of-independent-random-variables>
$$f_{U+V}(x)=\int _{-\infty }^{\infty }f_{U}(y)f_{V}(x-y)\,dy=\left(f_{U}*f_{V}\right)(x)$$

# Distributions

## Binomial

<https://en.wikipedia.org/wiki/Binomial_distribution>

Distribution of sum of two independent binomial variables: $X \sim \def\Bin{\mathord{\rm Bin}}\Bin(n,p)$, $Y \sim \def\Bin{\mathord{\rm Bin}}\Bin(m,p)$, $X+Y \sim \Bin(n+m,p)$
<https://math.stackexchange.com/questions/1176385/sum-of-two-independent-binomial-variables>

# Random walk

There are $2^n$ paths of length $n$.
A path from the origin to an arbitrary point $(n, x)$ exists $\iff \ n = p+q, \quad x = p - q$.
There are $N_{n,x} = \binom{p+q}{p} = \binom{p+q}{q}$ valid paths.

Lemma. (Reflection principle) The number of paths from A to B which touch or cross the x-axis equals the number of all paths from A' to B.

Ballot theorem. In an election where candidate A receives p votes and candidate B receives q votes with p > q, what is the probability that A will be strictly ahead of B throughout the count?

$$P(A) = {\frac {p-q}{p+q}}$$

$p_{n,r}$ — visit to r at epoch n

$$p_{n,r} = P(\{ S_n = r \}) = \binom{n}{\frac{n+r}{2}} 2^{-n}$$

$u_{2v}$ — zero at 2v, $f_{2v}$ — first zero at 2v:

$$u_{2v} = \binom{2v}{v} 2^{-2v}$$

Using Stirlings's forluma, we get:

$$u_{2v} \sim \frac{1}{\sqrt{\pi v}}$$

And relation between the two:

$$u_{2n} = f_2 u_{2n-2} + f_4 u_{2n-4} + \ldots + f_{2n} u_0$$

The main lemma. The probability that no return to 0 occurs at up to and including 2n is the same sa the probability that a return occurs at 2n:

$$P(\{ S_1 \neq 0, \ldots, S_{2n} \neq 0\}) = P(\{ S_{2n} = 0\}) = u_{2n}$$

Or, using the symmetry (these are equivalent):

$$P(\{ S_1 > 0, \ldots, S_{2n} > 0\}) = \frac{1}{2} u_{2n}$$

$$P(\{ S_1 \geq 0, \ldots, S_{2n} \geq 0\}) = u_{2n}$$

Lemma. $$f_{2n} =  u_{2n - 2} - u_{2n} = \frac{1}{2n-1} u_{2n}$$

It follows that $f_2 + f_4 + \ldots = 1$, i.e, returning to 0 is practically certain in a long game.

Probability of no return to 0 after 100 tosses is 0.08. 

$\alpha_{2k,2n} = u_{2k} u_{2n-2k}$ — last zero at 2k, up to and including 2n.

Approximation: $$\alpha_{2k,2n} = \frac{1}{n} f(x_k)$$, where $x_k = \frac{k}{n}$ and $$f(x) = \frac{1}{\pi \sqrt{x(1-x)}}$$.


Theorem. Probability that up to epoch $2n+1$ there occur exactly $r$ changes of sign is $\xi_{r, 2n+1} = 2 p_{2n+1, 2r+1} = 2 P(\{ S_{2n+1} = 2r+1 \})$.

The consequence of this is the lead never changes is more probable than any number of changes of sign: $\xi_{0,n} \ge \xi_{1,n} > \xi_{2,n} > \ldots$

# superlearn

<iframe class="autoresize nodisplay superlearn-iframe" src="{{ site.superlearn_url }}/ht/asdf2?deckname=math -- probability -- pdf and cdf">
    <p>Your browser does not support iframes.</p>
</iframe>

<iframe class="autoresize nodisplay superlearn-iframe" src="{{ site.superlearn_url }}/ht/asdf2?deckname=math -- probability -- random walk">
    <p>Your browser does not support iframes.</p>
</iframe>

