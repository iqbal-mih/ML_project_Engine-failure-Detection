# 🔧 Project: Engine Failure Prediction using Time-Series Data

This project focuses on analyzing time-series sensor data to understand patterns leading to **engine failure**, using the [Engine Failure Detection Dataset](https://www.kaggle.com/datasets). The primary goal is to identify critical features and build a machine learning model to classify engine fault types.

## 📊 Objective

Predict the **fault type** of engines (0: no fault, 1-3: different failure modes) based on sensor readings and time-based features.

## 🧰 Workflow

### 1. Exploratory Data Analysis (EDA)
- Analyzed sensor trends across time
- Visualized feature distributions using:
  - Line plots
  - Boxplots
  - Histograms
- Examined correlation heatmaps
- Checked class balance in the `fault_type` variable

### 2. Feature Engineering
- Created **rolling statistics features** (mean, std, min, max) over time windows
- Dropped less informative or highly correlated features

### 3. Classification Models
Tested multiple classification algorithms:
- **Random Forest Classifier**
- **XGBoost Classifier**

**Initial Challenge:**  
Multiclass classification yielded **low accuracy**, even with balanced class distribution.

### 4. Binary Classification Approach
- Converted multiclass `fault_type` into **binary classification** (0: normal, 1: faulty)
- Improved performance significantly
- Selected **top 12 most important features** using model-based importance (e.g., `feature_importances_`)

## 🧠 Key Learnings
- Feature selection and binary classification improved accuracy
- Rolling features helped capture temporal patterns
- Tree-based models handle high-dimensional sensor data effectively

## 📁 Repository Contents
- `EDA project on Engine.ipynb`: Full notebook with EDA, preprocessing, modeling
- `README.md`: Project overview and documentation

