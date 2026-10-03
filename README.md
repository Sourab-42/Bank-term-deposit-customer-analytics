# Bank Term Deposit Customer Analytics

Exploratory data analysis and a predictive model to understand which customers subscribe to a bank term deposit after a marketing campaign.

## Project Overview

- Cleaned and explored a dataset of **41,188 customer records** with 21 columns (demographics, contact details, campaign history and economic indicators).
- Analysed how age, job, call duration, contact method, month and number of contacts relate to subscription.
- Built a **Logistic Regression** model to predict subscription and identify high-potential customers.

The dataset follows the UCI Bank Marketing (`bank-additional-full`) format. About 11.3% of customers subscribed (4,640 "yes" vs 36,548 "no"), so the classes are imbalanced.

## Folder Structure

```
bank-term-deposit-customer-analytics
├── data
│   └── data.csv
├── notebooks
│   └── Advance_Bank_Term_Deposit.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

## Tech Stack

Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Jupyter Notebook

## Analysis Covered

1. Dataset overview and missing-value check
2. Customer demographics (age and job vs subscription)
3. Call duration vs subscription
4. Campaign effectiveness (contact method, month, number of contacts)
5. Correlation heatmap of numerical variables
6. Logistic Regression model with feature importance

## Model Results

Logistic Regression (80/20 stratified split, standardised features, `class_weight='balanced'`):

| Metric | Value |
|---|---|
| ROC-AUC | 0.9365 |
| Accuracy | 0.86 |
| Recall (subscribers) | 0.88 |
| Precision (subscribers) | 0.43 |

The model is tuned to catch most likely subscribers (high recall), at the cost of more false positives.

## Key Takeaways

- Customer demographics play a role in term deposit subscription.
- Longer calls are associated with more subscriptions.
- Contacting customers by cell phone works better than by telephone.
- How often customers are contacted affects campaign success.
- Logistic Regression can help identify customers likely to subscribe.

## How to Run

```bash
git clone <your-repo-url>
cd bank-term-deposit-customer-analytics

python -m venv venv
# Windows: venv\Scripts\activate
# macOS/Linux: source venv/bin/activate

pip install -r requirements.txt
jupyter notebook notebooks/Advance_Bank_Term_Deposit.ipynb
```

The notebook reads the data from `../data/data.csv`, so launch it from the repository as shown above.

## Author

**Sourab Sharma** - [LinkedIn](https://linkedin.com/in/sourab-sharma-1s)
