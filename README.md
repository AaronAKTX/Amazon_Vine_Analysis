# Amazon_Vine_Analysis


## Main Objective

Analyze a data set of Amazon reviews. Several sets of data of Amazon reviews, broken up by product type are available online. The goal of this challenge is to extract one of these datasets, transform the data in PySpark to fit a predefined data schema, then load the data into a Postgres database hosted by AWS RDS instance I started.
Once the data is loaded, we then analyze a dataframe of that data in PySparks looking for any type of relationship between ratings and whether the reviewer is a part of the Vine program that pays revewiers for reveiws.

## Reviews

- I selected outdoor product reviews. In the dataset there were many more unpaid reviewers than paid reviewers. Also, it shoud be noted that I filtered the dataset so I would only evaluate reivews that had 20 or more votes and a minimum of 50% of the votes were "helpful". 
- Of the data I evaluated, there were 39875 reviews. 
<img src = https://github.com/AaronAKTX/Amazon_Vine_Analysis/blob/main/resources/total_helpful%20reviews.PNG> <br />

- Of the data I evaluated, there were 107 Vine reviews(Paid reviews) and 39768 non-Vine reviews. (see below)
<img src = https://github.com/AaronAKTX/Amazon_Vine_Analysis/blob/main/resources/vine reviews.PNG> <br />
<img src = https://github.com/AaronAKTX/Amazon_Vine_Analysis/blob/main/resources/non-vine reviews.PNG> <br />
<br />


### Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
- vehicle length
- ground clearance 
### Is the slope of the linear model considered to be zero? Why or why not?
The slope of the linear model is not considered to be zero. A zero would indicate that the was no relation between the variables and the miles per gallon. The p-value of this model is 5.35e-11 which is a very small chance that these variables are not significant.
### Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
I think it does a pretty good job of predicting mpg of MechaCar prototypes. The R-squared value is .7149 which means that around 70% of the variation in miles per gallon between different prototypes can be explained by or predicted by the model.

## Summary Statistics on Suspension Coils

The t-test results of all the lots and each individual lots show that lot 3 is statisically significantly different from the population. If we take the results from all the lots together, they are close enough to the population mean to not be statistically significant, but individually, lot 1, and lot 2 are fine but lot 3 has too much variance.

All lots: <br />
<img src = https://github.com/AaronAKTX/MechaCar_Statistical_Analysis/blob/main/resources/t.test_all.PNG>
<br />
Lot 1:<br />
<img src = https://github.com/AaronAKTX/MechaCar_Statistical_Analysis/blob/main/resources/t.test_lot1.PNG>
<br />
Lot 2:<br />
<img src = https://github.com/AaronAKTX/MechaCar_Statistical_Analysis/blob/main/resources/t.test_lot2.PNG>
<br />
Lot 3:<br />
<img src = https://github.com/AaronAKTX/MechaCar_Statistical_Analysis/blob/main/resources/t.test_lot3.PNG>
<br />
### The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not 
<br />
Here are pictures of the total summary and lot summary dataframes:<br />
<img src = "https://github.com/AaronAKTX/MechaCar_Statistical_Analysis/blob/main/resources/total_summary.PNG"><br />
<img src = "https://github.com/AaronAKTX/MechaCar_Statistical_Analysis/blob/main/resources/lot_summary.PNG"><br />

From the dataframes above it's easy to see that the total variance in psi across all lots  is less than 63 pounds per square inch. Therefore, the design specification is met for all lots. However, looking at the individual lots, Lot 3 has a variance of over 170 pounds per square inch. This specific lot does not meet the design specifications.

## T-Tests on Suspension Coils

Comparing the population mean against the mean of the sample we have yields the following results.
The mean of the psi in the three lots we have in our sample is 1498.78. This is not statistically significantly different from the population mean of 1500.

<img src = "https://github.com/AaronAKTX/MechaCar_Statistical_Analysis/blob/main/resources/t.test_all.PNG"><br />

Looking at the individual lots, you can see that lot 3 has a p-Value of .04168 and is statistically different from the population mean.

Lot 1: <br />
<img src = "https://github.com/AaronAKTX/MechaCar_Statistical_Analysis/blob/main/resources/t.test_lot1.PNG"> <br />
Lot 2:<br />
<img src = "https://github.com/AaronAKTX/MechaCar_Statistical_Analysis/blob/main/resources/t.test_lot2.PNG"> <br />
Lot 3:<br />
<img src = "https://github.com/AaronAKTX/MechaCar_Statistical_Analysis/blob/main/resources/t.test_lot3.PNG"> <br />

## Study Design: MechaCar vs Competition
A study of the MechaCar versus the competitors could be set-up. The study would analzye the cost of the vehicle and how that relates to the city or highway fuel efficiency, horse power, maintenance cost, and safety rating. The study would set the cost as the dependent variable and the other variables as independant variables.
The study could use a multiple linear regression to see how these independent variables affect the cost of the vehicle. Then compare these results with competitor's results to see how different factors effect cost for different manufacturers. There may be some useful information in there.

