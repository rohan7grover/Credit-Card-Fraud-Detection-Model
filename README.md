# Credit Card Fraud Detection Model

This project aims to develop a model for detecting credit card fraud by analyzing a dataset containing 772 rows and 31 columns. The response variable, 'Class,' indicates the presence of fraud in a transaction, with a value of 1 indicating fraud and 0 indicating no fraud. To evaluate the accuracy of the model, five different machine learning algorithms were employed.

## Data

The dataset includes 772 rows and 31 columns. Principal component analysis was applied to features V1 to V28, whereas 'Time' and 'Amount' are the only two features not subjected to PCA. They represent the time elapsed between each transaction and the first transaction in the dataset and the transaction amount, respectively. The dataset is imbalanced, with only 763 rows belonging to class 0 (no fraud) and just 9 rows belonging to class 1 (fraud).

## Data Pre-processing:

To balance the dataset, the SMOTE oversampling technique was applied, which increased the row count to 1526, with half belonging to class 0 and the other half to class 1. Five samples were then created using different sampling techniques, including random sampling, systematic sampling, stratified sampling, cluster sampling, and convenience sampling.

## Model:

Five different machine learning models were used in this study, including Random Forest Classifier, Logistic Regression, Gaussian Naive Bayes, KNN, and SVM. The accuracy of each model was calculated using K Fold Cross Validation.

## Results:

|  | Cluster Sampling | Random Sampling | Systematic Sampling  | stratified Sampling | Convenience Sampling |
| :----: |:--------------------:|:------------:|:------------:|:---------------:| :---------------:|
| Random Forest Classifier | 0.987013 | 0.987013 | 0.993548  | 0.979050 | 0.986667 |
| Logistic Regression | 0.919173 | 0.953144  | 0.872871 | 0.940123 | 0.963333 |
| Gaussian Naive Bayes | 0.739645 | 0.846206 | 0.830196 | 0.835748 | 0.976667 |
| KNN | 0.820301 | 0.799248 | 0.699260 | 0.770848 | 0.836667 |
| SVM | 0.664252 | 0.666746 | 0.666631 | 0.643301 | 0.690000 |

The Random Forest Classifier demonstrated the highest accuracy among the five models, with a rate of 99.35% when applied to the data generated using systematic sampling.

