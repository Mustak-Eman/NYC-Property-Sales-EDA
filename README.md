# NYC-Property-Sales

This repository contains my NYC Property Sales data science project for coursework at **Lehman College**.  
It includes **data cleaning, exploratory data analysis (EDA), regression modeling, classification, and hypothesis testing** using Python.

## Project Overview
Using the NYC Property Sales dataset, I explored how property characteristics (square footage, units, year built, and location) relate to **sale prices**.  
The work is organized as milestone-style sections in the notebook.

## What I Did (Methods)
- **Data cleaning & preprocessing**
  - Filtered invalid / missing values (ex: sale_price > 0)
  - Applied **log transforms** to reduce skew for heavy-tailed features
- **EDA + Visualization**
  - Histograms, scatterplots, and relationship plots (Seaborn/Matplotlib)
- **Regression (predicting sale price)**
  - Built regression models to predict numeric sale prices
  - Tuned a **Random Forest Regressor** using different `max_depth` and `n_estimators`
- **Classification (price category prediction)**
  - Converted sale_price into **Low / Mid / High** categories (quantiles)
  - Trained a **KNN classifier**
  - Tuned k and plotted **Accuracy vs k**
  - Improved results by adding **borough (one-hot encoded)** as a location feature
- **Permutation Test (hypothesis testing)**
  - Used a **permutation test** to test whether two boroughs have different typical sale prices
  - Test statistic used: **absolute difference in median log1p(sale_price)**

## Key Results (Highlights)
- **Random Forest Regression:** best model achieved about **R² ≈ 0.51** (explained ~51% of variance in sale prices).
- **KNN Classification:**
  - Without borough: best accuracy ≈ **51.1%**
  - With borough: best accuracy ≈ **57.7%** (**+6.6 percentage points**), showing location is a strong predictor.
- **Permutation Test:** the observed statistic was far beyond the null distribution, so we **reject the null hypothesis** that the two boroughs have the same typical sale prices.

> Note: In the dataset, borough may be coded numerically (1–5).  
> Common mapping: 1=Manhattan, 2=Bronx, 3=Brooklyn, 4=Queens, 5=Staten Island.

## Contents
- `Milestone_1.ipynb` (or `NYC_Property_Sales.ipynb`) — main notebook with all code, plots, and analysis
- `nyc-rolling-sales.csv` — dataset used in the notebook
- `README.md` — project overview

## How to Run
1. Open the notebook in **Google Colab** or Jupyter.
2. Make sure the dataset file (CSV) is in the same folder (or update the file path in the notebook).
3. Run cells from top to bottom.

## Links
- 🔗 Project Webpage (Google Sites): **[Add your published link here]**
- 💻 Open in Colab: **[(https://colab.research.google.com/drive/1ZhIsGQgMQYwLHBKH2n7phu8N9lDlGYlQ?usp=sharing)]**
