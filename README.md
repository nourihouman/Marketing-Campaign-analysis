Marketing Campaign Analytics Project
Overview
This project involves comprehensive data analysis to understand customer behavior, segment customers, and optimize marketing strategies. The analysis includes data cleaning, exploratory data analysis (EDA), feature extraction, customer segmentation, market basket analysis, customer journey analysis, churn analysis, lifetime value prediction, and campaign effectiveness analysis using various data science techniques.

Table of Contents
Overview
Data Description
Data Cleaning and Preprocessing
Exploratory Data Analysis (EDA)
Feature Engineering
Analysis and Insights
Factors Influencing Store Purchases
Gold Spending and Store Purchases
Customer Segmentation
Market Basket Analysis
Customer Journey Analysis
Churn Analysis
Lifetime Value Prediction
Campaign Effectiveness
Average Customer Profile
Best-Performing Products
Differences in Customer Characteristics and Purchase Behaviors
Models and Methods
Results
Conclusions
Getting Started
Prerequisites

Data Description
The dataset used in this project includes various attributes related to customer demographics, purchasing behavior, and marketing campaign responses. The key columns include:

CustomerID: Unique identifier for each customer
Income: Customer's income
Kidhome: Number of children at home
Teenhome: Number of teenagers at home
Recency: Number of days since the last purchase
MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntGoldProds: Amount spent on various product categories
AcceptedCmp1, AcceptedCmp2, AcceptedCmp3, AcceptedCmp4, AcceptedCmp5: Response to marketing campaigns
First_Contact, Purchase_Date: Synthetic dates representing customer interactions and purchases
Data Cleaning and Preprocessing
Identified and addressed issues:

Removed leading spaces in column names.
Converted income column to numerical format and handled missing values.
Converted date columns to appropriate datetime format.
Handled missing values:

Imputed missing values in the income column.
Exploratory Data Analysis (EDA)
Visualized distributions of key variables.
Identified outliers and potential anomalies.
Analyzed correlations between variables using heatmaps.
Feature Engineering
Created new features to enhance analysis:
Join_month: Month the customer joined.
Join_weekday: Day of the week the customer joined.
Minorhome: Total number of minors in the family.
Total_Mnt: Total amount spent in the last two years.
Total_num_purchase: Total number of purchases in the last two years.
Total_accept: Total acceptances of marketing offers.
AOV (Average Order Value): Average order value of each customer.
Analysis and Insights
Factors Influencing Store Purchases
Using a linear regression model and feature importance from a random forest model, we identified the following significant factors related to the number of store purchases:

Total_num_purchase: Strongly positively correlated.
MntRegularProds: Significant positive impact.
NumCatalogPurchases: Positive relationship.
Gold Spending and Store Purchases
Performed a t-test to validate the claim that people who spent an above-average amount on gold in the last 2 years have more in-store purchases. The t-test results indicated a significant difference in the number of store purchases between those who spent above-average on gold and those who did not, supporting the claim.

Customer Segmentation
Using K-means clustering, we identified three main customer segments:

Low Income: Basic education, typically one kid.
Average Income: Often has one teenager.
High Income: Higher spending on wine, more responsive to campaigns.
Market Basket Analysis
Using the Apriori algorithm, we discovered strong associations between product categories:

Wines and Meat Products: Frequently bought together.
Meat Products and Fruits: Common combination.
Customer Journey Analysis
Analyzed the time taken for customers to make a purchase after their first contact, revealing insights into customer decision-making timelines and identifying critical decision periods.

Churn Analysis
Applied logistic regression to predict customer churn. The model was evaluated and improved using under-sampling to balance the dataset. Key findings:

Accuracy: 87.07%
Precision: 79.37%
Recall: 96.15%
F1 Score: 86.96%
Lifetime Value Prediction
Predicted customer lifetime value (LTV) using regression techniques, focusing on historical purchase data to identify high-value segments.

Campaign Effectiveness
Identified the most successful marketing campaign based on acceptance rates. Campaign 4 was found to be the most effective with a 7.44% acceptance rate.

Average Customer Profile
The average customer profile includes:

Income: $51,590
Number of Kids: 0.44
Number of Teenagers: 0.51
Recency: 49 days
Total Amount Spent on Wines: $305
Total Amount Spent on Meat Products: $165
Total Spending (Overall): $604
Best-Performing Products
Identified the best-performing products based on total spending:

Wines: $672,795
Meat Products: $362,826
Gold Products: $96,717
Fish Products: $82,879
Sweet Products: $59,453
Fruits: $57,897
Differences in Customer Characteristics and Purchase Behaviors
Investigated differences between customers who accepted the most successful campaign (Campaign 4) and those who did not. Key differences:

Income: Higher for those who accepted.
Total Spending: Significantly higher for those who accepted.
Campaign Responsiveness: Higher for those who accepted.
Models and Methods
Data Cleaning: Handled missing values, corrected data types, and addressed outliers.
EDA: Visualized data distributions, correlations, and outliers.
Feature Engineering: Created new features to improve model performance.
Clustering: K-means clustering for customer segmentation.
Association Rule Mining: Apriori algorithm for market basket analysis.
Regression Analysis: Linear regression and logistic regression for predicting store purchases and churn.
Lifetime Value Prediction: Regression techniques to predict customer LTV.
Campaign Effectiveness: Analyzed campaign responses to identify the most effective campaigns.
Results
Segmentation: Identified three main customer segments with distinct characteristics.
Market Basket Analysis: Discovered actionable product associations.
Customer Journey: Identified average time to purchase, highlighting critical decision periods.
Churn Prediction: Achieved high accuracy and recall with a balanced dataset.
LTV Prediction: Identified high-value customer segments.
Campaign Effectiveness: Determined Campaign 4 as the most effective.
Customer Profile: Developed a detailed profile of the average customer.
Best-Performing Products: Identified top-selling product categories.
Conclusions
This analysis provides a detailed understanding of customer behavior, allowing for targeted marketing strategies. The insights gained can improve campaign effectiveness, product recommendations, and customer retention efforts.
Getting Started
Prerequisites
Python 3.6+
Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn, mlxtend, networkx
