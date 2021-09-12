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
We have available to us the mpg test results for 50 prototype MechaCars.   Included in this data set we have multiple design specifications to identify ideal vehicle 
performance such as vehicle length, vehicle weight, spoiler angel, drivetrain, and ground clearance, were collected for each vehicle.    
With multiple linear regression model we are identifying which variables (vehicle weight, spoiler angle, ground clearance, AWD and vehicle length, in our case) in the dataset 
predict the mpg of MechaCar prototypes.  
**What are the relationships between variables and mpg of MechCar prototypes?**  

### **Null Hypothesis(HO) and Alternative Hypothesis (Ha) for Linear Regression** ###
With multiple linear regression model, we are establishing the following hypothesis:  

**HO**:  the slope of the linear model is zero or m = -0 (if there is no significant linear relationship, each dependent value would be determined by random chance and error.  Therefore, our linear model would be a flat line with a slope of 0).  
**Ha**: The slope of the linear model is not zero or m not equal to 0 (If there is a significant linear relationship, each dependent value would not be determined by 
random chance and error.  Therefore, our linear model would not be a flat line with a slope greater or lessser than 0.   

**1.  Which variables/coefficients provided a non-random amount of variance to the mpg values in the data set?**

To determine which variables, provide a non-random amount of variance to the mpg value we 
have to look at their individual **p-value**.  If the **p-value** is below 0.05 is statistically 
unlikely to provide random amounts of variance to the linear model, meaning that those 
variables have a significant impact on mpg.  According to our results (figure 1) ground 
clearance **p-value of 5.21**, vechicle length **p-value of 2.60** as well as 
intercept **p-value of 5.08** provided a non-random amount of variance to the mpg 
values in the dataset.  *When an intercept is statistically significant*, it means there 
are other variables and factors that contribute to the variation in mpg that have not been 
included in the model.  These variables may or may not be within our data set and may 
still need to be collected or observed.  This can be a continuous research process or exploring if variables have relationships (as described in Module 15.7.3).     

**2.  Is the slope of the linear model considered to be zero? Why or why not?**
Based on our results (Figure 1) **p-value** is 5.35 x 10-11, which is much smaller than our **assumed significance level of 0.05%**. Therefore, we can state that there is sufficient evidence to reject our null hypothesis. That indicates the slope of our linear model is not zero, meaning that there is significant linear relationship between variables and mpg of MechaCar prototype (from Module 15.7.2).

**3.  Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**
To determine if this linear model predict mpg of MechaCar prototypes effectively we need to take a look at its **r-squared value and p-value**. According to our results (below in
Figure 1) **r-squared is 0.7149** (and adjusted r-squared is 0.68) and indicates a strong positive linear relationship, therefore I can confirm that this linear model DOES 
effectively predict mpg of MechaCar prototypes (from Module 15.7.2).  Also,  the 3 *** indicator to the right, on the Intercept is an significance indicator that more than one 
independent variable impacts the variable of mpg.  
<p align="center">
  <img width="550" height=400" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/fig%201%20Linear%20Regress%20Results.jpg">
</p>
<p align="center">
Figure 1 - Linear Regression Results
</p>

# Deliverable #2
## Summary Statistics on Suspension Coils ## 

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils *must not exceed 100 pounds per square inch*. 
**Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?**

We'll start with **ALL LOTS**.  The current manufacturing data meets this design specification for all manufacturing lots in total. According to the results (Figure 2) shows that 
variance is 62.29 PSI and that is within requirements of not exceeding variance 100 PSI.

<p align="center">
  <img width="400" height=100" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/fig%202%20Summ%20Stats%20Susp%20Coils%20ALL%20Lots.jpg">
</p>
<p align="center">
Figure 2 - Summary Statistics on Suspension Coils for ALL LOTS
</p>

Next, we'll drill down to the **individual lots**.   The current manufacturing data partially meet this design specification for each lot separately. According to the results 
below (Figure 3), it shows that Lot 1 (variance of .97 PSI) and Lot 2 (variance 7.46 PSI) meet the design specification with and both are within requirements of not exceeding 
variance 100 PSI. 
Unfortunately, Lot 3 does not meet the design specification, (because of its variance of 170.28 PSI) and that exceeds the requirements variance of 100 PSI. Actually, Lot 3
causes disproportionately the variance at the full lot report level. This is described in more detail later in the study.    
<p align="center">
  <img width="500" height=225" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/fig%203%20summ%20stats%20Susp%20Coils%20for%20each%20lot%20individually.jpg">
</p>
<p align="center">
Figure 3 - Summary Statistics on Suspension Coils for Each Lot Individually 1, 2, & 3 ABOVE
</p>

# Deliverable #3 - 
## T-Tests on Suspension Coils ##

Below we will perform one-sample t-test, that is used to **determine whether there is a statistical difference between the means of a sample dataset (suspension coil data set) and 
a population dataset with a given mean of 1,500 PSI**.  
First, we establish the following hypothesis:  

**HO**:  There **is no** statistical difference between the suspension coil data set mean and its presumed population mean of 1500 PSI (they are statistically similar).  
**Ha**: There **is** statistical difference between the suspension coil data set mean and its presumed population mean of 1500 PSI (they are statistically different).  

In order to reject of fail to reject our null hypothesis we have to look at the **p-value** that determines if there is a statistical difference between the observed sample mean and 
its presumed population mean.   

Across all manufacturing lots, 1, 2, and 3 combined, we can see below that the **true mean is 1498.78**.  This combined with a **p-value of .06**, which is higher than the **assumed significance level of 0.05** there **is NOT enough evidence to support rejecting the null hypothesis (we will accept the null hypothesis)**.   In other words, the mean of all three of these manufacturing lots, combined,  **is statistically similar to the presumed population mean of 1500**.   

<p align="center">
  <img width="650" height=200" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/fig%204%20first%20one%20t-test%20Lot%20all.jpg ">
</p>
<p align="center">
Figure 4 - T-Test ALL LOTS -Combined Total
</p>

Next, we look at the individual lots.    

According to the results below in Figure 5:   
1.  Lot 1 has the same true sample mean of 1500 with a **p-value of 1**.  We will **accept the null hypotheseis** that there is no statistical difference bettween the observed 
                 sample mean and the presumed sample population mean of 1500.   
2.  Lot 2 has the same results with a sample mean of 1500.2 a pvalue of .061.  Therefore, again, we will **accept the null hypothesis** because the sample mean of 1500 are 
                 statistically similar.   
3.  However, Lot 3, is different.  Here **the sample mean is 1496.14 and the p-value is .04**, which is lower than the **assumed significance level of .05**. For this report, we 
                 will **reject the null hypothesis**.    
<p align="center">
  <img width="400" height=600" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/figure%205%20all%20indiv%203%20lots%20.jpg">
</p>
<p align="center">
Figure 5 - T-Test Lots - Individual 
</p>

# Deliverable #4 - 
## A new Study Design: MechaCar vs Competition ##
Deliverable Requirements:
Using your knowledge of R, design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

The statistical study design has the following:
-  A **metric** to be tested is described and defined 
-  A null **hypothesis and an alternative hypothesis** is described
-  A **statistical test** is described to test the hypothesis
-  This study would involve collecting **data on MechaCar** and **data from comparable models across several different manufacturers over the last 3 years**.

Questions to be answered:   
1.  What are the competitions' comparable models?
2.  Which cars will MechaCar be competing with head-to-head? which cars will be included in the study?
3.  Which factors will look at the study to determine the relevant to selling price?
4.  What Metrics are important to the genre that MechCar is marketing too?   
5.  What Metrics are available?  

Ideally, you would collect data for comparable models across all major manufacturers for past 3 years for the following metrics:
-  MPG (Gasoline Efficiency): Independent Variable
-  Current Price (Selling): Dependent Variable
-  Average Annual Cost of ownership (Maintenance): Independent Variable
-  Resale Value: Independent Variable
-  Safety Feature Rating: Independent Variable
-  Drive Package : Independent Variable
-  Engine (Electric, Hybrid, Gasoline / Conventional): Independent Variable
-  Average Annual Cost of ownership (Maintenance): Independent Variable

Below is a Potential Hypothesis:
**Null Hypothesis (Ho): MechaCar is priced correctly based on its performance of key factors for its genre.**
**Alternative Hypothesis (Ha): MechaCar is NOT priced correctly based on performance of key factors for its genre.**

The statistical tests best suited to this task would be a multiple linear regression to determine the factors that have the highest correlation/predictability with the list selling price (dependent variable).    
We could start with the following question: 
-   Which combination has the greatest impact on price?  how many of them?

*This is where I would start with the research and see where it leads us.*   

<p align="center">
   <img width="400" height=250" src="https://github.com/mjrotter4445/MechaCar_Statistical_Analysis/blob/main/Graphics/gear-wheels-gears-free-vector-hd-png.png">
</p>



Graphics Sources:  
Data Scientist, - Analytics Vidhya Blog site -  https://www.analyticsvidhya.com/blog/2020/12/quick-guide-to-perform-hypothesis-testing/   
Gears and Scientists -  KindPNG.com site  -  https://www.kindpng.com/imgv/TxbwxJ_vector-gear-wheels-gears-free-vector-hd-png/
