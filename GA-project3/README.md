# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

### Problem Statement

### A new company which aims to develop both mobile games and board games had approached me to help them in building a classification model to correctly classify the 2 categories. This project aims to make use of the posts by the users in the 2 subbreddit groups namely 'boardgames' and 'MobileGaming' for the modeling of this classification model.


### Executive Summary

Web-scraping using the reddit API gathers the data needed for training and testing of the classification models. Data cleaning need to be done on the data being pull from the API as some of the posts are either removed, deleted, empty or posted by the moderator.

14 models have been built for classification purpose. As our aim is to correctly classify the 2 groups, hence specificity and sensitivty are also important metrics in addition to accuracy. As the Extra Tree classifier with TfidfVectorizer achieve the highest accuracy of 87.1% as well as sensitivity and specificity of 85.8% and 88.5% respectively, this model will be chosen for the model to be used to classify between MobileGaming and Boardgames.

Below is the table that summarize the performance of all the 14 models.

| Model | Vectorizer | Accuracy | Sensitivity | Specificity | Precision | F1_score |
| --- | --- | --- | --- | --- | --- | --- |
| Logistic Regression | cvec | 0.849 | 0.151 | 0.814 | 0.885 | 0.874 | 0.842 |
| Logistic Regression | tvec | 0.857 | 0.143 | 0.852 | 0.861 | 0.857 | 0.855 |
| MultinomialNB | cvec | 0.857 | 0.143 | 0.897 | 0.818 | 0.828 | 0.861 |
| MultinomialNB | tvec | 0.84 | 0.16 | 0.882 | 0.799 | 0.811 | 0.845 |
| KNeighborsClassifier | cvec | 0.68 | 0.32 | 0.49 | 0.866 | 0.781 | 0.602 |
| KNeighborsClassifier | tvec | 0.765 | 0.235 | 0.598 | 0.928 | 0.8901 | 0.716 |
| DecisionTreeClassifier | cvec | 0.782 | 0.217 | 0.725 | 0.837 | 0.813 | 0.767 |
| DecisionTreeClassifier | tvec | 0.731 | 0.269 | 0.745 | 0.7178 | 0.72 | 0.733 |
| BaggingClassifier | cvec | 0.799 | 0.201 | 0.779 | 0.818 | 0.807 | 0.793 |
| BaggingClassifier | tvec | 0.825 | 0.174 | 0.77 | 0.88 | 0.863 | 0.813 |
| RandomForestClassifier | cvec | 0.855 | 0.145 | 0.828 | 0.88 | 0.871 | 0.849 |
| RandomForestClassifier | tvec | 0.862 | 0.138 | 0.833 | 0.89 | 0.881 | 0.856 |
| ExtraTreesClassifier | cvec | 0.831 | 0.169 | 0.848 | 0.813 | 0.816 | 0.832 |
| ExtraTreesClassifier | tvec | 0.872 | 0.128 | 0.858 | 0.885 | 0.879 | 0.868 |

### Data Dictionary

| Feature  | Data Type | Dataset | Description |
| --- | --- | --- | --- |
| subreddit_cat | Integer | Train/Test | Subreddit category, 1 for boardgames, 2 for MobileGaming|
| processed_text_lem | Object | Train/Test | Lemmatized Text |

