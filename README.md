# Customer Churn Prediction using Artificial Neural Network (ANN)

This project builds and evaluates a binary classification model using a feedforward Artificial Neural Network (ANN) in TensorFlow/Keras. The task is to predict whether a bank customer will churn based on historical data.

---

## 📂 Dataset: Churn_Modelling.csv

The dataset used is `Churn_Modelling.csv`, which contains customer data from a bank. Each row represents a customer, and the goal is to predict whether they have exited (churned) or not.

### 🔢 Key Features:

- `CreditScore`: Numerical credit score of the customer  
- `Geography`: Country of the customer (e.g., France, Germany, Spain)  
- `Gender`: Male or Female  
- `Age`: Customer's age  
- `Tenure`: Number of years with the bank  
- `Balance`: Account balance  
- `NumOfProducts`: Number of bank products used  
- `HasCrCard`: Has a credit card (0 or 1)  
- `IsActiveMember`: Active bank member (0 or 1)  
- `EstimatedSalary`: Estimated salary  
- `Exited`: **Target variable** (1 = churned, 0 = stayed)

### 🧹 Preprocessing:

- Converted categorical variables using OneHotEncoding / LabelEncoding  
- Scaled numerical features using StandardScaler  
- Split data into training and test sets

---

## ⚙️ What I Did

- Built an ANN for binary classification using customer data  
- Trained the model using the Keras Sequential API  
- Visualized training and validation accuracy/loss  
- Created an evaluation function to report model performance

---

## 🔬 How I Did It

### 🧠 Model Architecture

- Input Layer: 11 features after preprocessing  
- Hidden Layer 1: Dense(7), activation='relu'  
- Hidden Layer 2: Dense(6), activation='relu'  
- Output Layer: Dense(1), activation='sigmoid'

### ⚙️ Training Details

- Optimizer: `adam`  
- Loss Function: `binary_crossentropy`  
- Metrics: `accuracy`

---

## 📊 Evaluation

Created a custom function `evaluate_binary_model()` to compute:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC AUC Score
- Confusion Matrix (with heatmap)



