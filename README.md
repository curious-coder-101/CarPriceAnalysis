# What Drives the Price of a Used Car?

## Overview
This project analyzes a dataset of 426,000 used car listings to identify the key factors that influence pricing. The analysis was conducted for a used car dealership looking to optimize their inventory decisions. The project follows the **CRISP-DM** framework.

## Dataset
Source: [Kaggle - Craigslist Used Cars Dataset](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data)

## Key Findings
- **Vehicle age and mileage** are the strongest price drivers — newer, lower-mileage cars command significantly higher prices.
- **Luxury/performance brands** (Ferrari, Tesla, Porsche) hold their value far better than economy brands (Fiat, Mitsubishi, Kia).
- **Diesel vehicles** command a ~$13,000 premium over other fuel types.
- **Trucks and SUV brands** (Ram, GMC, Jeep, Ford) have the highest median prices among high-volume manufacturers.
- **Vehicle condition** has a meaningful impact — cars in "new" condition fetch a notable premium.

## Recommendations for Dealerships
1. Prioritize acquiring **low-mileage, newer vehicles** for the highest resale value.
2. Stock more **trucks, SUVs, and diesel vehicles** — they hold value best.
3. Invest in **premium brands** like Tesla, Porsche, and Lexus.
4. Avoid overinvesting in **economy brands** that depreciate faster.
5. **Recondition vehicles** before listing — improved condition significantly boosts price.

## Modeling Summary
Three regression models were evaluated using 5-fold cross-validation:

| Model | CV RMSE | Details |
|-------|---------|---------|
| Linear Regression | $7,639 | Baseline model |
| Ridge Regression | $7,639 | Best alpha = 1 |
| Lasso Regression | $7,594 | Best alpha = 1 (best model) |

The best model (Lasso) achieved a **test RMSE of $7,646** and **R² of 0.66**, explaining 66% of the variance in used car prices.

## Notebook
[View the Jupyter Notebook](./car_price_analysis.ipynb)

## Tools & Libraries
- Python, Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn (LinearRegression, Ridge, Lasso, GridSearchCV, Cross-Validation)
