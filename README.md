# AWS-ML-Feature-Engineering-Pipeline
## Project Overview

This project demonstrates an end-to-end machine learning pipeline for housing price prediction using the Ames Housing Dataset. The pipeline includes data preprocessing, feature engineering, and model training using AWS cloud services. The preprocessing pipeline is built locally using a Jupyter Notebook, while model training is performed using Amazon SageMaker. The goal of this project is to transform raw housing data into machine learning-ready features and train a predictive model using a scalable cloud-based environment.

## System Architecture
<img width="1175" height="294" alt="image" src="https://github.com/user-attachments/assets/0c0e68ab-aeb7-4a5b-8a88-b8abfd69a243" />

## Dataset

The dataset used is the Ames Housing Dataset, which contains detailed information about residential home sales in Ames, Iowa.
Link: https://www.kaggle.com/datasets/prevek18/ames-housing-dataset/code 

## Features include:

*  Numerical attributes (Lot Area, Year Built, Gr Liv Area)

*  Categorical attributes (Neighborhood, House Style, Roof Type)

*  Potential outliers and missing values

The dataset was processed and split into:

*  train.csv
*  test.csv

These files were uploaded to Amazon S3 for model training.

## Technologies Used

*  Python

*  Jupyter Notebook

*  scikit-learn

*  Pandas

*  NumPy

*  Amazon S3

*  Amazon SageMaker

## Project Architecture

The workflow of the system is as follows:

1. Load raw dataset locally

2. Perform preprocessing and feature engineering

3. Build a feature engineering pipeline using ColumnTransformer

4. Split dataset into training and testing sets

5. Save processed data as CSV

6. Upload processed data to Amazon S3

7. Train machine learning model using Amazon SageMaker

8. Evaluate model performance

## Feature Engineering Pipeline

A preprocessing pipeline was created using scikit-learn ColumnTransformer to handle:

*  Missing values

*  Numerical feature scaling

*  Categorical feature encoding

*  Feature transformation

This pipeline ensures consistent preprocessing before training the model.

## Data Storage

The processed datasets were uploaded to an Amazon S3 bucket where they were used for training the machine learning model on SageMaker.

*  train.csv
*  test.csv
  
## Model Training

The machine learning model was trained using an AWS SageMaker notebook instance.

Steps included:

1. Loading training data from S3

2. Training a regression model

3. Evaluating prediction performance

The results of model training and evaluation are available in the SageMaker notebook.

Repository Structure
aws-ml-feature-engineering-pipeline

├── preprocessing_pipeline.ipynb

├── sagemaker_training.ipynb

├── AmesHousing.csv
 
├── README.md 

├── Test.csv

└── Train.csv

## Screenshots
### Essential Libraries
<img width="1299" height="606" alt="image" src="https://github.com/user-attachments/assets/8ee96d86-4971-491c-91db-83b4cf488bf4" />

### Column Transformer 
<img width="1210" height="596" alt="image" src="https://github.com/user-attachments/assets/a349570b-19f1-4094-8794-c74dd543d994" />

### Train/Test Split
<img width="1226" height="602" alt="image" src="https://github.com/user-attachments/assets/ff1c0461-4db8-4f1e-bf1b-c16d0bcf49c6" />

### Files uploaded to S3 bucket
<img width="1335" height="554" alt="image" src="https://github.com/user-attachments/assets/5e3e0de4-b3b7-463a-9144-13e9e1678cd1" />

### Notebook Instance
<img width="1062" height="228" alt="image" src="https://github.com/user-attachments/assets/d58ad0dc-3322-4fa4-adde-5a5d5ec6c940" />

### Model evaluation results
<img width="1254" height="593" alt="image" src="https://github.com/user-attachments/assets/89e99e9b-eea1-46de-a2de-32e5395b45ab" />

## How to Run the Project
### Step 1

Clone the repository

*  git clone https://github.com/yourusername/aws-ml-feature-engineering-pipeline.git
### Step 2

Install required libraries

*  pip install pandas numpy scikit-learn boto3
### Step 3

Run the preprocessing notebook

*  preprocessing_pipeline.ipynb
### Step 4

Upload processed data to Amazon S3

### Step 5

Run the SageMaker training notebook

*  sagemaker_training.ipynb
## Results

The machine learning model was successfully trained using AWS SageMaker using the processed dataset stored in S3.

Model evaluation results and outputs are included in the training notebook.
