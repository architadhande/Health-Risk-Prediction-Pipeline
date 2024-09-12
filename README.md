# Health Risk Prediction Pipeline

This repository contains a comprehensive health risk prediction pipeline developed using **Google Cloud Platform (GCP)**, **Kubeflow Pipelines**, **TensorFlow**, **Vertex AI**, and **BigQuery**. The pipeline is designed to predict cardiovascular risk factors and assess the likelihood of cardiovascular events with high accuracy.

## Project Overview

The primary objective of this project was to build a scalable and efficient machine learning pipeline to predict the risk of cardiovascular events based on various health factors. The pipeline utilizes multiple models running in parallel, leveraging advanced imputation, feature engineering, and ensemble techniques to improve prediction accuracy.

### Key Features

- **EDA (Exploratory Data Analysis)**:
  - Performed initial data exploration using **Tableau**, identifying univariate and bivariate relationships.
  - Investigated feature distributions, correlations, and outliers across variables such as Age, BMI, Blood Pressure, Cholesterol, and Glucose levels.

- **Data Preprocessing**:
  - **Feature Engineering**: Applied transformations such as scaling, encoding categorical variables, and creating new features to enhance model performance.
  - **Imputation**: Used advanced imputation techniques to handle missing values, ensuring the integrity of the dataset for training.

- **Model Training and Evaluation**:
  - Developed multiple machine learning models including **Random Forest**, **Logistic Regression**, **Gradient Boosting**, and others to predict cardiovascular risk.
  - Implemented a **Voting Classifier ensemble** to aggregate predictions, achieving a substantial improvement in model performance.
  - Achieved an **F1-score of 97%**, surpassing the original target of 95%. The model effectively identified high-risk individuals, significantly improving prediction accuracy compared to baseline models.

## Pipeline Architecture

1. **Data Ingestion**:
    - Data stored in **Google Cloud Storage** is ingested through **BigQuery** for processing.
    
2. **Preprocessing Components**:
    - **Kubeflow Pipelines** manage the preprocessing steps including imputation, scaling, and feature selection.
    
3. **Model Development**:
    - Multiple machine learning models are trained in parallel within **Kubeflow Pipelines**.
    - Evaluated models based on performance metrics such as F1-score, precision, and recall to select the best models.
    
4. **Ensemble Model**:
    - The best-performing models are combined into an ensemble to improve prediction accuracy.
    
5. **Inference Pipeline**:
    - Deployed the final model on **Vertex AI** to allow real-time predictions for health risk assessments based on new patient data.

## Technologies Used

- **Google Cloud Platform (GCP)**: Used for scalable storage, processing, and deployment.
- **Kubeflow Pipelines**: Orchestrated the machine learning workflow, enabling parallel processing of models.
- **TensorFlow**: Built, trained, and optimized machine learning models.
- **Vertex AI**: Deployed the final ensemble model for real-time inference.
- **BigQuery**: Managed large datasets and performed data queries efficiently.
- **Tableau**: Used for EDA and creating detailed visual reports on health metrics.

## Results

- **F1-Score**: 97% (Exceeded the original target of 95%)
- **Model Performance**: Significantly improved over baseline models.
- **Prediction Accuracy**: Effectively identified high-risk individuals with increased accuracy and reliability.

## Setup Instructions

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/health-risk-prediction-pipeline.git

