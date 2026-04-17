# 🏠 House Price Prediction using XGBoost & ANN

## 📌 Project Overview

This project aims to predict house prices using two powerful approaches:

* **XGBoost (Tree-based model)**
* **Artificial Neural Network (ANN)**

The goal is to compare their performance and understand how different modeling approaches handle tabular data.

---

## 📂 Dataset

* File: `train.csv`
* Includes features such as:

  * Area / Size
  * Number of rooms
  * Location
  * Year built
  * Other house-related attributes
* Target variable: **House Price**

---

## ⚙️ Data Preprocessing

### 1. Train-Test Split

* 80% Training
* 20% Testing

### 2. Handling Missing Values

* Numerical features → filled with **mean**
* Categorical features → filled with **most frequent value**

### 3. Feature Engineering

* Categorical variables → **One-Hot Encoding**
* Numerical variables → **Standard Scaling**

### 4. ColumnTransformer

* Combined preprocessing steps into a single pipeline

---

## 🤖 Models Used

### 🔹 XGBoost

* Tree-based gradient boosting model
* Handles non-linear relationships well
* Does not require feature scaling

### 🔹 Artificial Neural Network (ANN)

* Dense layers with ReLU activation
* Optimizer: Adam
* Loss: Mean Squared Error
* Sensitive to feature scaling

---

## 🧪 Experiments

### 1. All Features

* Trained models using all available features

### 2. Feature Selection (for ANN)

* Selected top features using XGBoost feature importance
* Trained ANN again with selected features

---

## 📊 Evaluation Metrics

* MAE (Mean Absolute Error)
* RMSE (Root Mean Squared Error)

---

## 📈 Results

| Model                   | MAE                    | RMSE                   |
| ----------------------- | ---------------------- | ---------------------- |
| ANN (Selected Features) | ~21,028                | ~34,027                |
| ANN (All Features)      | ~21,358                | ~31,356                |
| XGBoost                 | ~17,194                | ~25,871                |

---

## 🔍 Key Findings

* ANN with **all features performed slightly better** than selected features
* Feature importance from XGBoost does not always improve ANN performance
* ANN captures complex patterns but struggles with high-value houses
* XGBoost is generally more stable for tabular data

---

## 📉 Residual Analysis

* Residual = Actual Price − Predicted Price
* Observations:

  * Errors increase with higher house prices
  * Presence of outliers
  * Model performs better on mid-range prices

---

## 🧠 Insights

* Tree-based models and ANN learn differently:

  * XGBoost → strong with structured/tabular data
  * ANN → benefits from feature interactions
* Feature selection should be validated experimentally
* High-value predictions remain challenging

---

## 🛠️ Tech Stack

* Python
* Pandas / NumPy
* Scikit-learn
* XGBoost
* TensorFlow / Keras
* Matplotlib

---

## 👤 Author

GitHub: https://github.com/IttikornMafaka

---

## ✅ Conclusion

This project compares XGBoost and ANN for house price prediction.
It highlights how different models perform on tabular data and emphasizes the importance of preprocessing, feature selection, and error analysis.
