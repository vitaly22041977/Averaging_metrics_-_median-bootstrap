# Averaging_metrics_-_median-bootstrap

Using the set date as an example
https://raw.githubusercontent.com/mwaskom/seaborn-data/master/tips.csv

1. Estimating Uncertainty (Spread)
The Mean and Median Problem:
The mean and median only provide point estimates (a single number), but do not indicate how reliable they are.
For example, the average tip may be $3, but without bootstrapping we do not know whether it ranges from [$2.8, $3.2] or [$1.5, $4.5].
Bootstrap Solution:
Generates multiple bootstrap samples and calculates a statistic (mean/median) for each.
Allows you to construct confidence intervals (e.g. 95% CI: [$2.7, $3.3]).
Shows how robust the estimate is to variations in the data.

2. Robustness to Distribution Assumptions
The Mean Problem:
The mean is sensitive to outliers and requires a normal distribution.
If the data is asymmetric (e.g. tips: most are small, but there are a few large ones), the mean can be misleading.
The median problem:
The median is robust to outliers, but does not provide information about the spread of the data.
Bootstrap solution:
Does not require distribution assumptions (nonparametric method).
Works with any data (normal, asymmetric, multimodal).
Allows you to compare the robustness of the mean and median (through the spread of their bootstrap distributions).

3. Applicability to any statistics
Limitation of the mean and median:
They only calculate the central tendency.
Not suitable for estimating other parameters (variance, correlation, quantiles, etc.).
Bootstrap advantage:
Can estimate any statistics:
Standard deviation.
Regression coefficients.

4. Comparison of the mean and median via bootstrap
Bootstrap allows you to clearly show:
How much the mean depends on outliers.
Why the median is often more reliable.

Conclusion:
Bootstrapping is a powerful tool for:
Assessing the uncertainty of statistics.
Comparing the stability of the mean and median.
Working with arbitrary distributions.
Calculating confidence intervals without complex formulas.
