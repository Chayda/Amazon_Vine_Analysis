# Amazon_Vine_Analysis
Analyze Amazon reviews with PySpark and Python (in Google Colab) to perform ETL with AWS RDS instance, and populating tables in Postgres.

## Overview:
Data obtained from Amazon's Vine program (a paid review program where Vine members are required to publish reviews for products) is analyzed for potential bias for the category: Personal Care Appliances. Using PySpark, the vine dataframe was filtered to show only reviews were there were more than 20 total votes, and further filtered to show only reviews that had 50%+ helpful votes (picking reviews that are more likely to be helpful).

### Reviews from Vine Program:
![Vine_reviews_y](https://user-images.githubusercontent.com/74624855/137602009-f1a73702-5057-43c3-9442-fdb1fb8c81f8.png)
### Reviews Not from Vine Program:
![Vine_reviews_n](https://user-images.githubusercontent.com/74624855/137602012-bd604416-0a9f-427c-9b98-a227035dc19f.png)


## Results from the filtered Vine reviews DataFrame:
#### 1. There were a total of three reviews from the Vine program, and 3094 reviews not from the Vine program.
### Total Reviews from Vine Program (paid):
![Count_reviews_y](https://user-images.githubusercontent.com/74624855/137602028-84e79688-c970-49e5-8331-11d1c5e368f3.png)
### Total Reviews Not from Vine Program (not paid):
![Count_reviews_n](https://user-images.githubusercontent.com/74624855/137602030-541fb27e-4c60-459f-a1f6-387d05b42941.png)

#### 2.There were two five-star reviews from the Vine program, and 1704 5-star reviews not from the Vine program.
### Total 5-Star Reviews from Vine Program (paid):
![Count_reviews_5star_y](https://user-images.githubusercontent.com/74624855/137601900-57131f78-7bdc-4df6-8ed2-25fdfdc35a82.png)
### Total 5-Star Reviews Not from Vine Program (not paid):
![Count_reviews_5star_n](https://user-images.githubusercontent.com/74624855/137601903-7aa2d7f0-db3d-4806-9cfc-2ff06cf8a98f.png)

#### 3. There was 66.67% 5-star reviews from the Vine program, and 55.07% 5-star reviews not from the Vine program.
### Percentage of 5-Star Reviews from Vine Program (paid):
![Percent_5star_y](https://user-images.githubusercontent.com/74624855/137601951-59c0ce0c-b846-43b2-8603-c55294ae42a6.png)
### Percentage of 5-Star Reviews from Vine Program (not paid):
![Percent_5star_n](https://user-images.githubusercontent.com/74624855/137601952-e0cd5971-c673-4844-9149-27cd077e1498.png)


## Summary:
If strictly taking into account only the results from this analysis of the percentage of 5-star reviews between the paid (Vine program) and not paid reviews, it would look as though there is a bias in the Vine program. The percentage of 5-star reviews from the Vine program-reviewed data was 66.67%, and the percentage for the not-Vine-reviewed data was 55.07%. This difference would indicate a bias exists; however, it's difficult to determine the validity of the bias of the Vine program from this analysis, as there wasn't a large enough sample of reviews from the Vine program (there were only three, compared with 1704 reviews not from the Vine program).

We could run additional analysis, which is strongly recommended, and find out how many Vine program reviews there are in the entire dataset (with no filters applied for number of "helpful" votes). This can be run to compare the total numbers for the Vine program and not-Vine program reviews. This can be done easily by reusing the code that was run for the above analysis, and instituting the names of dataframes containg the entire set of reviews. Running this as a quick test, the Vine program resulted in 75% 5-star reviews, while the non-Vine program resulted in 56.86%, which is close to the first analysis of the filtered reviews. The not-paid group remained stable and the bias increased with the larger dataset.




