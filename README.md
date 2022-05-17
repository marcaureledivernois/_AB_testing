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

# Credits

[Towards Data Science](https://towardsdatascience.com/ab-testing-with-python-e5964dd66143)