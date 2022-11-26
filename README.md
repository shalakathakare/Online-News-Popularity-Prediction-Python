# OnlineNewsPopularityPrediction

## Overview
Mashable is a digital media platform for news articles and entertainment. Like most such platforms, it is reliant on advertising revenue. This is done by attracting visitors and convincing advertisers that the buying space on the article is worthwhile. The more popular the article/blog is, the more advertisers will want to get involved and the more they’ll be willing to pay.  
In this project, we have explored and analyzed data for Mashable articles to develop classification models and predict the popularity of articles. This can help Mashable increase profits from advertisements by determining the article popularity before publication and setting a framework to sells ads accordingly.

## Project Objective:
Predict the popularity of articles prior to publication by implementing machine learning models to attract advertisers to buy ad space
Evaluate best model and perform cost-benefit analysis to determine the model which can generate maximum revenue from advertising

## Data
Features-61
Instances- 39,000
Target variable – shares 
We have used number of article shares as our target variable to determine popularity of articles. 
 
## Exploratory Data Analysis
•	Performed univariate and multivariate analysis to understand individual variable distribution and statistics
•	Converted the problem into a classification problem based on target variable where
-	Articles with Shares >1500 are Popular
-	Articles with Share > 1500 are Unpopular
•	Performed correlation analysis using heatmap to understand variable relationships and detect highly correlated columns
 

## Observations from EDA:
•	Articles with decent number of words have more number of shares than those with that are too long because they are too long to read

 

•	The number of shares is higher for channels like technology, entertainment and world news as compared to others.
 
•	The proportion of popular articles is higher on weekends than on weekdays
## Feature Engineering/Selection:
•	Removed features that are not helpful for prediction – url, timedelta
•	Removed highly correlated features – n_non_stop_unique_tokens, n_non_stop_words, kw_avg_min
•	Performed box cox transformation to handle outliers and correct skewness for features
•	Implemented capping to minimize data loss while removing outliers

## Models and Evaluation:
•	Naïve Bayes
•	Logistic Regression
•	KNN
•	Random Forest
Evaluation metrics: Accuracy. F1-Score, AUC, ROC 
Since Random Forest model had highest accuracy, we performed hyper-parameter tuning to increase performance.
## Cost-Based Analysis
A cost-benefit analysis was performed to determine the best model and prevent costly misclassifications. We have assigned costs to the following metrics for wrongly and correctly predicting the classification problem:
•	True Positive
•	False Positive
•	True Negative
•	False Negative
