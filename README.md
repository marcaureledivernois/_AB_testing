## A/B Testing

# Overview

We want to test whether a change in the product statistically changes its end results. To do so, 
we design an experiment and need two groups of people : a control group and a treatment group. The 
control group receives the "old product" and the treatment group receives the "new product". It is important
to do it simultaneously to remove any seasonality bias.

# Example

Let’s imagine you work on the product team at a medium-sized online e-commerce business. 
The UX designer worked really hard on a new version of the product page, 
with the hope that it will lead to a higher conversion rate. The product manager 
(PM) told you that the current conversion rate is about 13% on average throughout the 
year, and that the team would be happy with an increase of 2%, meaning that the new 
design will be considered a success if it raises the conversion rate to 15%.

# Steps

1. Compute the minimum sample size
2. Run the experiment
3. Test hypothesis
4. Draw conclusions

# Minimum sample size

Since we test on a sample population and not on the whole user base (our population), 
the conversion rates that we’ll get will inevitably be only estimates of the true rates.

The number of people (or user sessions) we decide to capture in each group will have an 
effect on the precision of our estimated conversion rates: the larger the sample size, 
the more precise our estimates (i.e. the smaller our confidence intervals), 
the higher the chance to detect a difference in the two groups, if present.

On the other hand, the larger our sample gets, the more expensive (and impractical) our study becomes.

We use **Power Analysis** to compute the sample size that we need in each group and it depends on three factors :

1. Power of the test (1 — β) — This represents the probability of finding a statistical difference between the groups in our test when a difference is actually present. This is usually set at 0.8 by convention.
2. Alpha value (α) — The critical value (usually set at 0.05). We want to be 1-α% confident it is statistically different.
3. Effect size — How big of a difference we expect there to be between the conversion rates

# Rule of thumb

Lehr's (rough) rule of thumb says that the sample size n for a two-sided Two-sample t-test with power 80% (β = 0.2) and significance level α = 0.05 should be:

n = 16 s<sup>2</sup> / d<sup>2</sup>

# Compute test statistics

If we have a very large sample, we can use the normal approximation for calculating our p-value.
If p<0.05, we can reject H0: old=new. Hence, if p<0.05, we can conclude that the new product is significantly different.

# Credits

[Towards Data Science](https://towardsdatascience.com/ab-testing-with-python-e5964dd66143)
