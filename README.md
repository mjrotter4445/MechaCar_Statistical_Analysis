# MechaCar Analysis 🚙 🚗 🏎️
*Statistics and R* 
## Background  
For this project we are performing statistical testing in programming language R for MechaCar car company.  Statistical tests provide data-based insight on the company performance and suggest additional testing for comparison of MechaCar company against their competition.    

## Resources
### Data Sources:
-  *MechaCar_mpg.csv*
-  *Suspension_Coil.csv*
### Software: 
-  **RStudio**
-  Languages: **R**

<p align="center">
  <img width="500" height=250" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/heading%20scientist%20graphic.jpg">
</p>
 

# Deliverable #1 - 
## Linear Regression to Predict MPG ## 

### **The Statistical question** ### 
There are mpg test results for 50 prototype MechaCars.   Multiple design specifications to identify ideal vehicle performance such as vehicle length, vehicle weight, spoiler angel, drivetrain, and ground clearance, were collected for each vehicle.    
With multiple linear regression model we are identifying which variables (vehicle weight, spoiler angle, ground clearance, AWD and vehicle length in our case) in the dataset predict the mpg of MechaCar prototypes.  
**What are the relationships between variables and mpg of MechCar prototypes?**  

### **Null Hypothesis and alternative hypothesis for linear regression** ###
With multiple linear regression model, we are establishing the following hypotheses:  
**HO**:  the slope of the linear model is zero or m = -0 (if there is no significant linear relationship, each dependent value would be determined by random chance and error.  Therefore, our linear model would be a flat line with a slope of 0).  
**Ha**: The Slope of the linear model is not zero or m not equal to 0 (If there is a significant linear relationship, each dependent value would not be determined by random change and error.  therefore, our linear model would not be a flat line with a slope greater or lessser than 0.   

**1.  Which variables/coefficients provided a non-random amount of variance to the mpg values in the data set?**

To determine which variables, provide a non-random amount of variance to the mpg value we 
have to look at their individual **p-value**.  If the **p-value** is below 0.05 is statistically 
unlikely to provide random amounts of variance to the linear model, meaning that those 
variables have a significant impact on mpg.  According to our results (figure 1) ground 
clearance (**p-value** = 5.21 x 10-8), vechicle length (**p-value** = 2.60 x 10-12) as well as 
intercept (**p-value** = 5.08 x 10-8) provided a non-random amount of variance to the mpg 
values in the dataset.  When an intercept is statistically significant, it means there 
are other variables and factors that contribute to the variation in mpg that have not been 
included in the model.  These variables may or may not be within our data set and may 
still need to be collected or observed.  This can be a continuous research process or exploring if variables have relationships (as described in Module 15.7.3).     

**2.  Is the slope of the linear model considered to be zero? Why or why not?**
Based on our results (Figure 1) **p-value** is 5.35 x 10-11, which is much smaller than our **assumed significance level of 0.05%**. Therefore, we can state that there is sufficient evidence to reject our null hypothesis. That indicates the slope of our linear model is not zero, meaning that there is significant linear relationship between variables and mpg of MechaCar prototype (from Module 15.7.2).

**3.  Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**
To determine if this linear model predict mpg of MechaCar prototypes effectively we need to take a look at its r-squared and p-value. According to our results (Figure 1) r-squared is 0.7149 (and adjusted r-squared is 0.68) and indicates a strong positive linear relationship, therefore I can confirm that this linear model effectively predicts mpg of MechaCar prototypes (Source 1: Module 15.7.2).
<p align="center">
  <img width="550" height=400" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/fig%201%20Linear%20Regress%20Results.jpg">
</p>
<p align="center">
Figure 1 - Linear Regression Results
</p>

# Deliverable #2
## Summary Statistics on Suspension Coils ## 

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. 
**Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?**

We'll start with **ALL LOTS**.  The current manufacturing data meet this design specification for all manufacturing lots in total. According to the results (Figure 2) shows that variance is 62.29 PSI, that is within requirements of not exceeding variance 100 PSI.

<p align="center">
  <img width="400" height=100" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/fig%202%20Summ%20Stats%20Susp%20Coils%20ALL%20Lots.jpg">
</p>
<p align="center">
Figure 2 - Summary Statistics on Suspension Coils for ALL Lots
</p>

Next, we'll drill down to the **individual lots**.   The current manufacturing data partially meet this design specification for each lot separately. According to the results below (Figure 3), it shows that Lot 1 (variance of .97 PSI) and Lot 2 (variance 7.46 PSI) meet the design specification with and both are within requirements of not exceeding variance 100 PSI. 
Unfortunately, Lot 3 does not meet the design specification, (because of its variance of 170.28 PSI) and that exceed the requirements variance of 100 PSI.
<p align="center">
  <img width="500" height=225" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/fig%203%20summ%20stats%20Susp%20Coils%20for%20each%20lot%20individually.jpg">
</p>
<p align="center">
Figure 3 - Summary Statistics on Suspension Coils for Each Lot Individually 1, 2, & 3 ABOVE
</p>

# Deliverable #3 - 
## T-Tests on Suspension Coils ##

Below we will perform one-sample t-test, that is used to determine whether there is a statistical difference between the means of a sample dataset (suspension coil data set) and a population dataset with a given mean of 1,500 PSI. With the t-test, we define the following hypothesis:

H0: There is no statistical difference between the suspension coil data set mean and its presumed population mean of 1,500 PSI.

Ha: There is statistical difference between the suspension coil data set mean and its presumed population mean of 1,500 PSI.

In order to reject or fail to reject our null hypothesis we have to look at the **p-value** that determines if there is a statistical difference between the observed sample mean and its presumed population mean. According to the result (Figure 4) **p-value** for all manufacturing lots is 0.5117, for lot 1 = 1.00, for lot 2 = .60, and for lot 3 = 0.04. In only 2 cases **p-value** is above the assumed significance level of 0.05. Therefore, there is evidence to reject the null hypothesis, meaning that the two means are significantly statistically different.   

<p align="center">
  <img width="650" height=200" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/fig%204%20first%20one%20t-test%20Lot%20all.jpg ">
</p>
<p align="center">
Figure 4 - T-Test All Lots - Total
</p>

<p align="center">
  <img width="400" height=600" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/figure%205%20all%20indiv%203%20lots%20.jpg">
</p>
<p align="center">
Figure 5 - T-Test Lots - Individual 
</p>






# Deliverable #4 - 
NEED MORE IDEAS HERE -  work on this part NEXT 


Study Design: MechaCar vs Competition
Deliverable Requirements:
Using your knowledge of R, design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

The statistical study design has the following:

A metric to be tested is mentioned
A null hypothesis or an alternative hypothesis is described
A statistical test is described to test the hypothesis
This study would involve collecting data on MechaCar and its comparable models across several different manufacturers over the last 3 years.

What are the competitions' comparable models,
Which cars will MechaCar be competing with head-to-head? which cars will be included in the study?
Which factors will look at the study to determine the relevant to selling price?
Metrics
Collecting data for comparable models across all major manufacturers for past 3 years for the following metrics:

Safety Feature Rating: Independent Variable
Current Price (Selling): Dependent Variable
Drive Package : Independent Variable
Engine (Electric, Hybrid, Gasoline / Conventional): Independent Variable
Resale Value: Independent Variable
Average Annual Cost of ownership (Maintenance): Independent Variable
MPG (Gasoline Efficiency): Independent Variable
Hypothesis: Null and Alternative
After determining which factors are key for the MechaCar's genre:

Null Hypothesis (Ho): MechaCar is priced correctly based on its performance of key factors for its genre.
Alternative Hypothesis (Ha): MechaCar is NOT priced correctly based on performance of key factors for its genre.
Statistical Tests
A multiple linear regression would be used to determine the factors that have the highest correlation/predictability with the list selling price (dependent variable); which combination has the greatest impact on price (it may be all of them!)






