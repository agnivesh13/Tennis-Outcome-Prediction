# 🎾 Tennis Match Outcome Prediction System

A machine learning project to predict the outcomes of professional men’s tennis matches using historical data, Elo rating systems, and classification models.

## 📌 Project Summary

This project aims to forecast match winners in ATP tennis using a combination of:
- Elo rating models (for relative player skill)
- Engineered features (head-to-head stats, recent form, serve metrics)
- Machine Learning classifiers (Logistic Regression, Random Forest)

## 📂 Dataset

- **File:** `Combined_Tennis_Data_1.csv`
- **Size:** ~96,000 ATP matches (1990–2024)
- **Features:** Match metadata, winner/loser IDs, seeds, ranks, player ages, performance stats (aces, double faults, break points, etc.)

## 🔧 Features Engineered

- Head-to-Head (overall and surface-specific)
- Last-N win streaks (N ∈ {3,5,10,25,100})
- Past-N serve performance (e.g. aces, double faults)
- Elo rating difference (with tuned K-factor)

## ⚙️ Models Trained

| Model                  | Accuracy | AUC  |
|------------------------|----------|------|
| Elo-only (K=25)        | 60%      | 0.65 |
| Logistic Regression    | 67%      | 0.73 |
| Random Forest          | 72%      | 0.78 |
| Random Forest + Elo    | **74%**  | **0.80** |

## 🧪 Evaluation

- Accuracy, AUC, Log-loss
- Probability calibration (Brier score)
- Feature importance from Random Forest
- Elo K-factor tuning via cross-validation

## 📊 Visualizations

- Accuracy vs K-factor curve for Elo-only model
- Calibration curve and feature importance plots (see notebooks)

## 🛠️ Tech Stack

- Python 3.11+
- Jupyter Notebook
- pandas, numpy, scikit-learn, matplotlib, seaborn

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/agnivesh13/tennis-outcome-prediction.git
   cd tennis-outcome-prediction

Install dependencies:

```bash
pip install -r requirements.txt
```
Run the notebook:
Open Tennis_Outcome_Prediction_Model.ipynb in Jupyter Lab/Notebook and run the cells sequentially.

📈 Future Work
Integrate live match updates with Elo re-computation

Add betting odds as features

Explore deep learning models (RNNs, LSTMs)

Build interactive dashboard for match predictions
