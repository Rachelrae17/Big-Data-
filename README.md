Amazon_Vine_Analysis 
Module 16 


Overview: In this project I Chose US Apparel product reviews from Amazon. The goal was to analyze if it would be worth it to subscribe to a Vine program if we were to sell similar products through their platform. The vine review program is an incentive model in which customers are gifted free stuff when they write good reviews. I was able to use PySpark to extract, transform, and load (ETL) the data to a AWS RDS I created and connected to my PostgreSQL server to be able to query it and extract my finished tables from there. Part of the data transformation was made using pandas as well.

Results: The first step was to extract the dataset from an AWS S3 using PySpark in order to transform it and load it to AWS again. There, I basically divided the whole dataframe into 4 smaller dataframes for better analysis. These dataframes were then loaded to AWS RDS using a a connection from PySpark to PostgreSQL.

![Step 1](https://user-images.githubusercontent.com/95897182/164992087-bf32145a-1106-43d6-aeb9-576a8aa8bbcf.png)

![Step 2](https://user-images.githubusercontent.com/95897182/164992144-f058a9c9-2cb6-432b-a8c3-d30801ec9e48.png) 

![Step 3](https://user-images.githubusercontent.com/95897182/164992236-3177d06c-5ad0-48c7-92ef-ff1ae22a2c5f.png)

![Step 4](https://user-images.githubusercontent.com/95897182/164992325-ca9071dc-9f69-43c0-99e5-d382db8e5f4f.png)

<img width="745" alt="Query 1" src="https://user-images.githubusercontent.com/95897182/164993499-b79ca189-fb98-4f98-b4e9-27672e610d46.png">

<img width="743" alt="Query 2" src="https://user-images.githubusercontent.com/95897182/164993524-2ba02a37-7d10-4993-804a-e58bd311219c.png">

<img width="741" alt="Query 3" src="https://user-images.githubusercontent.com/95897182/164993580-9091c9b3-baf8-4e5f-ac41-931478d0d3b1.png">



















