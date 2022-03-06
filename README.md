# Amazon_Vine_Analysis
Amazon Product reviews to determine the bias in the Automotive Section


## Resources
- Amazon_reviews_ETL.ipynb
- Vine_reviews_ETL.ipynb
-https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Automotive_v1_00.tsv.gz
----------------------------------------------------------------------
- Python(Google Colab)
- Spark
- pgAdmin
- Postegresql
- Pyspark

## Overview of Project:
![image_name](images/results_id.png)

I used my knowledge of the cloud ETL process to create an AWS RDS database with tables in pgAdmin. Spark helped me create multiple dataframes, like the one above, to easily transform the data into a more friendly format. I then uploaded the transformed data into the appropriate tables and ran queries in pgAdmin to confirm that the data has been uploaded. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. We will then be splitting the data to show the different amount of reviews.


## Results:
![image_name](images/vine.png)

How many Vine reviews and non-Vine reviews were there?
- The total number of reviews were:
- Paid: 82
- Unpaid: 24742

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
- The total number of reviews were:
- Paid: 33
- Unpaid: 12807

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
- The total percent of 5 star reviews were:
- Paid: 0.4024390243902439 %
- Unpaid: 0.5176218575701237 %


## Summary:
The initial ETL process wasnt too hard as the data came in an easy to use format. After transferring the clean table to Postgresql, the vine data can be split to show the difference between the reviews. When looking at the first two results, there is a massive domination of unpaid reviews opposed to paid. This also translates to the 5 star reviews as well, with only 33 five stars. In the last section of the reviews, the percentage of 5 star show the bias towards unpaid reviews. This is hard to conclude as the there is very little data in the paid category compared to the unpaid category.
