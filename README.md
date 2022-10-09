# Amazon_Vine_Analysis
## purose:
### The purpose of this challenge  is to analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.In this project, we have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. we need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. We are useing PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. 
### Using our knowledge of the cloud ETL process, we are createing an AWS RDS database with tables in pgAdmin, pick a dataset from the Amazon Review datasetsLinks to an external site (I am using Electronics_v1_00), and extract the dataset into a DataFrame. we are transforming the DataFrame into four separate DataFrames that match the table schema in pgAdmin. Then, we are upload the transformed data into the appropriate tables and run queries in pgAdmin to confirm that the data has been uploaded.
## Results:
### There were over three million reviews recorded in the dataset. The dataset was filtered down to count of total votes equal or greater than 20 and percent of helpful votes to total votes equal or greater than 50%. Reducing the number of total reviews to just over 50K
Percent_votes_df Image
### How many Vine reviews and non-Vine reviews were there : The Vine program members account for 1,080 or 2.1% of the reviews and non-Vine program members make up 49,659 or 97.9% of reviews. 
### How many Vine reviews were 5 stars : The Vine program members had 454 of the total five-star reviews out of 1,080.
### How many non-Vine reviews  were 5 stars : The Non-Vine program members had 23,034 of the total five-star reviews out of 49,659.
### What percentage of Vine reviews were 5 stars : The Vine program members accounted for 42% of the reviews were rated five stars.
### What percentage of non-Vine reviews were 5 stars : The Non-Vine program members were just over 46% of the rated five-star reviews.
Ratings_total_df Image
Paid_df Image
Non_paid_df Image
## Summary: 
### The analysis indicate that Vine program members did not show bias when rating products and might be more precarious in the review process. Since the number of five-star reviews for Vine program members (42%)  was almost 10% less  compared to non-Vine program members .In addition, running the same analysis using datasets from different product categories can provide us with the whole picture of whether reviews made by Vine members are bias.Vine members did not show bias when rating their products considering that the number of 5-star ratings was about 10% less than Non-Vine members (42% vs. 46.4%). With this, we can assume that Vine customers are more critical when submitting their review. However, in order to support this assumption further, we should include all of the data rather than filtering it to a percentage of helpful vs. total votes as we did for this analysis,
