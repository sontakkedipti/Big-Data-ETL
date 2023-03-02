# Big-Data-ETL
AWS Big Data ETL Project


In this assignment, many of Amazon's shoppers depend on product reviews to make a purchase. Amazon makes these datasets publicly available. They are quite large and can exceed the capacity of local machines. One dataset alone contains over 1.5 million rows; with over 40 datasets, data analysis can be very demanding on the average local computer. Your first goal will be to perform the ETL process completely in the cloud and upload a DataFrame to an RDS instance. The second goal will be to use PySpark or SQL to perform a statistical analysis of selected data.<br>

Link :  https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt

Extract two Amazon customer review datasets, transform each dataset into four DataFrames, and load the DataFrames into an RDS instance.<br><br>
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Toys_v1_00.tsv.gz <br>
https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Home_Improvement_v1_00.tsv.gz

Extract two Amazon customer review datasets and use either SQL or PySpark to analyze whether reviews from Amazon's Vine program are trustworthy.<br>
<br>![UsingPySPark](https://user-images.githubusercontent.com/112952607/222461152-bd761420-760f-4576-a0ea-40215efbf2b6.png)


Instructions

Upload the part_one_starter_code.ipynb into Google Colab and create a duplicate of this file.<br><br>
![UsingPySPark](https://user-images.githubusercontent.com/112952607/222461207-70b98ac6-bcbe-4637-b77e-428ab5eceacb.png)

Explore the Amazon ReviewsLinks to an external site. datasets and pick two datasets to perform ETL.<br><br>
Rename each part_one_starter_code.ipynb file according to the dataset you are using. For example, if you are going to use the Video Game reviewsLinks to an external site.<br> file, rename file, part_one_video_games.ipynb. Repeat the process for the duplicate file you created in Step 2.
Extract the Data<br><br>
Read in each dataset using the correct header and sep parameters.<br>
Get the number of rows in the dataset.<br><br>
![image](https://user-images.githubusercontent.com/112952607/222461541-9d4f4fcc-d318-461d-b6c5-15fce5483554.png)

Transform the Data<br>
For each dataset use the schema.sql file located in the Resources folder of the Starter_Code.zip file to create the four DataFrames as follows:<br>
Create the "review_id_df" DataFrame with the appropriate columns and data types.<br>
Create the "products_df" DataFrame that drops the duplicates in the "product_id" and "product_title columns.<br>
Create the "customers_df" DataFrame that groups the data on the "customer_id" by the number of times a customer reviewed a product.<br>
Create the "vine_df" DataFrame that has the "review_id", "star_rating", "helpful_votes", "total_votes", and "vine" columns.<br><br>

![image](https://user-images.githubusercontent.com/112952607/222462007-2e2f5577-4d3c-470e-a752-f16b14c00de2.png)

Load the Data into an RDS Instance<br><br>
Export each DataFrame into the RDS instance to create four tables for each dataset.<br><br>

![RDS_Database_table](https://user-images.githubusercontent.com/112952607/222462081-9d43d9e8-d18a-4a3b-b671-8e5d766d2379.png)
![Schema_Created_afterPGAdmin_Setup](https://user-images.githubusercontent.com/112952607/222462129-c1b15536-ac4d-4a79-a168-3fca4c169bd9.png)
![Review_Id_Table](https://user-images.githubusercontent.com/112952607/222462162-27c6c1c1-dfc5-4322-bbc2-27f8a3fdd1a0.png)
![vine_df](https://user-images.githubusercontent.com/112952607/222462188-185931fb-25ff-461e-bdb1-86712e064408.png)
![Product_table](https://user-images.githubusercontent.com/112952607/222462218-4af90234-6c59-4649-89d9-3ba57cc75274.png)
![Customer_Table](https://user-images.githubusercontent.com/112952607/222462236-263fee0c-f856-4b10-85d3-fafaa0dd7180.png)
