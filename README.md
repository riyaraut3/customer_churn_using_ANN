# Binary Classification using Artificial Neural Network (ANN)

This project builds and evaluates a binary classification model using a feedforward Artificial Neural Network (ANN) in TensorFlow/Keras.

---

## 📂 Dataset

The dataset used consists of structured tabular data with **13 numerical features** per sample. It is suitable for binary classification (label: 0 or 1).  
Common use cases for such data include **medical diagnostics**, **credit scoring**, or **churn prediction**, although the exact context can vary.

- 📌 Target variable: Binary (0/1)
- 📌 Total features: 13
- 📌 Data format: Preprocessed and scaled numeric values

---

## ⚙️ What I Did

- Built an ANN for binary classification.
- Trained the model using a labeled dataset.
- Visualized training & validation metrics (accuracy and loss).
- Wrote a reusable evaluation function to compute:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - ROC AUC Score
  - Confusion Matrix with heatmap

---

## 🔬 How I Did It

### 🔧 Model Architecture

- **Input Layer**: 13 features  
- **Hidden Layer 1**: Dense(7), activation='relu'  
- **Hidden Layer 2**: Dense(6), activation='relu'  
- **Output Layer**: Dense(1), activation='sigmoid'  

### 🧠 Training Configuration

- Optimizer: `adam`  
- Loss Function: `binary_crossentropy`  
- Metrics: `accuracy`

### 🧪 Evaluation Code

Created a function `evaluate_binary_model(model, X_test, y_test)` to:

- Predict class labels from the model
- Calculate core metrics
- Plot confusion matrix using Seaborn

---

## 📊 Training & Evaluation Workflow

1. **Train the Model**

```python
model.fit(X_train, y_train, epochs=..., batch_size=..., validation_data=(X_val, y_val))
