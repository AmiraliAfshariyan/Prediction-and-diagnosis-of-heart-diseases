# 💔 Heart Disease Prediction & Diagnosis System

An advanced medical data-science solution designed to **predict and diagnose the presence of heart disease** based on patients' clinical parameters and cardiovascular metrics. This repository contains an end-to-end machine learning workflow featuring rigorous data preprocessing, multi-scaler optimization, and precise model evaluation.

---

## 🎯 Key Features
- **Exploratory Data Analysis (EDA):** Complete statistical distribution profiling and visual analysis of core clinical indicators.
- **Multi-Scaler Optimization:** Comparative benchmarking using `StandardScaler`, `RobustScaler`, and `QuantileTransformer` to maximize accuracy across varied physiological scales.
- **High-Accuracy Classification:** Employs tuned classification algorithms to map patient metrics directly to diagnosis outcomes.
- **Strict Clinical Evaluation:** Models are scrutinized under critical medical standards to balance accuracy and positive diagnostic capture rates.

---

## 📊 Dataset Structure
The project processes a structured medical dataset (`heart.csv`) containing records of clinical patient examinations with the following core metrics:
- `age`: Patient's age in years.
- `sex`: Sex classification (`1` = male; `0` = female).
- `cp`: Chest pain type (ordinal indicator values).
- `trtbps`: Resting blood pressure (in mm Hg on admission to the hospital).
- `chol`: Serum cholesterol measurement in mg/dl.
- `fbs`: Fasting blood sugar levels (> 120 mg/dl, `1` = true; `0` = false).
- `restecg`: Resting electrocardiographic results.
- `thalachh`: Maximum heart rate achieved during examination.
- `output`: The final target diagnosis indicator (`1` = presence of heart disease, `0` = normal condition).

---

## 🛠️ Data Pipeline & Preprocessing

### 1. Robust Feature Scaling
Because physiological and biometric data can contain dramatic differences in raw scales (e.g., blood pressure vs. cholesterol counts), three scaler approaches are systematically integrated:
- **StandardScaler:** Normalizes continuous columns to center the mean around zero and scale to unit variance.
- **RobustScaler:** Minimizes distortion caused by clinical outliers or highly volatile biometric spikes using interquartile metrics (IQR).
- **QuantileTransformer:** Smooths non-linear biometric relationships by mapping physiological variables into stable normal distributions.

### 2. Validation Architecture
The dataset is split into independent training and validation domains using an optimized `train_test_split` ratio to carefully evaluate the model on completely unseen medical profiles.

---

## 🤖 Modeling & Performance Evaluation

The diagnostic classifier maps patient risk vectors to output precise health classifications. The pipeline delivered highly successful results on the evaluation framework.

### 📈 Model Performance Metrics
The system achieves excellent diagnostics accuracy on testing partitions:

| Metric | Score |
| :--- | :--- |
| **Accuracy** | **86.88%** |
| **Precision** | **90.00%** |
| **Recall (Sensitivity)** | **84.37%** |
| **F1-Score** | **87.10%** |

---

## 🚀 Installation & Usage

### Prerequisites
Ensure you have Python installed on your system. Install the required analytical data-science dependencies via pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
