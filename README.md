# Amazon_Vine_Analysis

## Overview
## Purpose
In this project, I am analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies will pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

I have chosen to analyze these reviews for pet products available on Amazon. I used PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then, I used PySpark to determine if there is any bias toward favorable reviews from Vine members in the dataset. 

## Analysis
### Amazon Vine Program Bias
I set out to determine if there is any bias towards reviews that were written as part of the Vine program. I wanted to know if having a paid Vine review makes a difference in the percentage of 5-star reviews.