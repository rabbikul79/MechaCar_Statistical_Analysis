# MechaCar_Statistical_Analysis
## Purpose:
Designing a linear model that predicts the mpg of MechaCar prototypes using several variables such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance to identify ideal vehicle performance.

## Analysis:

### Linear Regression to Predict MPG

* Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
  - The vehicle length and vehicle ground clearance variables provide a non-random amount of variance. Other variables have p-values that indicate a random    amount of variance.

* Is the slope of the linear model considered to be zero? Why or why not?
  - Analysis indicates the slope of the linear model is not zero. The p-value: 5.35e-11 is much smaller than the 5% assumed significant level, indicating there is enough evidence to reject our null hypothesis.

* Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
  - This model predicts the mpg of MechaCar prototypes effectively. The Multiple R-squared: 0.7149 indicates that approximately 71% of all mpg predictions will be determined.!

![D1_Result](https://user-images.githubusercontent.com/85530486/142143786-a75ee812-5fb9-4c2b-a661-f23ca7c72adf.png)

### Summary Statistics on Suspension Coils

* The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

The current manufacturing data meets this design specification for all manufacturing lots in total with a Var_PSI of 62.29356 which is well within the 100 PSI variance as shown below:

![D2_TotSum_DF](https://user-images.githubusercontent.com/85530486/142144977-1f75a42f-83e7-4cd0-b575-006a97ee66b5.png)

Performing different levels of analysis is critical to support overall findings and determine any outliers/anomalies.

- Lot1 has a Var_PSI of .09795918 which is significantly within the 100 PSI variance.
- Lot2 has a Var_PSI of 7.4693878 which is significantly within the 100 PSI variance.
- Lot3 has a Var_PSI of 170.2861224 which is NOT significantly within the 100 PSI variance. This lot is skewing the results of the total manaufacturing lots results.

![D2_lotSum_DF](https://user-images.githubusercontent.com/85530486/142145281-c2fa20e6-736d-4527-8184-8c1a3ef2e254.png)

### T-Tests on Suspension Coils

* All Lot - The t-test analysis results reveal that for all lots, the p-value = 0.06028 which is outside the significance level of 5%, which indicates there is not sufficient evidence to reject the null hypothesis. The analysis predicts that the dataset mean of 1498.78 is statistically similar to the population mean of 1500. The t-test results are shown below:

![D3_Mech_coilPSI_t-test](https://user-images.githubusercontent.com/85530486/142145589-b4b30589-9125-480c-8ff6-37f1422dfadd.png)

* Lot 1 - The t-test analysis results reveal that for Lot 1, the p-value = 1 which is outside the significance level of 5%, which indicates there is not sufficient evidence to reject the null hypothesis. The analysis predicts that the dataset mean of 1500 is the same as the population mean of 1500. The t-test results are shown below:

![D3_lot1_t-test](https://user-images.githubusercontent.com/85530486/142145804-45fdcf10-a325-4b34-b086-df26f6818f7a.png)

* Lot 2 - The t-test analysis results reveal that for Lot 2, the p-value = 0.6072 which is outside the significance level of 5%, which indicates there is not sufficient evidence to reject the null hypothesis. The analysis predicts that the dataset mean of 1500.2 is almost the same as the population mean of 1500. The t-test results are shown below:

![D3_lot2_t-test](https://user-images.githubusercontent.com/85530486/142145915-067fcd40-5c58-4bc2-a5c1-d1edfba0c9b3.png)

* Lot 3 - The t-test analysis results reveal that for Lot 3, the p-value = 0.04168 which is inside the significance level of 5%, which indicates there is sufficient evidence to reject the null hypothesis. The analysis predicts that the dataset mean of 1496.14 is not statistically different to the population mean of 1500. The t-test results are shown below:

![D3_lot3_t-test](https://user-images.githubusercontent.com/85530486/142146629-31fc305a-b2ee-4676-987b-ddef1a8ab628.png)

### ## Study Design: MechaCar vs Competition

As the EV's are increasing in the market everyday consumer who are still unsure about making that big leap, but they are concerned about the fuel economy. A design analysis should be perfomed how MechaCar will perform in mpg. We performed linear regression to predict mpg and found that vehicle length and ground clearance directly affect mpg.

In your description, address the following questions:

What metric or metrics are you going to test?
In addition to the current six variables, other metrics to consider include trip distances (short = 0-100 miles), (long = 101-500 miles), weather variances such as rain and fog, and location such as urban vs rural.

What is the null hypothesis or alternative hypothesis?
Null Hypothesis (Ho): Based on the above metrics, MechaCar has the same mpg than the competition.
Alternative Hypothesis (Ha): MechaCar does NOT have the same mpg as the competition.

What statistical test would you use to test the hypothesis? And why?
We propose a multiple linear regression model to determine the factors that have the highest correlation with the mpg.

What data is needed to run the statistical test?
The mpg would be the dependent variable; the others (in combination) would be independent variables to determine which has the greatest impact on the mpg.
