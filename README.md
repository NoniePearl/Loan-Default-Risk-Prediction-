# LOAN DEFAULT RISK PREDICTION: A DATA-DRIVEN JOURNEY

---

## 📌 Problem Statement  
Every financial institution faces a common dilemma: **How do we know if a borrower will repay a loan or default?**  

Traditional credit scoring methods often fail to capture the complexity of human behavior and financial conditions. Defaults not only harm banks' profitability but also limit opportunities for honest borrowers.  

This project explores the use of **machine learning** to build a robust loan default prediction system that can support smarter credit decisions.  

---

## 🎯 Objectives  
- Collect and preprocess borrower data from multiple sources.  
- Explore, clean, and transform raw datasets into reliable features.  
- Engineer new features from historical loan behavior.  
- Build, train, and evaluate machine learning models for default prediction.  
- Compare algorithms and recommend the best-performing model for deployment.  

---

## 🛠 Methodology  
Our journey followed a structured, iterative **data science lifecycle**. We started by collecting clues (data), cleaning them, discovering patterns, and finally testing different suspects (models) to find the best predictor.  

### 1. Data Collection  
- **Target (trainperf):** Contained current loan applications and the crucial `good_bad_flag` (target variable).  
- **Profile (traindemographics):** Customer personal details such as age, bank, and employment status.  
- **History (trainprevious):** A detailed ledger of past loan transactions for each customer.  

### 2. Data Preprocessing  
- **Performance Data:** Dropped `referredby` column (86% missing values).  
- **Demographics Data:** Removed 12 duplicate customer profiles. Dropped nearly empty columns like `bank_branch_client` and `education_level`.  
- **Previous Loans Data:** Converted date strings into machine-readable `datetime`. Missing categorical values (e.g., employment status) filled with `"Unknown"`.  

### 3. Feature Engineering  
From historical loan data, we crafted new features to tell a story about each customer:  
- **Repayment Delay** = difference between due date and repayment date.  
- **Interest Rate** = normalized interest based on loan amount and term days.  
- **Repayment Ratio** = total due ÷ loan amount.  
- **Customer Age** = age of borrower at loan creation date.  

### 4. Exploratory Data Analysis (EDA)  
Applied visualization techniques (histograms, boxplots, correlation heatmaps). Findings:  
- Most loans had terms of **30 days**.  
- **Good loans** outweighed **Bad loans**.  
- Features like **repayment delay**, **interest rate**, and **past loan amounts** showed strong predictive signals.  

### 5. Modelling  
- Split data into **Training (80%)** and **Testing (20%)**.  
- Built a preprocessing pipeline (standardized numerical data & encoded categorical data).  
- Trained **four algorithms**:  
  - Logistic Regression → Fundamental, interpretable baseline.  
  - Decision Tree → Rule-based model.  
  - Random Forest → Ensemble method combining many trees.  
  - Gradient Boosting → Sequential ensemble technique correcting errors.  

### 6. Model Evaluation  
Models evaluated using **accuracy, F1-score, precision, recall, and confusion matrices**.  
- **Gradient Boosting** emerged as the most reliable with **80% test accuracy** and **96% recall**.  

---

## 📊 Results & Findings  
- **Gradient Boosting** outperformed others in balancing **accuracy** and **recall**.  
- **Best Model:** Gradient Boosting — highest balance of accuracy, F1 score, and recall.  
- **Recall (0.96):** Extremely effective at identifying customers who would **repay loans**.  
- Logistic Regression also performed well, especially on recall.  

---

## ✅ Conclusion  
This project demonstrated that combining borrower demographics, loan performance, and repayment history with **machine learning** can significantly improve loan default prediction.  

Key Insights:  
- Advanced **ensemble models** provide superior predictive power compared to traditional methods.  
- **Gradient Boosting** stood out as the hero, offering banks a reliable shield against financial risks.  
- By adopting this model, institutions can:  
  - Reduce defaults.  
  - Safeguard profitability.  
  - Extend fairer credit access.  




