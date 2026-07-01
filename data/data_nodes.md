# Data Notes — PaySim Fraud Detection

## Source
- Dataset: Synthetic Financial Datasets For Fraud Detection
- Author: Edgar Lopez-Rojas
- URL: https://www.kaggle.com/datasets/ealaxi/paysim1
- License: CC BY-SA 4.0

## Why It Fits
PaySim simulates mobile money fraud — account takeover,
emptying funds via TRANSFER then CASH_OUT. Directly matches
Use Case 1 (Transaction Fraud Monitoring).

## Dataset Overview
- Rows: 6,362,620
- Columns: 11
- Missing values: None
- Simulation period: 744 steps (1 step = 1 hour = 30 days)

## Class Imbalance
- Non-fraud: 6,354,407 (99.87%)
- Fraud: 8,213 (0.13%)
- Heavily imbalanced — model must account for this

## Transaction Types
- CASH_OUT: 35%
- PAYMENT: 34%
- CASH_IN: 22%
- TRANSFER: 8%
- DEBIT: 1%
- Fraud ONLY occurs in TRANSFER and CASH_OUT types

## Columns Excluded as Features
- oldbalanceOrg, newbalanceOrig, oldbalanceDest, newbalanceDest
- These leak the fraud label since fraudulent transactions
  get cancelled, causing balance anomalies that aren't
  real predictive signals

## Columns Used as Features
- step, type, amount, isFlaggedFraud

## Assumptions
- Dataset represents African mobile money patterns
- Scaled to 1/4 of original logs
- Synthetic data mirrors real fraud behaviour patterns

## Limitations
- Synthetic — may not capture all real-world fraud patterns
- No demographic or device data available
- Class imbalance requires careful handling

## Bias/Data Quality Risks
- Fraud patterns are simplified vs real-world complexity
- Only one fraud type represented (account takeover)
- Results may not generalise to all real-world fraud scenarios