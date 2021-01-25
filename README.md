# MechaCar_Statistical_Analysis

## Linear Progression to Predict MPG

<p align="center">
  <img width="460" height="300" src="https://github.com/LManago/MechaCar_Statistical_Analysis/blob/main/Images/Linear%20Regression%20to%20Predict.PNG">
</p>

* Each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model. According to our results, vehicle length, ground clearance and intercept provide a non-random amount of variance to the linear model of mpg.

* the multi linear model is:
mpg = 6.27 * vehicle_length + 1.25e-3 * vehicle_weigth + 6.88e-2 * spoiler_angle -3.41 * AWD + 3.55 * ground_clearance - 1.04e+2

Approximated to:
mpg = 6.27 * vehicle_length - 3.41 * AWD + 3.55 * ground_clearance - 104
The slope of the linear model is not considered to be zero.

* R-square is 0.71 so 71% of the variations in mpg can be explained by changes in the vehicle length, the vehicle weight, the spoiler angle, the drivetrain and the ground clearance. We can consider this linear model as fairly efficient to predict mpg of MechaCar prototypes.

## Summary Statistics of Suspension Coils

<p align="center">
  <img width="460" height="100" src="https://github.com/LManago/MechaCar_Statistical_Analysis/blob/main/Images/Suspension%20Coil%20Total%20Summary.PNG">
</p>
<p align="center">All Manufacturing Lots</p>

<p align="center">
  <img width="460" height="100" src="https://github.com/LManago/MechaCar_Statistical_Analysis/blob/main/Images/Lost%20Summary.PNG">
</p>
<p align="center">By Each Manufacturing Lot</p>

* The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.
The design specs are for all manufacturing lots in total with a global variance of 62.3 psi.
On the lot level, Lot 1 and Lot 2 are into specs with variances of 0.98 and 7.5 psi. The Lot 3 is out of specs with a variance of 170.3 psi.

## T-Tests on Suspension Coils
<p align="center">
  <img width="460" height="100" src="https://github.com/LManago/MechaCar_Statistical_Analysis/blob/main/Images/One%20sample%20t%20test.PNG">
</p>
<p align="center">T-test All Manufacturing Lots Against Mean PSI of the Population</p>
* The significance level is the common 0.05 percent, our p-value of 0.7486 is above the significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we can state that the PSI across all manufacturing lots is statiscally similar to the population mean of 1498.78 psi.

##### Lot 1 & 2

<p align="center">
  <img width="460" height="100" src="https://github.com/LManago/MechaCar_Statistical_Analysis/blob/main/Images/PSi%20lot%201%20sample%20t-test.PNG">
</p>
<p align="center">
  <img width="460" height="100" src="https://github.com/LManago/MechaCar_Statistical_Analysis/blob/main/Images/PSi%20lot%202%20sample.PNG">
</p>

* The p-value is below the significance level of 0.05 percent, so we can reject the null hypothesis and conclude that the PSI across the Lot 1 is statistically different from the population mean.

##### Lot 3

<p align="center">
  <img width="460" height="100" src="https://github.com/LManago/MechaCar_Statistical_Analysis/blob/main/Images/PSi%20lot%203%20sample.PNG">
</p>

* The p-values are above the significance level, so we can conclude that the PSI for Lot2 and Lot3 are statistically similar to the population mean.

## Study Design: MechaCar vs Competition

To compare the performance of the MechaCar prototype against the vehicles from the competition, we will perform a statistical analysis based on the following metrics:

* safety rating.
* "0 to 60 mph" time
* fuel economy (mpg)
* power
* braking distance

The null hypothesis would be each performance metrics is statistically similar between the MechaCar prototype and all vehicle from the other manufacturers.

We would use a one-way ANOVA test; in this analysis we would compare the means for each metric across the different manufacturers.

To perform the test, we would need data of MechaCar vehicles and its competition, all gathered in a single dataframe where each metric is a column.

