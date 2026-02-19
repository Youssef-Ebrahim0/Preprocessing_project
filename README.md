# Team 1 -> Preprocessing_project
🌧️ Rain Tomorrow Prediction – Machine Learning Project
📌 Project Overview

This project focuses on predicting whether it will rain tomorrow (RainTomorrow) using historical weather data from Australia. The solution applies a complete end-to-end Machine Learning pipeline including:

Exploratory Data Analysis (EDA)

Missing value handling

Feature preprocessing

Class imbalance handling

Model training and evaluation

The final model uses a Random Forest Classifier to predict rainfall for the next day.

📂 Dataset

Dataset Name: weatherAUS.csv

Target Variable: RainTomorrow (Yes/No)

Type: Binary Classification

Domain: Weather Forecasting

The dataset contains multiple meteorological features such as:

Temperature (MinTemp, MaxTemp)

Rainfall

Humidity

Wind Speed

Pressure

Cloud coverage

Location & Date information

⚙️ Project Workflow
1️⃣ Data Exploration (EDA)

Checked dataset structure and summary statistics

Analyzed feature distributions

Visualized relationships between features and target variable

Identified missing values

Visualized class imbalance

2️⃣ Data Preprocessing
✔ Handling Missing Values

Numerical features: IterativeImputer

Categorical features: SimpleImputer (most_frequent)

✔ Feature Engineering

Converted Date column to datetime format

Separated numerical and categorical features

✔ Encoding

Applied LabelEncoder to categorical variables

✔ Scaling

Applied StandardScaler to normalize numerical features

3️⃣ Handling Class Imbalance

The dataset showed imbalance in the RainTomorrow variable.

To address this:

Applied SMOTE (Synthetic Minority Over-sampling Technique)

Balanced the training dataset before model training

4️⃣ Model Training

Model Used: Random Forest Classifier

RandomForestClassifier(
    n_estimators=500,
    class_weight='balanced',
    random_state=42,
    n_jobs=-1
)


Reasons for choosing Random Forest:

Handles non-linearity well

Robust to noise

Works effectively with mixed feature types

Performs well on structured tabular data

5️⃣ Model Evaluation

Evaluation Metrics Used:

Accuracy

Confusion Matrix

Precision

Recall

F1-Score

ROC-AUC Score

Example Performance:

Accuracy: ~84%

Strong performance on majority class

Good ROC-AUC score indicating solid discrimination ability

The confusion matrix and ROC-AUC were visualized for better interpretability.

📊 Technologies & Libraries

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Imbalanced-learn (SMOTE)
