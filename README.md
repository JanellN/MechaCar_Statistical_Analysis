# MechaCar_Statistical_Analysis

## Overview

A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.
In this challenge, you’ll help Jeremy and the data analytics team do the following:
Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
1. Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
2. Run t-tests to determine if the manufacturing lots are statistically different from the mean population
3. Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

This new assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:
Deliverable 1: Linear Regression to Predict MPG
Deliverable 2: Summary Statistics on Suspension Coils
Deliverable 3: T-Test on Suspension Coils
Deliverable 4: Design a Study Comparing the MechaCar to the Competition


## Results
## Linear Regression to Predict MPG

mpg = (6.267)vehicle_length + (0.0012)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD + (-104.0)


![dev1](https://user-images.githubusercontent.com/103154070/180671154-991e0a21-27b8-4c00-a9ed-5942d3ffae59.png)


* The most significant variables in our dataset which show a non-random effect on the MPG of the MechaCar are the **Vehicle Length** and the **Ground Clearance**.  The intercept was also statistically significant, indicating that there are likely other factors, not included in our dataset, that have a strong impact on the MPG.


* The p-Value for this model, p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, which further indcates that the slope of this linear model is not zero.  This means that the relationship between our variables and the miles per gallon is subject to more than random chance.

* Although there are still unconsidered factors, this model does predict the mpg of the MechaCar prototype with some relative effectiveness. The r-squared value of 0.7149 indicates that the model is 71.5% accurate.

### Summary Statistics on Suspension Coils
<img width="550" alt="totalsummary" src="https://user-images.githubusercontent.com/103154070/180671849-24b551f7-3c0d-482a-a3a2-9e5fddf57b5a.png">

![lot_summary](https://user-images.githubusercontent.com/103154070/180671838-e50a1721-8df3-49ad-8d9b-effdc2018437.png)

* While the overall variance, as shown in the Total Summary data above, is under 100 psi and meets specifications, there is a problem with one of the individual lots. As shown in the Lot Summary stats, the variance for Lot 3 is well over the acceptable threshold, at 170.28.This very simple boxplot illustrates the differences between the lots:

![plt2](https://user-images.githubusercontent.com/103154070/180671855-927f74a7-dbad-4c91-855e-4351322961ea.png)



### T-Tests on Suspension Coils

![onesamplettest](https://user-images.githubusercontent.com/103154070/180672140-3d6051bd-b053-416b-8971-16d872a9ac58.png)

* Lot 1: p-value = 1, alpha = .05; 1 > .05, which means Lot 1 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

* Lot 2: p-value = .6072, alpha = .05; .60 > .05, which means Lot 2 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.

* Lot 3: p-value = .04168, alpha = .05; .04 < .05, which means it is statistically significant from the normal distribution and normality cannot be assumed. However, the mean falls within the 95% confidence interval.

* The overall manufacturing, Lot 1, and Lot 2 show a normal distribution. Therefore, there is not sufficient evidence to reject the null hypothesis, which shows the two means are statistically similar.

### Study Design: MechaCar vs Competition

When comparing MechaCar to its competitor’s other metrics that could be of interest to a consumer could include cost, car color, city fuel efficiency, highway fuel efficiency, horsepower, maintenance cost, or safety rating. The next metrics to test should be cost, city and highway fuel efficiency, horsepower, safety rating, and carbon waste output.

We will be testing whether or not the MechaCar has statistically significant differences in these metrics compared to competing models. The null hypothesis will be that these observables don't vary significantly from the competition, and the alternative hypothesis will be that the MechaCar does indeed vary significantly in these variables compared to the competition.

We will perform one-tailed t-tests in order to determine if the MechaCar has higher or lower observed values in these variables than the competition according to which direction the consumer would prefer. The consumer would want the cost to be lower, the city and highway fuel efficiency to be higher, the horsepower to be higher, the safety rating to be higher, and the carbon waste output to be lower.

In order to run these statistical tests, we would need the cost, fuel efficiency, horsepower, safety rating, and carbon waste output data from the MechaCar as well as the MechaCar's competitors.

