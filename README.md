# Amazon_Vine_Analysis




## Overview of Project


This project’s objective is to analyse Amazon reviews written by members of the paid Amazon Vine program. 
The deliverables for this project are:


*	Perform ETL on Amazon Product.

* 	Determine Bias of Vine.		

							

## Software


PySpark, AWS, Google Colab and SQL. 



## Results 


### Perform ETL on Amazon Product. 


Using Google Colab and PySpark, a dataset from Amazon Review dataset was extracted as dataframe.



![image](https://user-images.githubusercontent.com/86136535/137652119-0c645dcb-50a2-42c4-bb30-5bb3ddf85e28.png)




The dataframe was divided in four datasets and uploaded in AWS RDS database. The new dataframes are customer, product, review and vine. 




![image](https://user-images.githubusercontent.com/86136535/137652148-15777485-fc6c-48b9-a79a-1b5e32584c6a.png)




The new dataframes were transferred from AWS RDS to pgAdmin.




![image](https://user-images.githubusercontent.com/86136535/137652169-3d4bc7bd-deb6-49e0-896c-f6b9a2c3ccd6.png)




![image](https://user-images.githubusercontent.com/86136535/137652182-c6622ab8-2b82-4652-951e-cf6d011f1a10.png)



### Determine Bias of Vine.




•	How many Vine reviews and non-Vine reviews were there?



![image](https://user-images.githubusercontent.com/86136535/137652207-b979ea57-ba08-4947-a9e2-c6a1611066eb.png)


•	How many Vine reviews and non-Vine reviews were there?



![image](https://user-images.githubusercontent.com/86136535/137652247-c467995f-c589-4bfb-8f2d-9178223303fb.png)


•	How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?




![image](https://user-images.githubusercontent.com/86136535/137652267-41b9f5d1-2bfc-462e-9ad0-75758bf4d969.png)


•	What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?




![image](https://user-images.githubusercontent.com/86136535/137652285-1012addb-0f06-4ed0-b8db-a92b7e3d9e66.png)


### Summary


In this analysis, any vine with less than 20 reviews were excluded from the total count.  The analysis shows that there is no bias in the Amazon vine reviews as the numbers of paid reviews is significantly smaller than the unpaid reviews. 



