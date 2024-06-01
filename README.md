# Spam_Or_Non-Spam_Email_Classification_Analysis
## Introduction
### 1.1. Context
With the proliferation of email communication, spam emails have become a significant problem, causing inconvenience and potential security risks for users. Efficiently filtering out spam emails is crucial for maintaining the integrity of email communication systems.

### 1.2. Objective
My primary goal is to develop a machine learning model to classify emails as spam or non-spam.
Besides, I'm also curious about the features that contribute most to spam classification and evaluating different machine learning algorithms for their effectiveness in this task.
### 1.3. Dataset
The project utilizes the Spambase dataset from the UCI Machine Learning Repository.\
Dataset Link: https://archive.ics.uci.edu/dataset/94/spambase    \

#### Dataset Description 
Specifically, (i) file “spambase.data” contains the actual data, and (ii) files “spambase.names” and “spambase.DOCUMENTATION” contain the description of the data.
This dataset has 4601 records, each record representing a different email message. Each record is described
with 58 attributes (indicated in the aforementioned .names file): attributes 1-57 represent various content-
based characteristics already extracted from each email message (related to the frequency of certain words
or certain punctuation symbols in a message as well as to the usage of capital letters in a message), and the last attribute represents the class label for each message (spam or non-spam).

## Model Development
Based on email characteristics and various criteria, I created two different models for detecting spam messages:\
**Model(i)** The optimal model focused solely on maximizing overall predictive accuracy, without considering any cost information.\
**Model(ii)** The best cost-sensitive classification model, designed to minimize the average misclassification cost.

## Model Validation


## Conclusion
