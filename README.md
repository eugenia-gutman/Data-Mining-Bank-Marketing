# **DATA MINING FOR BANK DIRECT MARKETING**


## EXECUTIVE SUMMARY


**Project overview and goals**

Portugese banks are experiencing increasing competitive and economic pressures to sell
Advanced Deposit investment product to their customers. The increase in number of telemarketing campaigns seems to reduce the effect of those promotions. The goal of this data mining project is to improve potential customer targeting to make the campaigns more efficient.

\
**Findings**

The best machine learning model for improving telemarketing campaings efficiency is Logistic Regression with manual feature engineering and selection. The model has 89.7% test accuracy score, 67% recall. Model selection was based on the highest accuracy score.

\
**Recommendations**

Apply Logistic Regression model with a threshold of 75% to improve campaign conversion from 11% to 14%. This approach will result in obtaining 90% of Advanced Deposit sales by contacting targeted 75% of customers that would have had to be contacted without the targeting.

\
![lift_curve.png](https://github.com/eugenia-gutman/Data-Mining-Bank-Marketing/blob/main/images/lift_curve.png)

\
Most powerful predictors of the sales phone call outcome are:


*   **Economic conditions.** During the times of low Employment Variation Rate and high Consumer Price Index customers are more likely to purchase Advanced Deposit
*   **Previous calls results.** Customers who previously declined Advance Deposit are more likely to decline it in the future
*   **Month when call is made.** Most successes are achived in March, August and December



\
*

# METHODOLOGY

\
**Data**

The dataset comes from the UCI Machine Learning repository [link](https://archive.ics.uci.edu/ml/datasets/bank+marketing). The data is from a Portuguese banking institution and is a collection of the results of multiple marketing campaigns.

\
**Machine Learning Models**


The analysis follows a **classification modeling approach** to predict whether a bank customer will subscribe to a term deposit. After cleaning the data, removing the post-call duration variable to avoid data leakage, encoding categorical variables, and splitting the data into training and test sets, three baseline models were compared: **K-Nearest Neighbors (KNN), linear Support Vector Machine (SVM), and Logistic Regression**.

Logistic Regression model was enhanced through feature scaling, removal of redundant/correlated variables, polynomial features and interactions, L1 regularization for feature selection, and statistical significance testing. The final model achieved approximately 89.7% test accuracy, 66% positive precision, and 21.6% positive recall.

\
**Classification Models Comparison**
| Model | Train Time | Train Accuracy | Test Accuracy |
| ----- | ---------- | -------------  | -----------   |
|  Base Model (KNN)   |  4 sec  |0.912434     |0.887357     |
|  Simple Model (SVM)   |  3 min  |0.873822     |0.872103     |
|  Logistic Regression   |  2 min  |0.900554     |0.897331     |


\
**Python Code**


[CRISP_DM_bank_marketing.ipynb](CRISP_DM_bank_marketing.ipynb)






---


