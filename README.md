# Amazon_Vine_Analysis


## Main Objective

Analyze a data set of Amazon reviews. Several sets of data of Amazon reviews, broken up by product type are available online. The goal of this challenge is to extract one of these datasets, transform the data in PySpark to fit a predefined data schema. Load the data into a Postgres database on an RDS instance hosted by AWS.
Once the data is loaded, it is then used to populate a dataframe in PySparks looking for any type of relationship between rating values and whether the reviewer is a part of the Vine program that pays revewiers for reveiws.

## Reviews

- I selected outdoor product reviews. In the dataset there were many more unpaid reviewers than paid reviewers. Also, it shoud be noted that I filtered the dataset so I would only evaluate reivews that had 20 or more votes and a minimum of 50% of the votes were "helpful". 
- Of the data I evaluated, there were 39875 reviews. 
<img src = https://github.com/AaronAKTX/Amazon_Vine_Analysis/blob/main/resources/total_helpful%20reviews.PNG> <br />

- Of the data I evaluated, there were 107 Vine reviews(Paid reviews) and 39768 non-Vine reviews. (see below)
<img src = https://github.com/AaronAKTX/Amazon_Vine_Analysis/blob/main/resources/vine%20reviews.PNG> <br />
<img src = https://github.com/AaronAKTX/Amazon_Vine_Analysis/blob/main/resources/non-vine%20reviews.PNG> <br />
<br />
- The percentage of the Vine and Non-Vine reviews that were 5 stars were both right around 52%. See the summary below:
- 
<img src = https://github.com/AaronAKTX/Amazon_Vine_Analysis/blob/main/resources/summary.PNG> <br />

## Summary
- After the analysis, I did not see any signs of positivity bias from the Vine participants vs the non-vine participants. There was such a small subset of Vine reviews in my dataset though, I think further analysis would be prudent. More datasets of different products could be added to collect more data. These results may bring to light any bias that was missed by my analysis. Also, specific reviewers could be analyzed to see if there are viners out there just popping 5 stars on every product they review.
