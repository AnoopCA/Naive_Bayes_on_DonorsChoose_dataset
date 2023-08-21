Predicting Project Funding on the DonorsChoose Dataset using Naive Bayes:
This repository contains code for predicting whether a project on the DonorsChoose platform will be successfully funded or not using a Naive Bayes classifier. The DonorsChoose dataset provides information about educational projects and their funding outcomes.

Introduction:
DonorsChoose is a crowdfunding platform connecting teachers seeking educational resources with potential donors. The dataset comprises project details, funding requests, and outcomes, and the task is to predict project funding success.

Loading Data:
To begin, the code loads the dataset from Google Drive using the Google Colab environment.

Data Preprocessing and Feature Engineering:
The code performs the following steps for data preprocessing and feature engineering:

Splitting Data
Data is split into training and test sets using stratified sampling to maintain class distribution.

Text Feature Encoding
The essay text feature is encoded using both TF-IDF and Count Vectorization techniques. This enables the conversion of textual data into a format suitable for modeling.

Categorical Feature Encoding
Categorical features like school state, teacher prefix, project grade category, clean categories, and clean subcategories are one-hot encoded using Count Vectorization.

Numerical Feature Normalization
Continuous features like price and teacher number of previously posted projects are normalized.

Model Application
The code applies the Naive Bayes classifier to two sets of features (Bag-of-Words and TF-IDF encoded essays) and performs hyperparameter tuning using GridSearchCV to optimize the model's performance. It then generates ROC-AUC curves and confusion matrices for both models.

Summary:
The key observations from the experiment are:
The Bag-of-Words (BoW) model slightly outperforms the TF-IDF model.
The AUC score is lower on the test set, indicating potential overfitting.
Top important features include words related to students, school, classroom, and learning.
Due to resource constraints, only a subset of the dataset and a limited number of features were used. Using the entire dataset and more features could lead to better results.
For more details and observations, refer to the code and comments in the notebook.

This project demonstrates the application of the Naive Bayes algorithm to predict the funding success of educational projects on DonorsChoose. By combining text, categorical, and numerical features, the models aim to provide insights into the factors influencing project outcomes.