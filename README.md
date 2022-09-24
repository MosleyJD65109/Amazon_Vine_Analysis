# Amazon_Vine_Analysis

## Overview
In this project, we have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products.  We picked Gift Cards datasets. 
We used PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. And then used PySpark again to determine if there is any bias toward favorable reviews from Vine members in our dataset. 


## Results


* **The customers_table DataFrame** :  
<p align="left">
  
![Customer_Table_DF](https://user-images.githubusercontent.com/104540261/192103839-952fd680-e501-4ac8-b13e-efb25b5633b3.png)
  
</p>

* **The products_table DataFrame** :  
<p align="left">
  
![Products_Table_DF](https://user-images.githubusercontent.com/104540261/192103864-604dcb01-852d-4242-aaa6-90d240ad6933.png)
  
</p>

* **The review_id_table DataFrame** :  
<p align="left">
  
![review_id_table_DF](https://user-images.githubusercontent.com/104540261/192103894-cf7d3f11-1de6-4014-b845-b2f52c3498cf.png)
  
</p>

* **The vine_table DataFrame** :  
<p align="left">
  
![vine_table_DF](https://user-images.githubusercontent.com/104540261/192103930-64c76321-3bf8-4510-ba52-b91f04fffc75.png)
  
</p>





-----------------------------------------------------------------------------

* There are 149086 total reivews
* There are 129709 5-star reviews


-----------------------------------------------------------------------------
* There are total 0 vine (vine = Y) reviews
* There are 0,Five-star vine (vine = Y) reviews
* There are 0.0 % 5-star vine (vine = Y) reviews


-----------------------------------------------------------------------------
* There are total 149086 non-vine (vine = N) reviews
* There are 129709 5-star non-vine (vine = N) reviews
* There are 87.0 % 5-star non-vine (vine = N) reviews


-----------------------------------------------------------------------------
## Results

### State if there is any positivity bias for reviews in the Vine program
There are zero paid 5 start reviews. Our dataset is for gift cards and it seems like companies don't pay for gift card reviews. It's hard to detremine bias as there is not enough data to conclude paid reviews. Unpaid reviews has 87% positive reviews. So even unpaid reviews are also very positive.

We could perform the similar analysis for next best rating - (rating 4) and see if there is any bias. 

NOTE : it's very strange situation where there is no paid reviews which makes it harder to do any meaningful compariosn between paid vs unpiad. 
