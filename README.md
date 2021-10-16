# Amazon_Vine_Analysis
Analyze Amazon reviews with PySpark and Python (in Google Colab) to perform ETL with AWS RDS instance, and populating tables in Postgres.

## Overview:
Data obtained from Amazon's Vine program (a paid review program where Vine members are required to publish reviews for products) is analyzed for potential bias for the category: Personal Care Appliances. Using PySpark, the vine dataframe was filtered to show only reviews were there were more than 20 total votes, and further filtered to show only reviews that had 50%+ helpful votes (picking reviews that are more likely to be helpful).

## Results from the filtered Vine reviews DataFrame:
1. There were a total of three reviews from the Vine program, and 3094 reviews not from the Vine program.
### Total Reviews from Vine Program (paid):
![Vine_reviews_y](https://user-images.githubusercontent.com/74624855/137601868-d2bf4a50-afbe-4ab5-88f4-cd3bde4e1ce6.png)
### Total Reviews Not from Vine Program (not paid):
![Vine_reviews_n](https://user-images.githubusercontent.com/74624855/137601870-7a45cd3e-ccab-436a-8e81-446515575152.png)

2.There were two five-star reviews from the Vine program, and 1704 5-star reviews not from the Vine program.
### Total 5-Star Reviews from Vine Program (paid):
![Count_reviews_5star_y](https://user-images.githubusercontent.com/74624855/137601900-57131f78-7bdc-4df6-8ed2-25fdfdc35a82.png)
### Total 5-Star Reviews Not from Vine Program (not paid):
![Count_reviews_5star_n](https://user-images.githubusercontent.com/74624855/137601903-7aa2d7f0-db3d-4806-9cfc-2ff06cf8a98f.png)

3. There was 66.67% 5-star reviews from the Vine program, and 55.07% 5-star reviews not from the Vine program.
### Percentage of 5-Star Reviews from Vine Program (paid):
![Percent_5star_y](https://user-images.githubusercontent.com/74624855/137601951-59c0ce0c-b846-43b2-8603-c55294ae42a6.png)
### Percentage of 5-Star Reviews from Vine Program (not paid):
![Percent_5star_n](https://user-images.githubusercontent.com/74624855/137601952-e0cd5971-c673-4844-9149-27cd077e1498.png)


## Summary:





