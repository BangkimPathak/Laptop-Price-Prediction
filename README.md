# 💻 Laptop Price Prediction using Multiple Linear Regression

 **MLOps Lab Assignment**  
**Topic**: Predicting Laptop Prices in Indian Rupees (INR / Rs.) based on Hardware Specifications  

---

## 📌 Project Overview
This project implements an end-to-end Machine Learning pipeline using **Multiple Linear Regression** to predict laptop prices based on technical hardware specifications. 

The pipeline includes synthetic data generation, exploratory data analysis (EDA), model training, evaluation metrics calculation (MAE, RMSE, $R^2$), feature importance analysis, and high-resolution data visualization.

---

## 🎯 Target & Features

- **Target Variable ($y$)**: `Price` — Continuous numerical value in Indian Rupees (INR / Rs.)
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
├── laptop_prices.csv              # Synthetic dataset (300 records)
├── actual_vs_predicted.png        # High-resolution scatter plot visualization
└── README.md                      # Project documentation
```

---

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

## 📊 Sample Model Performance & Results

### 1. Regression Equation:
$$\text{Price (Rs.)} = 8671.25 + (2979.38 \times \text{RAM}) + (54.61 \times \text{SSD}) + (3575.19 \times \text{CPU\_Cores}) + (2950.53 \times \text{Screen\_Size})$$

### 2. Feature Weight Interpretation:
- **CPU Cores ($\approx \text{Rs. } 3,575.19$)**: Each additional core adds approx. $\text{Rs. } 3,575$ to price.
- **RAM ($\approx \text{Rs. } 2,979.38$)**: Each additional GB of RAM adds approx. $\text{Rs. } 2,979$.
- **Screen Size ($\approx \text{Rs. } 2,950.53$)**: Each additional inch adds approx. $\text{Rs. } 2,950$.
- **Storage SSD ($\approx \text{Rs. } 54.61$)**: Each GB of SSD storage adds approx. $\text{Rs. } 54.61$.

### 3. Evaluation Metrics on Test Set:
- **MAE**: $\text{Rs. } 3,565.59$
- **RMSE**: $\text{Rs. } 4,444.32$
- **$R^2$ Score**: **0.9890** ($98.90\%$ variance explained)

---

## 🖼️ Output Visualization

The notebook automatically exports a publication-quality visualization: **`actual_vs_predicted.png`**.

