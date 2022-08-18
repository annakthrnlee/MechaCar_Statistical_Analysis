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

It would appear that the total variance for all 50 prototypes is below the necessary 100 PSI limit. This is why it's important to also view the lot summary which categorized all of the vehicles into three lots. As you can see below, lot 3 is, however, over the necessary 100 or less PSI. Thus, the manufacturers should review their prototypes and lean more towards manufacturing vehicles that fall under the same category as lot 1 and 2.

<img width="496" alt="Screen Shot 2022-08-17 at 6 29 49 PM" src="https://user-images.githubusercontent.com/104043438/185266525-898c66a8-7861-4cf5-a3aa-bf91f898f8fd.png">
