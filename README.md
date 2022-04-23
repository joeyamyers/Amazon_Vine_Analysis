# Amazon_Vine_Analysis

## Resources 
- Data Source: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Pet_Products_v1_00.tsv.gz

## Overview
## Purpose
In this project, I have analyzed Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Amazon invites trusted reviewers based on their past reviews on purchased products to help other Amazon customers make informed purchased. Companies will then pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

I have chosen to analyze these reviews for pet products available on Amazon. I used PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then, I used PySpark to determine if there is any bias toward favorable reviews from Vine members in the dataset. 

## Results
I set out to determine if there is any bias towards reviews that were written as part of the Vine program. I wanted to know if getting a paid Vine review causes a difference in the percentage of 5-star reviews given for pet products.

Firstly, I filtered the reviews to only include those that received 20 or more votes in order to pick reviews that are more likely to be helpful. Additionally, I filtered the rows again to include only those that earned at least a 50% rate of "helpful" reviews. I sorted the reviews into two dataframes: one with Vine reviews and the other with non-Vine reviews. 

### Reviews
#### Total Reviews
As one may expect, the non-Vine reviews far out numbered the Vine reviews.
- Vine reviews: 170
- non-Vine reviews: 37,840

#### 5-Star Count
- Vine reviews with 5 stars: 65
- non-Vine reviews with 5 stars: 20,612

#### 5-Star Percentage
- Vine reviews' 5-star percentage: 38.2%
- non-Vine reviews' 5-star percentage: 54.5%


## Summary
### Bias
Based off of my findings, it does not indicate that there is any positivity bias for reviews in the Vine program as Vine reviewers gave out 5-star ratings at a lower rate than non-Vine reviewers. This is significant because it builds the consumers trust that they can depend on these reviews from Amazon Vine for products they are interested in. 

Additionally, it would be helpful to determine the variance of the reviews for each individual pet product between Vine reviews and non-Vine reviews. Seeing the disparities in the ratings would provide even more insight for the helpfulness of the Amazon Vine program. Because the Vine programs 5-star rate is lower than non-Vine memebers, it is a possibility that Amazon finds that these reviewers simply review the product on a stricter scale.

Tools Used:
- AWS: RDS
- Apache Spark
- PostgreSQL