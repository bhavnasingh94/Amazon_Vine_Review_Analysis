# Amazon_Vine_Review_Analysis

## Overview

The objective of this project is to analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

I, first, picked one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, we use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. 

## Analysis

Using the knowledge of ETL process, I created a new database with Amazon RDS. A python script using PySpark was used to analyze the dataset written by Vine and Non-Vine members. This was then compared to the most favorable 5-star reviews from each group. We selected the rows where the number of helpful_votes divided by the number of Total_Votes is greater than or equal to 50% in order to analyze them in a "helpful review category."

![customerreview](https://user-images.githubusercontent.com/98790082/179382932-a8371414-eeb9-41a5-b271-4f9f723aab13.png)


![amazonreviews](https://user-images.githubusercontent.com/98790082/179382933-5b749a8e-0286-4c83-a248-ee87a7f699a3.png)

![vinereview](https://user-images.githubusercontent.com/98790082/179382942-4577c993-0c31-4b6f-98cf-cc237de8ec39.png)

## Summary

Approximately 36% of the vine reviews out of 613 are 5-star reviews whereas 47% are 5-star reviews for non-Vine customers. This shows that non-Vine customers are more like to give 5-star reviews than the Vine paid customers.

