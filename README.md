# Customer Churn Prediction (Python, scikit-learn)

Predicts which telecom customers are likely to churn, using the Telco Customer Churn dataset from Kaggle (7,032 customers after cleaning).

## Tools
Python, pandas, matplotlib, seaborn, scikit-learn, Google Colab

## Steps
1. Cleaned the data (fixed TotalCharges, removed 11 blank rows, dropped customerID)
2. Explored churn by contract, tenure, internet service and payment method
3. One-hot encoded categorical columns and scaled numeric ones
4. Trained Logistic Regression, Random Forest and a class-balanced Logistic Regression

## Results (churn class)
| Model | Accuracy | Precision | Recall | F1 |
|---|---|---|---|---|
| Logistic Regression | 0.80 | 0.65 | 0.57 | 0.61 |
| Random Forest | 0.79 | 0.62 | 0.51 | 0.56 |
| Logistic Regression (balanced) | 0.73 | 0.49 | 0.79 | 0.61 |

The balanced model is the final choice because missing a churner costs more than a false alarm. It catches 297 of 374 churners.

## Key Insights
- Overall churn rate is 26.6%.
- Higher churn: fiber optic internet, electronic check payment, month-to-month contracts, short tenure.
- Lower churn: one- and two-year contracts, longer tenure.

## Recommendations
- Offer incentives to move month-to-month customers to longer contracts.
- Investigate fiber optic service quality and pricing.
- Target retention offers at customers in their first months.

## Dataset
Telco Customer Churn (Kaggle, by BlastChar)
