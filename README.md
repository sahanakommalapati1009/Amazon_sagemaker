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

## Project Workflow
### 1. Data Preparation:
* Downloaded the dataset and stored it locally.
* Preprocessed the data, including splitting into training and testing datasets.
* Uploaded the datasets to an S3 bucket.
### 2. Model Building:
* Used SageMaker's built-in XGBoost algorithm.
* Configured hyperparameters such as max_depth, eta, gamma, and subsample.
* Trained the model using managed spot training to optimize cost.
### 3. Model Deployment:
* Created an endpoint for real-time predictions using SageMaker's deployment feature.
* Configured serialization and deserialization for data input/output.
### 4. Evaluation:
* Assessed model predictions on test data.
* Visualized classification performance using a confusion matrix and accuracy metrics.

## Technologies and Tools
* Amazon SageMaker: For model training, deployment, and endpoint creation.
* Amazon S3: For dataset storage and management.
* XGBoost: Used for binary classification.
* Python Libraries:
  - pandas, numpy: For data manipulation.
  - boto3: For AWS S3 integration.
  - sagemaker: For managing SageMaker training and deployment.

## Key Results
* Overall Classification Accuracy: 89.7%
* Confusion Matrix:
  - True Negatives: 10,785
  - False Positives: 151
  - False Negatives: 1,124
  - True Positives: 297

## Usage
### 1. Ensure AWS and Python Are Set Up:
* Make sure you have an AWS account and the AWS CLI is configured on your machine.
* Install Python and the required dependencies.
### 2. Install Dependencies:
pip install pandas numpy boto3 sagemaker matplotlib scikit-learn
### 3. Run the Python Script:
python BankMarketingPrediction.py

