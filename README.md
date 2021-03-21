# Overview
This project analyzes Amazon reviews that have been written by members of the paid, 'Amazon Vine' program. Amazon Vine is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
\
\
The project examines a dataset of groceries, and uses PySpark to perform the ETL process. It extracts the dataset, transforms the data, connects to an AWS RDS instance, and loads the transformed data into pgAdmin. Next, the evaluation employs PySpark to determine if there is any bias that's affecting the favorable reviews.
\
\
The project only looks at products with verified purchases. Filters retrieve all the rows where:
\
-the count of total votes is equal to or greater than 20. This serves to pick 'helpful reviews.'
\
-the number of 'helpful reviews' divided by the count of total votes, and the number of these results that is equal to or greater than 50%.
\
-the count of reviews, written as part of the Vine program.
\
-the count of reviews, NOT written as part of the Vine program.
\
-the number and percentage of 5 star reviews.
# Results
18,592 reviews had more than 20 votes. They retain the label "helpful votes".
17,340 reviews were considered 'helpful reviews' and constituted at least 50% of all votes.
Only 1 'helpful review' constituted a Vine review. 
17339 'helpful reviews' were NOT Vine reviews. 
This means nearly 100% of the 'helpful reviews' were unpaid and unbiased. 
9,866 'helpful reviews' gave the grocery item five stars. 
This represents about 56% of the total 'helpful reviews.'


# Summary
The results indicate that grocery product reviews appear unbiased by the Vine program. With only 1/2 products receiving 5 stars, the grocery-line also appears to need improvement.
\
\
**Appendix**
\
Analysis to determine reviews with 20 votes or more. Labeled "helpful reviews".
\
\
!["20%2BVotesPerReview.PNG"](https://github.com/dagibbins186/Amazon_Vine_Analysis/blob/main/Amazon_Vine_Analysis/Images/20%2BVotesPerReview.PNG)
\
\
Analysis to determine reviews with 50% or more "helpful reviews".
!["VotesGreaterThan50%25.PNG"](https://github.com/dagibbins186/Amazon_Vine_Analysis/blob/main/Amazon_Vine_Analysis/Images/VotesGreaterThan50%25.PNG)
\
\
Analysis to show Vine reviews
!["VineReview.PNG"](https://github.com/dagibbins186/Amazon_Vine_Analysis/blob/main/Amazon_Vine_Analysis/Images/VineReview.PNG)
\
\
Analysis to show NON-Vine reviews
\
\
!["NotVineReview.PNG"](https://github.com/dagibbins186/Amazon_Vine_Analysis/blob/main/Amazon_Vine_Analysis/Images/NotVineReview.PNG)
\
\
Analysis to show 5 star ratings
\
\
!["5StarReviews.PNG"](https://github.com/dagibbins186/Amazon_Vine_Analysis/blob/main/Amazon_Vine_Analysis/Images/5StarReviews.PNG)
