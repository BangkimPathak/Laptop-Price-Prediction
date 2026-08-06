# 💻 Laptop Price Prediction using Multiple Linear Regression

<<<<<<< HEAD
**Course**: Machine Learning / MLOps Lab Assignment  
**Topic**: Predicting Laptop Prices in USD ($) based on Hardware Specifications  
=======
**Topic**: Predicting Laptop Prices in Indian Rupees (INR / Rs.) based on Hardware Specifications  
>>>>>>> 29382b89f9ea5f69a9189c8827a5f4adb797cf81

---

## 📌 Project Overview
This project implements an end-to-end Machine Learning pipeline using **Multiple Linear Regression** to predict laptop prices based on technical hardware specifications. 

The pipeline includes synthetic data generation, exploratory data analysis (EDA), model training, evaluation metrics calculation (MAE, RMSE, $R^2$), feature importance analysis, and high-resolution data visualization.

---

## 🎯 Target & Features

- **Target Variable ($y$)**: `Price` — Continuous numerical value in US Dollars ($)
- **Feature Matrix ($X$)**:
  1. `RAM_GB`: Installed System RAM capacity (in GB)
  2. `Storage_SSD_GB`: SSD Storage capacity (in GB)
  3. `CPU_Cores`: Number of CPU processor cores
  4. `Screen_Size_Inches`: Display diagonal size (in Inches)

---

## 📁 Repository Directory Structure

```text
.
├── laptop_price_prediction.ipynb  # Main Jupyter Notebook containing complete ML code
├── laptop_prices.csv              # Dataset in USD (300 records)
├── actual_vs_predicted.png        # High-resolution scatter plot visualization
├── .gitignore                     # Git configuration ignoring cache & CSV files
└── README.md                      # Project documentation
```

---
## 📁 Databases extracted  from 
LINK: https://www.kaggle.com/datasets/sohaibdevv/modern-laptops-hardware-and-pricing-dataset-2026

## ⚙️ Environment Setup & Dependencies

Ensure Python 3.8+ is installed along with the required libraries:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn
```

### Required VS Code Extensions:
- **Python** (`ms-python.python`)
- **Jupyter** (`ms-toolsai.jupyter`)

---

## 🔄 Machine Learning Pipeline Steps

1. **Synthetic Data Generation**: 
   Generates a realistic synthetic dataset (`laptop_prices.csv`) with 300 samples based on ground-truth market pricing logic plus Gaussian noise.
2. **Exploratory Data Analysis (EDA)**:
   Performs initial dataset inspection using `df.head()`, `df.info()`, and `df.describe()`.
3. **Data Splitting**:
   Splits dataset into **80% Training Set** (240 samples) and **20% Testing Set** (60 samples) with `random_state=42`.
4. **Model Training**:
   Fits `sklearn.linear_model.LinearRegression` to fit the multiple linear regression weights.
5. **Model Evaluation**:
   Calculates regression evaluation metrics on the test set:
   - **Mean Absolute Error (MAE)**
   - **Root Mean Squared Error (RMSE)**
   - **R-squared ($R^2$) Score**
6. **Data Visualization**:
   Generates a publication-ready scatter plot (`actual_vs_predicted.png`) comparing actual vs. predicted laptop prices against an ideal fit reference line ($y = x$).

---

## 📊 Sample Model Performance & Results (USD)

### 1. Regression Equation:
$$\text{Price (\$)} = 55.07 + (37.69 \times \text{RAM\_GB}) + (0.69 \times \text{Storage\_SSD\_GB}) + (43.13 \times \text{CPU\_Cores}) + (36.76 \times \text{Screen\_Size\_Inches})$$

### 2. Feature Weight Interpretation:
- **CPU Cores ($\approx \$43.13$)**: Each additional CPU core increases laptop price by approximately $\$43.13$.
- **RAM ($\approx \$37.69$)**: Adding 1 GB of RAM increases price by $\$37.69$.
- **Screen Size ($\approx \$36.76$)**: An extra inch in screen size adds about $\$36.76$.
- **Storage SSD ($\approx \$0.69$)**: Every extra GB of SSD storage adds about $\$0.69$.

### 3. Evaluation Metrics on Test Set:
- **MAE**: $\$53.48$
- **RMSE**: $\$66.67$
- **$R^2$ Score**: **0.9848** ($98.48\%$ variance explained)

---

## 🖼️ Output Visualization

The notebook automatically exports a publication-quality visualization: **`actual_vs_predicted.png`**.

