# 🏷️ Price Prediction for Kids' Resale Items

## 📊 Project Overview

This project aims to predict the prices of kids' clothing and accessories listed on a Shopify-based resale platform. By analyzing product features such as brand, condition, and item type, a regression model is built to estimate fair resale prices.

---

## 🔍 Problem Statement

Accurate pricing is critical for resale platforms to ensure fairness and competitiveness. This project uses historical Shopify product data to build a machine learning model that predicts item prices based on relevant features from active listings.

---

## 🗃️ Dataset

- **Source**: Shopify product export (`products_export_1-2.csv`)
- **Scope**: Thousands of product listings, 53 columns
- **Filtered**: Focused only on active listings (archived listings removed)

---

## 🧾 Features Used

- **Brand**
- **Condition** (cleaned into: Excellent, Very Good, Like New, etc.)
- **Item Type**
- **Custom Tags** from Title (e.g., Joggers, Jeans, Leggings)
- **Optional**: Age/Size (evaluated for impact)

---

## 🔄 Workflow

### 1. 📥 Data Loading & Inspection
- Loaded CSV into Pandas
- Viewed structure using `.head()`, `.info()`, `.describe()`
- Checked for missing values and duplicates

### 2. 📊 Exploratory Data Analysis (EDA)
- Scatter plots and trend visuals for key features vs. price
- Condition and brand analysis for price distribution

### 3. 🧹 Data Cleaning
- Filtered to keep only “active” listings
- Cleaned condition column values
- Removed irrelevant columns
- Dropped rows with excessive nulls

### 4. 🚫 Outlier Detection & Normalization
- Identified outliers in pricing
- Removed extreme values
- Normalized features to scale input data

### 5. 🏗️ Feature Engineering
- Extracted item subtypes from titles (e.g., “Joggers” → new column)
- One-hot encoded categorical variables (e.g., condition, item type)

### 6. 🤖 Model Building
- Applied regression algorithms (Linear, Decision Tree, Random Forest)
- Split data into training & testing sets (80/20)
- Trained model and tuned basic hyperparameters

### 7. 📈 Evaluation
- Evaluated model using:
  - **R² Score**
  - **Mean Absolute Error (MAE)**
  - **Root Mean Squared Error (RMSE)**
- Compared predictions with actual prices

---

## ✅ Results

- **R² Score**: ~0.75  
- **MAE**: Low deviation from actual price  
- **Model**: Random Forest performed best overall

---

## 🛠️ Tools Used

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- Jupyter Notebook

---

## 💡 Future Work

- Deploy model using Streamlit or Flask  
- Automate daily price recommendations via Shopify API  
- Incorporate deep learning for improved accuracy  
- Apply GridSearchCV or RandomizedSearchCV for optimization

---

## 👨‍💻 Author

**Adan Abdullahi**  
Data Analyst | Machine Learning Enthusiast  
📍 Toronto, Canada  
🔗 [LinkedIn](https://www.linkedin.com/in/adan798)

