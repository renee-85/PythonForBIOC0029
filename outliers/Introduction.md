# Outliers

## __<font color=blue>What are outliers?</font>__
---

In the lab, we often repeat the same measurement (called __repeats or replicates__) to see how much random variation there is. Sometimes, one of these repeated measurements doesn’t match the others very well. For example, you might measure the absorbance of a protein sample three times to calculate its concentration using Lambert-Beer's law, but one result looks much higher or lower than the other two.
```{image} ./Images/Absorbance280nm.png
:alt: Example of possible outlier in technical repeats
:width: 600px
:align: center
```
Another common problem encountered in the lab are outliers in linear regression. For example, you might measure several (_e.g._ six) protein standards to create a standard curve for a colorimetric assay. Five of the points may line up nicely to form a straight line or smooth curve, while the sixth point sits far away from the trend.
```{image} ./Images/StandardCurve.png
:alt: Examples of possible outliers in standard curves
:width: 600px
:align: center
```

Being able to recognize and handle unusual results is an important skill in data analysis. If you suspect an __outlier__, start by checking for possible __mistakes__:
- Were the values entered correctly in your lab notebook?
- Could there be a calculation error, for example in one of the samples used to create a standard curve?
- Could one of the data points be a procedural mistake, such as accidentally adding protein to the same well twice and missing another well? Did you see a different volume in some wells?

If no obvious mistake is found, consider whether the unusual result could simply be due to __natural variation__. One important property of any dataset is how the values are distributed. Most data we measure tend to follow one of a few common __distributions__, for example normal (Gaussian), student's t, binomial, Poisson, or chi-squared (χ²). Knowing these distributions helps us estimate the probability of finding values within certain subranges within the span of the data. However, it’s not always easy to tell which distribution best describes a particular dataset, so careful judgement is needed! A data value that is an outlier on the assumption of a certain distribution may or may not be an outlier if the distribution is different.

Does this mean that we can never reject suspected outliers? No, but we need to __be very careful__! If suspect values are needlessly retained, _measurement quality_ suffers, while if they are wrongly rejected we may be guilty of _adjusting the data_, perhaps subconsciously, to fit our preconceived idea of what the results should be.

## __<font color=blue>How to detect and handle outliers?</font>__
---

### __<font color=red>Significance or statistical tests</font>__
---

Some __significance or statistical tests__ are designed to detect a __single outlier__ (_e.g._ the Grubbs test), while others can detect __multiple outliers__ at once (_e.g._ the generalized Extreme Studentized Deviate (ESD) test).

__Masking__ can occur when too few outliers are specified in the test. For example, if you test for a single outlier when there are actually two or more, the additional outliers can influence the test statistic enough that no points are identified as outliers.

__Swamping__ can occur when too many outliers are specified in the test. For example, if you test for two or more outliers when there is actually only one, the test may declare both points as outliers.

Because of the risk of masking and swamping, it is helpful to visually inspect your data before performing significance tests.

### __<font color=red>Weighted regression</font>__
---

Ideally, each condition used to construct a calibration or standard curve should be measured at least three times. If one of these values is suspect, it can then be subjected to a significance test to deterimine if it may be omitted from the data prior to calculating the regression line.

If the point is not omitted, __weighted regression__ will reduce the effect of a single outlier among each set of replicates. Weights can be estimated directly from sample variances.

We discussed weighted fitting in the section "SciPy For Data Fitting" in "Python basics".

### __<font color=red>Standardized or studentised residuals</font>__
---

Detection of outliers based on __standardized or studentized residuals__ is used widespread in linear regression.

### __<font color=red>Other tools: IQR and robust regression</font>__
---

Other commonly used tools are __the Inter-Quartile Range (IQR) method__ for large datasets and __robust regression__ for linear and non-linear regression.

Briefly, the IQR method detects outliers by labeling any data point that lies more than 1.5 times the IQR below the first quartile (25 %) or above the third quartile (75 %) as an outlier. 
```{image} ./Images/IQR.png
:alt: Examples of possible outliers in standard curves
:width: 600px
:align: center
```

Robust regression reduces the influence of outliers by _e.g._
- computing the slope as the median of all slopes between pairs of points (__Theil-Sen method__ for robust linear regression)
- giving them less weight during least squares fitting (__Huber Loss function__ for robust linear and non-linear regression)
- randomly picking subsets of data, building models on those, and then figuring out which model fits the majority of the data best (__random sample consensus (RANSAC) method__ for linear and nonlinear regression)
- ...

See [sklearn.linear_model.HuberRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.HuberRegressor.html), [sklearn.linear_model.TheilSenRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.TheilSenRegressor.html) and [sklearn.linear_model.RANSACRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.RANSACRegressor.html) for code for robust linear regression. See [scipy.optimize.least_squares](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.least_squares.html)'s option "loss" for robust non-linear regression with Huber Loss.

Robust regression is considerably more technical than the previous methods! We will not go into more detail here. We only include it to make you aware that it exists.