# Spam_or_Non-Spam_Email_Classification_Analysis
## Introduction
### Context
With the proliferation of email communication, spam emails have become a significant problem, causing inconvenience and potential security risks for users. Efficiently filtering out spam emails is crucial for maintaining the integrity of email communication systems.

### Objective
My primary goal is to develop a machine learning model to classify emails as spam or non-spam.
Besides, I'm also curious about the features that contribute most to spam classification and evaluating different machine learning algorithms for their effectiveness in this task.
### Dataset
The project utilizes the Spambase dataset from the UCI Machine Learning Repository.\
Dataset Link: https://archive.ics.uci.edu/dataset/94/spambase    

#### Dataset Description 
Specifically, (i) file “spambase.data” contains the actual data, and (ii) files “spambase.names” and “spambase.DOCUMENTATION” contain the description of the data.
This dataset has 4601 records, each record representing a different email message. Each record is described
with 58 attributes (indicated in the aforementioned .names file): attributes 1-57 represent various content-
based characteristics already extracted from each email message (related to the frequency of certain words
or certain punctuation symbols in a message as well as to the usage of capital letters in a message), and the last attribute represents the class label for each message (spam or non-spam).

## Classification Model
For the classification task, I selected four machine learning models: K-Nearest Neighbors (KNN), Support Vector Machine (SVM), Logistic Regression, and XGBoost. Each model was subjected to hyperparameter tuning using Grid Search to identify the optimal parameters.
Besides,to ensure robust and unbiased performance evaluation, nested cross-validation (CV) was employed. 

Two different models for detecting spam messages were considered based on email characteristics and various criteria:\
**Model (i): Maximizing Predictive Accuracy**: This model is focused solely on maximizing overall predictive accuracy without considering any cost information.\
**Model (ii): Cost-Sensitive Classification**: This model is designed to minimize the average misclassification cost. (10:1 cost ratio for different misclassification errors)

## Conclusion
**Model (i): Maximizing Predictive Accuracy**: The XGBoost model shows a strong performance in spam email identification, achieving an accuracy of approximately 95.5%. This high accuracy indicates the model's effectiveness in correctly identifying both spam and non-spam emails, making it a reliable choice for general spam detection tasks.\
**Model (ii): Cost-Sensitive Classification**: The XGBoost model, with a total cost of 287 on the test set, exhibits the best performance in cost-sensitive classification. This demonstrates its superior ability to minimize the average misclassification cost, indicating its effectiveness in scenarios where the cost of false positives and false negatives needs to be carefully managed.

## Limitation
The project considered only four models (KNN, SVM, Logistic Regression, and XGBoost). While these models are popular and effective, there are many other machine learning algorithms that were not explored, such as Random Forest, Neural Networks, Gradient Boosting Machines other than XGBoost, and ensemble methods. The exclusion of these models means that there could be potentially better-performing models that were not identified.
