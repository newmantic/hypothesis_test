# hypothesis_test

Hypothesis testing is a statistical method used to make inferences or decisions about a population parameter based on sample data. It involves the following steps:

Null Hypothesis (H0): The hypothesis that there is no effect or no difference. It represents the status quo.
Alternative Hypothesis (H1 or Ha): The hypothesis that suggests there is an effect or a difference.
Choose a Significance Level (alpha):

Common choices for alpha are 0.05 or 0.01, representing the probability of rejecting the null hypothesis when it is actually true (Type I error).

Calculate the Test Statistic:
The test statistic is a value calculated from the sample data used to compare against a critical value or to compute a p-value.

Determine the p-value:
The p-value is the probability of observing a test statistic as extreme as, or more extreme than, the value observed under the null hypothesis.

Make a Decision:
If the p-value <= alpha, reject the null hypothesis (H0).
If the p-value > alpha, fail to reject the null hypothesis.



Z-Test
Z-Test is used to determine if there is a significant difference between the means of two groups when the population standard deviations are known.

Test Statistic (Z):
Z = (X_bar - mu) / (sigma / sqrt(n))
Where:
X_bar = Sample mean
mu = Population mean under H0
sigma = Population standard deviation
n = Sample size

Decision Rule:
Calculate the p-value using the standard normal distribution.
Compare the p-value with the significance level (alpha).


T-Test
T-Test is used to compare the means of two groups, especially when the population standard deviations are unknown.

Test Statistic (T):
For a one-sample T-test:
T = (X_bar - mu) / (s / sqrt(n))

For an independent two-sample T-test:
T = (X1_bar - X2_bar) / sqrt( (s1^2 / n1) + (s2^2 / n2) )
Where:
X_bar = Sample mean
mu = Population mean under H0
s = Sample standard deviation
n = Sample size
X1_bar and X2_bar = Means of the two samples
s1 and s2 = Standard deviations of the two samples
n1 and n2 = Sizes of the two samples

Degrees of Freedom (df):
For a one-sample T-test:
df = n - 1
For an independent two-sample T-test:
df = n1 + n2 - 2

Decision Rule:
Calculate the p-value using the t-distribution.
Compare the p-value with the significance level (alpha).

Chi-Squared Test
Chi-Squared Test is used to test the independence of two categorical variables or to test the goodness of fit.

Test Statistic (Chi^2):
Chi^2 = sum( (O_i - E_i)^2 / E_i )
Where:
O_i = Observed frequency
E_i = Expected frequency

Degrees of Freedom (df):
For a Chi-squared test of independence:
df = (r - 1) * (c - 1)
Where:
r = Number of rows in the contingency table
c = Number of columns in the contingency table

Decision Rule:
Calculate the p-value using the chi-squared distribution.
Compare the p-value with the significance level (alpha).


Choosing among the Z-test, T-test, and Chi-squared test depends on the nature of your data and the specific hypothesis you are testing. 

Use the Z-test when:
Sample Size: The sample size is large (typically n > 30).
Population Standard Deviation Known: The population standard deviation (sigma) is known.
Data Type: You're comparing the means of one or two groups (e.g., comparing the sample mean to a known population mean).
Distribution: The data is approximately normally distributed.

Use the T-test when:
Sample Size: The sample size is small (typically n ≤ 30), but it can also be used for larger samples.
Population Standard Deviation Unknown: The population standard deviation is unknown, and you estimate it using the sample standard deviation.
Data Type: You're comparing the means of one or two groups (e.g., one-sample t-test, two-sample t-test, paired t-test).
Distribution: The data should be approximately normally distributed or the sample size should be large enough for the Central Limit Theorem to apply.

Use the Chi-squared test when:
Data Type: The data is categorical, not numerical. This test is used for frequencies (counts) rather than means.
Hypothesis: You are testing the independence of two categorical variables (e.g., whether gender is independent of voting preference) or the goodness-of-fit (e.g., testing if a sample distribution fits a theoretical distribution).
Distribution: The data should consist of observed frequencies, and expected frequencies should generally be 5 or more in each cell of the contingency table.
