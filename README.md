# House Price Prediction - Ridge & Lasso Regression

> Predicting Australian house prices using regularized regression models for Surprise Housing's market entry strategy.

## Business Problem

Build a regression model to predict house prices in Australia, helping Surprise Housing identify undervalued properties for profitable investment.

**Key Objectives:**

- Identify significant variables in predicting house prices
- Determine optimal lambda (alpha) values for Ridge and Lasso regression
- Enable data-driven property investment decisions

## Dataset

- **Source:** Australian housing market data (`train.csv`)
- **Records:** 1,460 houses with 81 features
- **Target:** SalePrice (in dollars)
- **Features:** Property characteristics, quality ratings, location, amenities, age, etc.


## Results

| Model             | Test R² | Test RMSE | Alpha | Features   |
| ----------------- | ------- | --------- | ----- | ---------- |
| Linear Regression | 0.034   | $82,097   | N/A   | 269 (all)  |
| Ridge Regression  | 0.861   | $31,201   | 500   | 269 (all)  |
| Lasso Regression  | 0.846   | $32,802   | 100   | 209 (auto) |

### Top 5 Predictors (Lasso)

1. PoolArea ($85,371)
2. HasPool (-$72,222)
3. PoolQC_Gd (-$23,000)
4. TotalSF ($16,186)
5. OverallQual ($10,948)

### Recommendation

**Ridge Regression** - Best overall performance (R²=0.861) with stable predictions across all features.

## Technologies Used

- **Python:** 3.12.8
- **Jupyter Notebook:** Latest
- **Libraries:**
  - **NumPy:** 2.4.1
  - **Pandas:** 2.3.3
  - **Matplotlib:** 3.10.8
  - **Seaborn:** 0.13.2
  - **Scikit-learn:** 1.8.0
  - **SciPy:** 1.17.0

## Repository Structure

```
AssignmentDataAnalytics/
├── train.csv                        # Dataset
├── data_description.txt             # Feature descriptions
├── house_price_prediction.ipynb    # Main analysis notebook
├── Subjective_Answers.pdf           # Assignment answers
├── README.md                        # This file
└── output/                          # Generated results
    ├── model_comparison.csv
    ├── lasso_feature_importance.csv
    └── ridge_feature_importance.csv
```

## Quick Start

```bash
# Install dependencies
pip install numpy pandas matplotlib seaborn scikit-learn scipy jupyter

# Run analysis
jupyter notebook house_price_prediction.ipynb
```


## Contact

Created by [@PrangyaPradhan](https://github.com/pprangya) - Feel free to reach out!

---
