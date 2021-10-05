### Overview 
The purpose of this project was to perform the ETL process on a chosen dataset of Amazon reviews which were written by either non-vine reviewers or vine reviewers (Vine reviewers are paid reviewers here), then connect to an AWS RDS instance and load the data into pgAdmin. After this, PySpark was used to determine if there was any bias toward favorable reviews from Vine members.

### Results 
In the Amazon_Review_ETL.ipynb file, an AWS RDS database was created with tables in pgAdmin. The selected dataset was then loaded into a Spark dataframe and four different dataframes were created to match the tables in the SQL database in order to load the data into the respectable tables. 

in the Vine_Review_Analysis.ipnyb file, the vine table created in the Amazon_Review_ETL.ipynb file was filtered multiple times to only show reviews that had 20 or more votes, and where the helpful votes accounted for 50% of the total votes. 

The following are findings about the vine and non-vine reviews:
- of the total 16,695 reviews in the dataset, 231 reviews were from Vine memebers and 16,464 were from non-Vine members 
- 93 Vine members gave 5-star reviews, and 4,867 non-Vine members gave 5-star reviews
- 5-star reviews account for 40% of the Vine reviews, and 30% of the non-Vine reviews 

### Summary 
Based on the findings above, there does not seem to be much bias in the overall reviews of this dataset. Another possible analysis that could be done to prove this would be to redo the above analyses for each star review to see if there is bias there. 
