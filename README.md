# Fraud Watch Dashboard 🔍

An AI-powered transaction fraud monitoring solution built for the OptimusAI Hackathon.

## Problem
Banks and fintechs face fraud risks across mobile money transfers, 
cards, POS, and digital wallets. Fraud teams need tools to detect 
suspicious patterns quickly and take action.

## Solution
Fraud Watch Dashboard helps fraud/risk analysts:
- View and search transaction records
- See AI-generated fraud risk scores
- Understand *why* a transaction was flagged
- Receive recommended next steps for investigation

## Dataset
- Source: PaySim Synthetic Financial Dataset (Kaggle)
- Link: https://www.kaggle.com/datasets/ealaxi/paysim1
- 6.3 million synthetic mobile money transactions
- Fraud rate: 0.13% (8,213 fraud cases)

## Project Structure
- fraud-watch-dashboard/
- data/         ← dataset collection file and data notes
- notebooks/    ← data prep, model training, evaluation
- app/          ← dashboard application code
- README.md
## Tech Stack
- Python, Pandas, Scikit-learn
- Streamlit (dashboard)
- Openrouter API (LLM explanation layer)

## How to Run
Coming soon.

## Responsible AI
This tool supports human decision-making only. 
It does not automatically block accounts or make 
final fraud decisions. All flags require human review.