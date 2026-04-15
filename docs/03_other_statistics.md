## Pearson & Spearman correlation coefficients

* Both: scaled from [-1, 1]. -1 is an inverse relationship, 1 is a positive relationship, 0 is no correlation.

### Pearson $r$:

* Calulated as $$ r = \frac{cov(X, Y)}{\sigma_X \sigma_Y} $$ where $cov(X, Y)$ is the covariance between variables $X$ and $Y$, and $\sigma_X$ and $\sigma_Y$ are the standard deviations of $X$ and $Y$, respectively.

* Pearson is to model **linear relationships** used for **continuous variables**
* For normally distributed data.
* Requires homoscedasticity, which means the variability of the residuals is the same across all levels of the independent variable. 
    * If this assumption is violated, the results may be unreliable.


### Spearman $\rho$:

* Models a **monotonic relationship**, for continuous or discrete variables. What is a monotonic relationship? 
    * M(1) as one increases, the other does not decrease.
    * M(-1) as one decreases, the other does not increase.
* Non parametric - does not assume a distribution of data. Can be useful if there is a small sample size, non normal distribution, outliers, high variance..
* Variables are ranked. This means that the actual values of the data are not used, but rather their ranks (e.g., 1st, 2nd, 3rd, etc.). 
    * Makes it less sensitive to outliers because the ranks are less affected by extreme values than the actual data points.
* Calculated as $$ \rho = 1 - \frac{6 \sum d_i^2}{n(n^2 - 1)} $$ where $d_i$ is the difference between the ranks of corresponding values of $X$ and $Y$, and $n$ is the number of observations.
* Ranks are literally the order of values, rank 1 = smallest.


Summary: 
* For normally distributed data with a linear relationship, use $r$.
* For non-normal distributed data, or when the relationship is monotonic but not linear, use $\rho$.
* Given an exponential relationship, we would get a spearman of 1. But pearson would be less, because it's not linear.