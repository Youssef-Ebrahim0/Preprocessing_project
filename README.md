# Team 1 -> Preprocessing_project
🌧️ Rain Tomorrow Prediction – Machine Learning Project
📌 Project Overview

This project aims to predict whether it will rain tomorrow (RainTomorrow) using historical weather data from Australia. It implements a complete end-to-end Machine Learning pipeline including data preprocessing, handling missing values, managing class imbalance, model training, and performance evaluation.

The final model is built using a Random Forest Classifier.

📂 Dataset

Dataset: weatherAUS.csv

Target Variable: RainTomorrow (Yes/No)

Problem Type: Binary Classification

Domain: Weather Forecasting

Key Features:

Temperature (MinTemp, MaxTemp)

Rainfall

Humidity

Wind Speed

Pressure

Cloud coverage

Location and Date

⚙️ Project Workflow
1️⃣ Exploratory Data Analysis (EDA)

Inspected dataset structure and data types

Checked missing values

Analyzed feature distributions

Visualized correlations

Examined class imbalance in target variable

2️⃣ Data Preprocessing
✔ Missing Value Handling

Numerical features → IterativeImputer

Categorical features → SimpleImputer (most_frequent)

✔ Feature Engineering

Converted Date column to datetime format

Separated numerical and categorical features

✔ Encoding

Applied LabelEncoder for categorical variables

✔ Scaling

Applied StandardScaler to numerical features

3️⃣ Handling Class Imbalance

The dataset was imbalanced.

To address this:

Applied SMOTE (Synthetic Minority Over-sampling Technique) on training data

Balanced the minority class before training

4️⃣ Model Training

Model Used: Random Forest Classifier

from sklearn.ensemble import RandomForestClassifier

rf_model = RandomForestClassifier(
    n_estimators=500,
    class_weight='balanced',
    random_state=42,
    n_jobs=-1
)

Why Random Forest?

Handles non-linear relationships

Robust to noise

Performs well on structured tabular data

Reduces overfitting via ensemble learning

📊 Model Evaluation
Metrics Used:

Accuracy

Confusion Matrix

Precision

Recall

F1-Score

ROC-AUC Score

Example Performance:

Accuracy: ~84%

Good balance between precision and recall

Strong ROC-AUC indicating reliable discrimination

🛠️ Technologies & Libraries

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-learn

Imbalanced-learn (SMOTE)
