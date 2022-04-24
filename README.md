Amazon_Vine_Analysis 
Module 16 


Overview:
In this project I Chose US Apparel product reviews from Amazon. The goal was to analyze if it would be worth it to subscribe to a Vine program if we were to sell similar products through their platform. The vine review program is an incentive model in which customers are gifted free stuff when they write good reviews. I was able to use PySpark to extract, transform, and load (ETL) the data to a AWS RDS I created and connected to my PostgreSQL server to be able to query it and extract my finished tables from there. Part of the data transformation was made using pandas as well.

Results: 
The first step was to extract the dataset from an AWS S3 using PySpark in order to transform it and load it to AWS again. There, I basically divided the whole dataframe into 4 smaller dataframes for better analysis. These dataframes were then loaded to AWS RDS using a a connection from PySpark to PostgreSQL.

![Step 1](https://user-images.githubusercontent.com/95897182/164992087-bf32145a-1106-43d6-aeb9-576a8aa8bbcf.png)

![Step 2](https://user-images.githubusercontent.com/95897182/164992144-f058a9c9-2cb6-432b-a8c3-d30801ec9e48.png) 

![Step 3](https://user-images.githubusercontent.com/95897182/164992236-3177d06c-5ad0-48c7-92ef-ff1ae22a2c5f.png)

![Step 4](https://user-images.githubusercontent.com/95897182/164992325-ca9071dc-9f69-43c0-99e5-d382db8e5f4f.png)

<img width="745" alt="Query 1" src="https://user-images.githubusercontent.com/95897182/164993499-b79ca189-fb98-4f98-b4e9-27672e610d46.png">

<img width="743" alt="Query 2" src="https://user-images.githubusercontent.com/95897182/164993524-2ba02a37-7d10-4993-804a-e58bd311219c.png">

<img width="741" alt="Query 3" src="https://user-images.githubusercontent.com/95897182/164993580-9091c9b3-baf8-4e5f-ac41-931478d0d3b1.png">

And lastly, I worked with the last table called vine_table to perform the Vine program analysis to filter the best reviews, and see if there were significantly more 5-star reviews in the paid and incentivized (vine) program. The best reviews were those that were highly voted as helpful. Then, I filtered to see which of those were part of the vine program and which were not.

Unpaid Reviews 
* 45,388 total Reviews 
* 23,733 5- star Reviews 
* 52.3% of unpaid Reviews were 5- Star 

Paid Vine Program 
* 33 total Reviews 
* 15 5-Star Reviews 
* 45.5% of Vine Reviews were 5- Star 


Summary: 

For This analysis, the vine program might just not be worth it for the apparel category. As it can be seen, there were not many helpful reviews that made part of it (total of 33), and only around half of them were 5-star rated (45%). Very similarly to the unpaid reviews which also only half of them were 5 star rated (52%). Even though the percentages may be misleading as the volume of reviews in the vine and non-vine programs vary so much, this itself is a sign that the vine program is not very popular in this category. We might not want to pay for it as it is not incentivizing the people to write better reviews.This allows us to conclude that customers don't feel a positivity bias for leaving good reviews in the paid program as there are so few and not so many well-rated. Nevertheless, if we were to further analyze we could calculate the mean of the star ratings on each programs' reviews to see if there's a significant incentive.




















