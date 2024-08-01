# Heart Failure Prediction System

This project predicts the risk of heart failure using a machine learning model trained on the Heart Failure Clinical Records Dataset. The system also includes a graphical user interface (GUI) for user interaction.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Dependencies](#dependencies)
- [Data Preprocessing](#data-preprocessing)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)
- [Prediction](#prediction)
- [GUI Application](#gui-application)
- [Usage](#usage)
- [License](#license)

## Overview

Heart failure is a serious condition where the heart cannot pump enough blood to meet the body's needs. This project aims to predict the risk of heart failure using various clinical features. By leveraging machine learning, specifically a Support Vector Machine (SVM) classifier, we can help healthcare professionals identify at-risk patients and potentially take preventive measures.

## Dataset

The dataset used in this project is the Heart Failure Clinical Records Dataset, which contains medical records of 299 patients. It includes the following 13 features:

- **Age**: Age of the patient (years)
- **Anaemia**: Decrease of red blood cells or hemoglobin (boolean)
- **High Blood Pressure**: If the patient has hypertension (boolean)
- **Creatinine Phosphokinase (CPK)**: Level of the CPK enzyme in the blood (mcg/L)
- **Diabetes**: If the patient has diabetes (boolean)
- **Ejection Fraction**: Percentage of blood leaving the heart at each contraction (percentage)
- **Platelets**: Platelets in the blood (kiloplatelets/mL)
- **Serum Creatinine**: Level of serum creatinine in the blood (mg/dL)
- **Serum Sodium**: Level of serum sodium in the blood (mEq/L)
- **Sex**: Male or female (binary)
- **Smoking**: If the patient smokes or not (boolean)
- **Time**: Follow-up period (days)
- **Death Event**: If the patient deceased during the follow-up period (boolean, target variable)

## Dependencies

The project requires the following Python libraries:

- `numpy`: For numerical operations
- `pandas`: For data manipulation and analysis
- `scikit-learn`: For machine learning algorithms and tools
- `tkinter`: For creating the graphical user interface

You can install these dependencies using `pip`:  
`pip install numpy pandas scikit-learn tkinter`

## Data Preprocessing

Data preprocessing steps include:

1. **Loading the Dataset**: The dataset is loaded into a pandas DataFrame from a CSV file.
2. **Feature Selection**: We select the relevant features from the dataset for training the model.
3. **Handling Missing Values**: Missing values are imputed or handled appropriately.
4. **Feature Scaling**: The clinical features are scaled using `StandardScaler` from scikit-learn. This standardizes the features to have a mean of 0 and a standard deviation of 1, which helps in improving the performance of the SVM classifier.

## Model Training

The model training process involves the following steps:

1. **Data Splitting**: The dataset is split into training and testing sets using `train_test_split` from scikit-learn.
2. **Model Selection**: An SVM classifier with a linear kernel is selected.
3. **Training the Model**: The SVM classifier is trained on the training data using the `fit` method.

## Model Evaluation

The model's performance is evaluated using the following metrics:

1. **Accuracy**: The accuracy of the model is calculated using `accuracy_score` from scikit-learn. This measures the proportion of correctly predicted instances out of the total instances.
2. **Confusion Matrix**: A confusion matrix is generated to visualize the performance of the model.

## Prediction

The system includes a function to make predictions based on user input. The input features provided by the user are scaled using the same scaler used during training. The SVM classifier then predicts the risk of heart failure based on these features.

## GUI Application

A simple GUI is created using Tkinter to make the system user-friendly. The GUI allows users to:

1. **Input Features**: Enter the clinical features of a patient.
2. **Get Prediction**: Click a button to get the prediction on the risk of heart failure.

The GUI displays the result, indicating whether the patient is at risk of heart failure or not.

## Features
- Data Collection and Analysis: Utilizes the heart failure clinical records dataset for analysis.
- Model Training: Implements a Support Vector Machine (SVM) classifier to predict heart failure.
- Graphical User Interface (GUI): Provides an interactive Tkinter-based interface for user input and prediction.
## Example
Once the script is running, you will see a Tkinter window where you can input the following details:

- Age
- Anaemia
- Creatinine Phosphokinase
- Diabetes
- Ejection Fraction
- Blood Pressure
- Platelets
- Serum Creatinine
- Serum Sodium
- Gender
- Smoking
- Time  
After entering the values and clicking "Predict", the application will display a message indicating whether the patient is at risk of heart failure.

##License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

