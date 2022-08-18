# MechaCar_Statistical_Analysis
### Overview:
The MechaCar_mpg.csv contains 50 prototypes of AutosRU's newest vehicle, the MechaCar; The MechaCar, however, is suffering from production troubles that are blocking the manufacturing team’s progress. My job is to review the production data for insights that may help the manufacturing team.

### Software:
- RStudio RStudio: 2022.07.1+554 MacOs

### Deliverable 1: Linear Regression to Predict MPG
For this deliverable, I created a linear regression using the lm() function to assess the 6 variables (i.e., columns). The job of linear regression analysis is to calculate the slope and y-intercept values (also known as coefficients) that minimize the overall distance between each data point from the linear model. 

Using the summary() function I then obtained the statistical measurements: 
Based on the observations, we can analyze the Pr(>|t|) values which represent the probability that each coefficient contributes a random amount of variance to the linear model. According to my results, Intercept, Vechile_Length, and Ground_Clearance all have significance codes of '0' which means they are statistically unlikely to provide random amounts of variance to the linear model. In other words, those variables have a significant impact on quarter-mile race time. This could factor into the production problems the new vehicle is experiencing. 
Some good questions to ask yourself are:
- Is the vehicle too close or high off the ground? 
- Is the vehicle too long or short?

<img width="859" alt="Screen Shot 2022-08-17 at 5 52 23 PM" src="https://user-images.githubusercontent.com/104043438/185263271-a3e70b3b-6509-4bcb-9290-961b5b648b67.png">

The slope (hp) of the linear model was = -0.01846 so the linear regression model for our dataset is: qsec = -0.02 + 20.56

The p-value is also quiet small compared to the signifance value. Thus, we can state that there is sufficient evidence to reject our null hypothesis, which means that the slope of our linear model is not zero.

<img width="346" alt="Screen Shot 2022-08-17 at 6 08 08 PM" src="https://user-images.githubusercontent.com/104043438/185264688-bf2f8b16-d1c2-4559-9f3d-9d196429484e.png">

### Deliverable 2: Summary Statistics on Suspension Coils
The CSV file contained 3 variables: VehicleID, Manufacturing_Lot, and PSI (pounds per square inch). Below is the total summary for all vehicles which includes the mean, median, variance, and standard deviation (SD). The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. 

<img width="341" alt="Screen Shot 2022-08-17 at 6 21 45 PM" src="https://user-images.githubusercontent.com/104043438/185265873-ab573c3d-8fb1-4597-a1a6-5af1f2905c0a.png">

It would appear that the total variance for all 50 prototypes is below the necessary 100 PSI limit. This is why it's important to also view the lot summary which categorized all of the vehicles into three lots. As you can see below, lot 3, however,is over the necessary 100 or less PSI. Thus, the manufacturers should review their prototypes and lean more towards manufacturing vehicles that fall under the same category as lot 1 and 2.

<img width="496" alt="Screen Shot 2022-08-17 at 6 29 49 PM" src="https://user-images.githubusercontent.com/104043438/185266525-898c66a8-7861-4cf5-a3aa-bf91f898f8fd.png">

### Deliverable 3: T-Tests on Suspension Coils
For starters, I used the t.test() function to determine if the PSI across all manufacturing lots was statistically different from the population mean of 1,500 pounds per square inch. Assuming our significance level was the common 0.05%, our p-value is above our significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis. The p-value for all lots was = 1 and a p-value less than 0.05 (typically ≤ 0.05) is statistically significant. 

<img width="445" alt="Screen Shot 2022-08-17 at 6 45 57 PM" src="https://user-images.githubusercontent.com/104043438/185267990-4f868ec7-ddb9-4227-9751-3a214a536522.png">

P-value for lots 1-3:
- Lot 1: <img width="439" alt="Screen Shot 2022-08-17 at 6 50 56 PM" src="https://user-images.githubusercontent.com/104043438/185268486-62b350ce-ce72-46bf-a0e9-afecfee62101.png">

The p-value is above our significance level: we do not have sufficient evidence to reject the null hypothesis. 

- Lot 2: <img width="443" alt="Screen Shot 2022-08-17 at 6 51 22 PM" src="https://user-images.githubusercontent.com/104043438/185268517-c89ad3fa-51f1-4486-b931-118aaf748afd.png">

The p-value is below our significance level: which indicates strong evidence against the null hypothesis, as there is less than a 5% probability the null is correct. Lot 2 is statistically different from the population mean of 1,500 pounds per square inch. 

- Lot 3: <img width="464" alt="Screen Shot 2022-08-17 at 6 51 41 PM" src="https://user-images.githubusercontent.com/104043438/185268545-a7cf0844-a1bc-438a-8138-6ace88a33062.png">

The p-value is above our significance level: we do not have sufficient evidence to reject the null hypothesis. 

### Deliverable 4: Study Design: MechaCar VS Competition
Goal: Compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

##### Overall, the MechaCar does a decent job of staying within the required metrics. 
As you can see from my summary in deliverable 2, the total variance for all 50 prototypes is below the necessary 100 PSI limit. Lot 3, however, was above by more than half which is a problem when it comes to performance against other manufacturers. The MechCar needs to average their total variances out so that each lot stays below 100 PSI, or evaluate lot 1 and 2 to see the differences that correlate with lot 3's high variance. 
####### Metric: re-consider how heavy each MechaCar is (PSI) and compare that to other manufacturers to see where new vehicles fall on the bell curve distribution. 
####### Metric: Does the higher PSI found in lot 3 affect the speed of the vehicle enough to deter consumers? 

##### Potential hypothesises: 
• Null Hypothesis (Ho): MechaCar is priced accordingly based on its performance factors for its genre.

• Alternative Hypothesis (Ha): MechaCar is NOT priced accordingly based on its performance factors for its genre.

The manufacturers of the MechaCar should complete a two-sample t-test by comparing another similar manufacturer with their MechaCar design. Doing so would allow the manufacturers to analyze the statistical difference between the distribution means from the two samples. If the manufacturers wanted to compare their vehicle with multiple other competitors, conducting an ANOVA test should be suggested. 
