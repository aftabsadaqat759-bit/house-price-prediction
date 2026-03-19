
# House Price Prediction Model

## Project Overview
An end-to-end regression system that predicts house prices based on key features including median income, room count, and house age.

## Problem Statement
Predict house prices accurately using available features to support real estate decisions.

## Dataset
- Source: California Housing Dataset
- Samples: 20,640 houses
- Features: 8 features + target price
- Target: Median house price (in dollars)

## Methodology
1. Data Cleaning: Handled 5,594 outliers using IQR method
2. EDA: Comprehensive visualization analysis (8+ plots)
3. Feature Selection: Selected top 3 features based on correlation
4. Feature Scaling: StandardScaler for normalization
5. Model: Linear Regression with train-test split (80-20)
6. Validation: 5-fold cross-validation

## Model Performance
| Metric | Value | Interpretation |
|--------|-------|----------------|
| R² Score | 0.5200 | Explains 52.0% of price variance |
| MAE | $58,482.14 | Average prediction error |
| RMSE | $77,905.62 | Typical prediction error |
| MAPE | 35.75% | Average percentage error |
| CV Mean R² | 0.4990 | Cross-validation average |

## Key Insights
- Median Income: Most important feature (+$97,350 per std dev)
- House Age: Older homes add value (+$20,094 per std dev)
- Room Count: Negative impact (-$24,455 per std dev) - suggests need for better room quality metrics
- Residuals: Centered at zero with slight positive skew
- Model Stability: Cross-validation shows consistent performance (std = 0.0536)

## Technologies Used
- Python (Pandas, NumPy)
- Scikit-learn (Linear Regression, preprocessing, cross-validation)
- Matplotlib & Seaborn (Visualization)
- Jupyter Notebook

## Repository Structure
├── data/               # Raw and cleaned datasets
├── models/             # Saved model files
├── notebooks/          # Jupyter notebook with complete analysis
├── visualizations/     # All plots (9+ visualizations)
└── README.md          # Project documentation

## How to Run
1. Clone repository
2. Install requirements: pip install -r requirements.txt
3. Run notebook: jupyter notebook notebooks/house_price_prediction.ipynb

## Future Improvements
- Add location features (latitude/longitude)
- Try non-linear models (Random Forest, XGBoost)
- Include square footage data
- Deploy as web application using Flask/Streamlit

---
Developed as part of Machine Learning & Data Science portfolio
