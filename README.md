# Big-Data-ETL
In this assignment I managed to test my ETL skills with some data that i found on the Amazon website.
I had reviews on software and home entertainemnt.

DATA SOURCE:
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Software_v1_00.tsv.gz
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Home_Entertainment_v1_00.tsv.gz

I managed to complete the ETL process in the cloud and upload a DtaFrame to an RDS instance. I used PySpark  and SQL to perform statistical analysis of the data.

PROCESS

EXTRACT
I read each dataset using PySpark and got the number of rows in each dataset.


TRANSFORM
I created four DataFrames namely:review_id, products_df, customer_id and vine
_df.
I created the review_id df wuth the appropriate columns and data types.
I dropped the duplicates in the products_df. 
I created customers_df DataFrame that groups the data on the customerId by the number of times a customer reviewed a product.
I created the vine_df that has the review_id, star_rating, helpful_votes, and vine clolumns.


Load 
When I had finshed the extraction and transformation I then exported each DataFrame into the RDS instance to create four tables for each dataset.

