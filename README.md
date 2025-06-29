# 🔍 Churn Prediction using Artificial Neural Network (ANN)

This project presents a machine learning pipeline to predict customer churn using an **Artificial Neural Network (ANN)**. It includes data preprocessing, encoding categorical variables, feature scaling, ANN model training using **TensorFlow/Keras**, and prediction evaluation.

---

## 📁 Project Overview

The goal is to build a binary classification model that predicts whether a customer will **exit (churn)** or stay, based on features like geography, age, balance, and activity.

---

## 🧠 Model Highlights

- **Framework**: TensorFlow / Keras
- **Model Type**: Fully Connected ANN (Feedforward Neural Network)
- **Architecture**:
  - Input Layer (11+3 geography features)
  - Hidden Layers: 64 and 32 units with ReLU
  - Output Layer: 1 unit with Sigmoid activation
- **Loss**: Binary Crossentropy
- **Optimizer**: Adam (`lr=0.01`)
- **EarlyStopping**: Enabled to prevent overfitting
- **TensorBoard**: Used for training visualization

---

## 📊 Dataset

- Dataset: `Churn_Modelling.csv`  
- Contains 14 columns including:
  - `CreditScore`, `Geography`, `Gender`, `Age`, `Balance`, `NumOfProducts`, etc.
  - Target column: `Exited` (1: Churned, 0: Retained)

---

## ⚙️ Workflow Steps

1. **Data Preprocessing**
   - Dropped irrelevant columns: `RowNumber`, `CustomerId`, `Surname`
   - Label Encoding: `Gender`
   - One-Hot Encoding: `Geography`
   - Feature Scaling: `StandardScaler`

2. **Model Training**
   - Train-test split (80/20)
   - Compiled ANN with `Adam` optimizer and `binary_crossentropy`
   - Used EarlyStopping and TensorBoard for training monitoring

3. **Model Saving**
   - Saved trained model as `model.h5`
   - Saved encoders and scaler using `pickle`

---


