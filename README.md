# 🎧 Headphone Recommendation System (R Programming)

This project is a complete analysis and recommendation system for headphones using R.  
It includes data cleaning, exploratory data analysis (EDA), clustering, machine learning models, and a final recommendation engine that suggests headphones by price range and feature similarity.

---

## 🚀 Project Overview

The goal was to understand how different factors — such as price, brand, ratings, discount, and type — influence headphone pricing and purchase preferences.  
Using these insights, we built:

- A price prediction model  
- A price-segment classifier (Budget / Mid / Premium)  
- A dual-layer recommendation system  
- Multiple visualizations to understand patterns  

All analysis and modelling were done using **RStudio**.

---

## 📊 What the Project Includes

### ✔ Data Preprocessing
- Removed duplicates & missing values  
- Cleaned inconsistent category labels  
- Created new fields like  
  - Discount %  
  - Price After Discount  
  - Popularity (Rating × Number of Ratings)  
- Normalized numerical features  
- One-hot encoded categorical attributes  

---

## 📈 Exploratory Data Analysis

Some patterns discovered:

- **Wireless & on-ear headphones are the most expensive**
- **Budget category contains most products (~79%)**
- **Ratings and number of ratings strongly influence popularity**
- **Higher discounts usually mean lower selling price**
- **Some brands consistently sell at premium prices**

### Visual Outputs

| Chart | Image |
|------|-------|
| Average Selling Price by Type | ![](/Average Selling Price by Headphone Type.jpg) |
| Price vs Rating (Clustered) | ![](/Clusters — Price vs Rating by Segment.jpg) |
| Correlation Heatmap | ![](/Correlation Heatmap.jpg) |
| Actual vs Predicted (Random Forest) | ![](Actual vs Predicted — Random Forest (Regression).jpg) |
| Feature Importance | ![](/Top 15 Important Features — Random Forest.jpg) |
| Top Companies by Average Price | ![](/Top Companies by Average Price.jpg) |
| Price Distribution by Segment | ![](/Price Distribution by Segment.jpg) |

---

## 🤖 Machine Learning Models Used

### **1. Linear Regression**
- Baseline model  
- R² ≈ 0.70  

### **2. Decision Tree**
- Good interpretability  
- Classification accuracy ≈ 99%  

### **3. Naïve Bayes**
- Performed poorly (≈ 18% accuracy)

### **4. Random Forest (Best Performing)**
- **R²: ~0.91**  
- **Lowest RMSE & MAE**  
- Excellent for non-linear pricing patterns  
- Top features: Price Segment, MRP, Discount %, Brand indicators  

---

## 🎯 Recommendation Engine

### ✔ Price-Based Recommendation  
Suggests alternatives within **₹500** of the selected headphone.

### ✔ Similarity-Based Recommendation  
Uses **cosine similarity** on:
- Brand  
- Type  
- Colour  
- Ratings  
- Discount %  

This ensures the user gets **budget-friendly + similar feature** recommendations.

---

## 🧠 Difficulties Faced

- Many “Type” values were actually colours (e.g., “Red”, “Black”), so manual cleaning was needed.  
- Naïve Bayes failed because the dataset had correlated features.  
- Clustering needed scaling and normalization to work properly.  
- Random Forest required tuning to get stable and accurate results.

---

## 📘 What I Learned

- Handling real-world, messy e-commerce data  
- Creating useful derived features for better ML performance  
- Difference between linear vs tree-based models  
- How discounts and popularity influence price  
- Designing a practical recommendation workflow  
- Using R packages like **ggplot2**, **dplyr**, **caret**, **cluster**, etc.  
- Creating meaningful visual explanations  

---
## 👤 Authors

- **Krutika Chaudhari** (1132231002)  
- **Shravani Wani** (1132230868)  
MIT World Peace University, Pune
## 📂 Project Structure

