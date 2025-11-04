# 🌦️ Weather Prediction using Machine Learning

This project develops **machine learning models** to classify weather conditions using the **Seattle Weather Dataset**.  
It applies multiple algorithms, handles class imbalance, tunes hyperparameters, and compares ensemble methods to achieve highly accurate weather classification.

---

## 📋 Table of Contents

- [Introduction](#introduction)  
- [Objectives](#objectives)  
- [Methodology](#methodology)  
- [Data Analysis](#data-analysis)  
- [Data Preprocessing](#data-preprocessing)  
- [Model Training and Results](#model-training-and-results)  
- [Results and Analysis](#results-and-analysis)  
- [Conclusion](#conclusion)  
- [Tech Stack](#tech-stack)  
- [How to Run](#how-to-run)  
- [Contributors](#contributors)  
- [License](#license)

---

## 🧠 Introduction

This project aims to classify daily weather into **five categories** — `rain`, `sun`, `drizzle`, `snow`, and `fog` — using machine learning models trained on the **Seattle Weather Dataset**.  
The dataset consists of approximately **1,460 daily observations** with meteorological features such as precipitation, temperature, and wind speed.

---

## 🎯 Objectives

- Develop and compare multiple machine learning models for weather classification.  
- Handle class imbalance using **SMOTEENN** (Synthetic Minority Oversampling + Edited Nearest Neighbors).  
- Perform **hyperparameter tuning** for Random Forest and XGBoost.  
- Evaluate performance using accuracy, precision, recall, and F1-score.  
- Explore **ensemble learning techniques** (Voting and Stacking) for optimal accuracy.

---

## ⚙️ Methodology

### 🧩 Process Flow

1. Load Seattle Weather Dataset  
2. Exploratory Data Analysis (EDA) & Visualization  
3. Data Preprocessing and Feature Engineering  
4. Apply **SMOTEENN** for class balancing  
5. Train-Test Split (80-20)  
6. Train 7 Machine Learning Models  
7. Perform Hyperparameter Tuning  
8. Implement Ensemble Methods  
9. Evaluate and Compare Models  

### 🤖 Algorithms Implemented

- Logistic Regression  
- Decision Tree  
- Support Vector Machine (SVM)  
- Random Forest  
- K-Nearest Neighbors (KNN)  
- AdaBoost  
- XGBoost  

### 🧮 Ensemble Methods

- **Voting Classifier** – Combines tuned Random Forest, KNN, and XGBoost using soft voting.  
- **Stacking Classifier** – Combines multiple base learners with Logistic Regression as meta-model.  

---

## 📊 Data Analysis

- **Total observations:** 1,461  
- **Missing values:** None  
- **Class imbalance:** Significant (Rain & Sun dominant)  
- **Feature correlation:** Max/Min temperature strongly correlated  
- **Distributions:** Precipitation is right-skewed; temperature follows normal distribution  

---

## 🧹 Data Preprocessing

- Extracted temporal features (`month`, `day`) from date.  
- Applied **SMOTEENN** to balance classes, expanding the dataset to **2,174 samples**.  
- Encoded labels numerically for model compatibility.  
- Split dataset into **80% training** and **20% testing**.

---

## 🧪 Model Training and Results

### 🔹 Initial Model Performance

| Model | Accuracy |
|--------|-----------|
| Logistic Regression | 0.7609 |
| Decision Tree | 0.9218 |
| SVM | 0.7701 |
| Random Forest | 0.9609 |
| KNN | 0.9287 |
| AdaBoost | 0.4736 |
| XGBoost | 0.9609 |

### 🔹 Hyperparameter Tuning

| Model | Tuned Accuracy |
|--------|----------------|
| Random Forest | 0.9678 |
| XGBoost | 0.9632 |

### 🔹 Ensemble Results

| Model | Accuracy | Precision | Recall | F1-Score |
|--------|-----------|------------|---------|-----------|
| **Stacking Ensemble** | **0.9839** | 0.9843 | 0.9839 | 0.9840 |
| Voting Ensemble | 0.9770 | 0.9776 | 0.9770 | 0.9770 |

---

## 📈 Results and Analysis

- **Ensemble methods** outperformed individual models.  
- **Stacking Classifier** achieved the highest accuracy (**98.39%**).  
- **Voting Ensemble** followed with **97.70%** accuracy.  
- **Tree-based models** (Random Forest, XGBoost, Decision Tree) performed best.  
- **SMOTEENN** significantly improved minority class recognition.  
- **AdaBoost** underperformed on this dataset (47.36% accuracy).  

---

## ✅ Conclusion

The project successfully demonstrates how **machine learning** and **ensemble techniques** can be used to accurately predict weather conditions.  
The **Stacking Classifier** achieved top performance (98.39%), proving the value of combining multiple algorithms.  

---

## 💻 Tech Stack

- **Python 3.9+**  
- **Libraries:**  
  - pandas, numpy  
  - matplotlib, seaborn  
  - scikit-learn  
  - xgboost, imbalanced-learn  

---

## 🚀 How to Run

1. Clone this repository  
   ```bash
   git clone https://github.com/<your-username>/weather-prediction-ml.git
   cd weather-prediction-ml
