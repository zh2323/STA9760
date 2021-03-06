# STA9760
## Analyzing 10Gb of Yelp Reviews Data
This project is to uplad and perform analysis on Yelp's Reviews and Businesses dataset from Kaggle by provisioning a Spark Cluster on AWS EMR. 
Firt, I created a EMR Cluster and downloaded datasets from Kaggle. Then I uploaded datasets onto S3 Bucket.
Second, I loaded the datasets and performed a series of analysis in Jupyter Notebook with PySpark.

## Part I: Installation and Initial Setup
I installed and imported required packages (pandas, matplotlib and seaborn). Then I loaded my datsets (business,user and review) as pyspark datafrom.
## Part II: Analyzing Categories
I performed a general analysis of business dataset. Splitting each category of each business if a business has more categories. There are 1336 unique categories avaliable. And I also calculated the number of businesses of each category and ranked them. The top 5 categories are Restaurants, Shopping, Food, Home Services and Beauty & Spas. A barplot also shows direct ranking of top 20 categories. 
## Part III: Do Yelp Reviews Skew Negative?
In order to check if users who left written reviews are more pessimistic or more optimistic as compared to the overall business rating, I started from getting the average stars they rated for each business. And then I compared those reviewers' stars with actual business stars by calcuting the skew with the formula (row['avg(stars)'] - row['stars']) / row['stars']. Last I ploted a plot to see the general distribution of those skews and we can see that the skew is negative and then reviewers who left a written response are more dissatisfied and strict than the normal.
## Part IV: Should the Elite be Trusted?
There are elite users and normal users. In order to check if elite users are more pessimistic or more optimistic as compared to the overall business rating, I started from selecting elite users from the user dataset. Then join the elite_user with business to get the average stars they rated for each business. And then I compared those elite reviewers' stars with actual business stars by calcuting the skew with the formula (row['avg(stars)'] - row['stars']) / row['stars']. Last I ploted a plot to see the general distribution of those skews and we can see that the skew is a little positive and then elite reviewers are more satisfied than the normal.

## Cluster Configuration 
![cluster_configuration](https://user-images.githubusercontent.com/65482040/100181379-0f278900-2f15-11eb-955c-ca6c8775a147.png)


## Notebook Configuration
![notebook_configuration](https://user-images.githubusercontent.com/65482040/100183899-1d78a380-2f1b-11eb-9c4d-25ca4f162316.png)
