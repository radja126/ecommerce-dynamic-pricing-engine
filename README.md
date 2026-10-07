# E-Commerce Dynamic Pricing & Demand Elasticity Engine

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange.svg)](https://scikit-learn.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

An end-to-end Machine Learning pipeline and price elasticity simulation designed to predict product demand and optimize pricing strategies for maximum revenue in an e-commerce ecosystem.

---

## Executive Summary

Pricing decisions in e-commerce are heavily influenced by competitor behavior, seasonality, and shipping costs. This project builds a predictive regression engine using **Gradient Boosting** to forecast sales volume (`qty`) and simulates dynamic price adjustments (-20% to +20%) to identify optimal price points that maximize overall revenue.

---

## Key Features & Workflow

1. **Exploratory Data Analysis (EDA):** Analyzed multi-category e-commerce transactions, identifying strong negative elasticity between unit price / freight price and demand.
2. **Advanced Feature Engineering:** Formulated domain-specific interaction features:
   * **Competitor Price Ratio & Difference:** Relative pricing against competitor averages.
   * **Freight Ratio:** Shipping cost sensitivity relative to unit price.
   * **Price Change Dynamics:** Percentage change relative to lag prices.
3. **Robust Preprocessing Pipeline:** Built `ColumnTransformer` with `StandardScaler` and `OneHotEncoder` to eliminate data leakage.
4. **Hyperparameter Tuning:** Optimized `GradientBoostingRegressor` via `GridSearchCV` ($R^2 = 0.42$, $MAE = 7.15$).
5. **Dynamic Price Optimization Engine:** Simulated price elasticity scenarios to identify revenue-maximizing price points.

---

## Tech Stack
Language: Python

Data Processing: Pandas, NumPy

Machine Learning: Scikit-Learn (Gradient Boosting, GridSearch)

Visualization: Matplotlib, Seaborn

---

## Business Impact & Simulation Results

In a sample scenario, the elasticity simulation recommended increasing a product's price from **$19.99** to **$21.99 (+10%)**, resulting in an estimated revenue increase from **$301.38** to **$375.46 (+24.5%)**.

---

## Project Structure

```text
├── retail_price.csv          # E-Commerce dataset
├── dynamic_pricing.ipynb     # Jupyter Notebook with full analysis & code
├── feature_importance.png    # Top 10 Feature Importance plot
├── .gitignore                # Git ignore rules
└── README.md                 # Project documentation