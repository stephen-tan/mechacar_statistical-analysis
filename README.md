# MechaCar Statistical Analysis


## Project Overview
The purpose of this project was to analyze datasets of a MechaCar automobile prototype to predict average miles per gallon (MPG), summary statistics of suspension coil pounds per square inch (PSI), perform statistical analyses such as t-tests, and use the data interpret the findings and compare them against vehicles from other manufacturers.<br/>

## Linear Regression to Predict MPG

### Linear Model
![Linear Regression](Resources/d1_lm.png)<br/>

### Summary Statistics
![Summary Statistics](Resources/d1_summary.png)<br/>

**Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?**</br>
*In the image above, vehicle length, vehicle weight, and ground clearance were three out of the six total variables that provided a non-random amount of variance because their p-values (column Pr(>|t|) were all less than 0.05 alpha (threshold) value.*

**Is the slope of the linear model considered to be zero? Why or why not?**</br>
*In the image above, the slope is non-zero because all of the coefficients are also non-zero, which means that there is a correlation that changes in MPG can be attributed to changes in the variables in the given dataset.*

**Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**</br>
*With an R-squared value of 0.7149, roughly 71% of the data fits the linear model, suggesting that the model is a good fit for effectively predicting MPG of the MechaCar prototypes.*

## Summary Statistics on Suspension Coils
**The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?**</br>
*Variance of the total summary (shown below) was 62.29 PSI and for each respective lot (in order of lots 1, 2, and 3, respectively) were 0.98, 7.47, and 170.29 PSI. As a result, both lots 1 and 2 were within specifications but not lot 3.*

### Total Summary
![Total Summary for Suspension Coils](Resources/d2_total_summary.png)<br/>

### Lot Summary
![Lot Summary for Suspension Coils](Resources/d2_lot_summary.png)<br/>


## T-Tests on Suspension Coils
**Null hypothesis**: Manufacturing lot has no effect on MechaCar suspension coil PSI</br>
**Alternative hypothesis**: Manufacturing lot affects MechaCar suspension coil PSI</br>

The p-value for all lots was found to be 0.683, which means that we accept the null hypothesis and that there is no effect of manufacturing lot on MechaCar performance. The population mean of 1498.06 PSI is statistically similar to that of the other manufacturing lots. For lots 1 and 2, the p-values are both < 0.05, which means that we reject the null hypothesis and that the PSI found in lots 1 and 2 are statistically different than that of lot 3, which had a p-value > 0.05.

### Total Summary
![T-Test All Lots Suspension Coils](Resources/d3_all_ttest.png)<br/>

### Lot Summaries

Lot 1</br>
![T-Test Lot 1 Suspension Coils](Resources/d3_lot1_ttest.png)<br/>

Lot 2</br>
![T-Test Lot 2 Suspension Coils](Resources/d3_lot2_ttest.png)<br/>

Lot 3</br>
![T-Test Lot 3 Suspension Coils](Resources/d3_lot3_ttest.png)<br/>


## Study Design: MechaCar vs Competition
Horsepower (hp) and safety rating are two important metrics that folks consider when purchasing a new car. The null hypothesis would be that the MechaCar prototype is not significantly different (performance-wise) from cars of another manufacturer. In order to test the null hypothesis, one could run ANOVA tests to see how much variance there is between each variable. In order to run the statitical analysis, one would first need to gather information from other car manufacturers, perhaps by fetching vehicle data APIs from different car manufacturers or by performing a web scrape.
