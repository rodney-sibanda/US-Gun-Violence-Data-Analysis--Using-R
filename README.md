# US-Gun-Violence-Data-Analysis---Using-R

# Problem Statement 
1. Is there a relationship between gun ownership and gun violence in the United States?
2. Do states with greater gun ownership also have more gun-related deaths?


# Dataset 
- Data Belongs to:

  - U.S. Centers for Disease Control and Preventionre

  - Kalesan B, Villarreal MD, Keyes KM, et al, Gun ownership and social gun culture. Injury Prevention 2016;22:216-220.

- The variables included in the dataset are:
  - state: Two-letter state code.
  - mortality_rate: The number of gun-related deaths per 100,000 people in each state in 2014.
  - ownership_rate: The percentage of adults in each state who own a gun, according to a 2013 survey of 4,000 adults.


# Uploading Data

<img width="1430" alt="image" src="https://user-images.githubusercontent.com/126027138/221377408-dc447356-1609-4f80-a8a7-565bf52dc3dc.png">

# Relationship between gun ownership and gun mortality in the US

![image](https://user-images.githubusercontent.com/126027138/221377789-90abd26e-4113-423a-a267-e0f30b738fc0.png)

- Plotted using ownership rate as the predictor and mortality rate as the response.
- We can see that the relationship looks moderately linear but not strong enough to be able to comfortably use a linear model to predict the mortality rate in the US from the gun ownership rate. Since the relationship is linear we can quanitfy the strength of the relationship with the correlation coefficient

Correlation: ![image](https://user-images.githubusercontent.com/126027138/221378211-755edcb5-47c4-43ed-ad72-ff0d2d83a837.png)
 The correlation coefficient of 0.678 suggests a moderate positive linear relationship between the gun ownership rate and the mortality rate due to gun violence. The correlation coefficient of 0.678 suggests that this trend is moderately strong, but not strong enough to predict the mortality rate in the US from the gun ownership rate with a high degree of accuracy.
 
 # Summary 
 
 ![image](https://user-images.githubusercontent.com/126027138/221379597-34bd0a99-9524-44ba-ab4b-164ee99f7e40.png)
- The coefficient estimates indicate that for every one-unit increase in the mortality rate, there is a corresponding increase of 0.02245 in the ownership rate
- The R-squared value of 0.46 indicates that the model explains 46% of the variation in the ownership rate, which is a moderate level of explained variance
- The p-value associated with this coefficient is very small (6.24e-08), which suggests that this relationship is statistically significant
- In terms of the residuals, they appear to be relatively small, with no obvious pattern or trend in their distribution. This suggests that the linear regression model is a reasonable fit for the data

Overall, based on this summary, it can be concluded that there is a statistically significant positive relationship between gun violence and gun ownership in the US, as measured by the mortality rate and ownership rate respectively. However, it is important to note that the model only explains 46% of the variation in the ownership rate, which suggests that there may be other important factors that are not accounted for in the model
 
 # Regression Residuals
 
 ![image](https://user-images.githubusercontent.com/126027138/221378778-eaf1b791-237b-40ec-b526-34628fa71ebf.png)


Using residual plots, check for:
(1) linearity
(2) nearly normal residuals
(3) constant variability

![image](https://user-images.githubusercontent.com/126027138/221378901-a1f60c35-b54f-41d3-88f9-17e2e68bbe4c.png)

The residual plots of suggest that the model assumption of states with greater gun ownership also have more gun-related deaths is NOT true. With a positive non - linear pattern being shown in the first residual graph and also with the uneven right-skewed histrogram, we can come to the conclusion that the underlying assumption is false. 
