# Bank Application Using Amazon SageMaker and S3

This repository contains an end-to-end machine learning project for predicting the effectiveness of a bank's marketing campaign. The project leverages Amazon SageMaker for model training, deployment, and prediction, and AWS S3 for storing and managing datasets. The model is built using XGBoost, one of the most efficient machine learning algorithms for classification problems.

## Project Highlights
### 1. Dataset: 
* The dataset contains information about a bank's telemarketing campaign and includes features like customer demographics, contact details, and campaign outcomes.
* Dataset source: https://d1.awsstatic.com/tmt/build-train-deploy-machine-learning-model-sagemaker/bank_clean.27f01fbbdf43271788427f3682996ae29ceca05d.csv
### 2. Amazon S3 Integration:
* Created an S3 bucket (bankkapplication) for secure storage of training and testing data.
* Uploaded processed datasets (train.csv and test.csv) into S3 for seamless integration with SageMaker.
### 3. Model Training:
* Used Amazon SageMaker's built-in XGBoost container to train a binary classification model.
* Hyperparameter tuning was performed to optimize the model for better accuracy and efficiency.
* Achieved 89.7% overall classification accuracy on the test data.
### 4. Deployment:
* Deployed the trained XGBoost model as a real-time prediction endpoint using SageMaker.
* Configured an ml.m4.xlarge instance for serving predictions.
### 5. Predictions:
* Evaluated model performance on test data, calculating key metrics like classification accuracy, true positive rate, and false positive rate.
* Generated a confusion matrix to visualize the model's prediction performance.

