# Overview
This project analyzes Amazon reviews that have been written by members of the paid, 'Amazon Vine' program. Amazon Vine is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
\
The project examines a dataset of groceries, and uses PySpark to perform the ETL process. It extracts the dataset, transforms the data, connects to an AWS RDS instance, and loads the transformed data into pgAdmin. Next, the evaluation employs PySpark to determine if there is any bias that's affecting the favorable reviews.
\
\
The project only looks at products with verified purchases. Filters retrieve all the rows where:
\
-the count of total votes is equal to or greater than 20. This serves to pick 'helpful reviews' and division by zero errors later on.
\
-the number of 'helpful reviews' divided by the count of total votes, and the number of these results that is equal to or greater than 50%.
\
-the count of reviews, written as part of the Vine program.
\
-the count of reviews, NOT written as part of the Vine program.
\
-the number and percentage of 5 star reviews.
# Results



Determine the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for the two types of review (paid vs unpaid).
# Summary
