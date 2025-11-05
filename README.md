# premier-league-prediction
Predicting Premier League match outcomes using machine learning and deep learning models

# Premier League Match Outcome Prediction

This project predicts match outcomes (Home Win / Draw / Away Win) using Machine Learning and Deep Learning models.  
Developed as part of my undergraduate research at CUHK (2024).

---

## Abstract
Predicting Premier League match outcomes is a critical area in sports analytics, with significant applications in team strategy, betting markets, and fan engagement. This paper provides a comparative study of four approaches (Random Forest, XGBoost, an ensemble of both (RF+XGB), and a Simple Recurrent Neural Network (RNN)) using data obtained from Kaggle([1]). The original dataset contained only Season_End_Year, Wk, Date, Home, HomeGoals, AwayGoals, Away, and FTR (final time result). Through feature engineering, I derived additional columns such as Home_Last_Season_Rank, Away_Last_Season_Rank, Home_Avg_Goals_Scored_Prev_Season, Home_Avg_Goals_Conceded_Prev_Season, Away_Avg_Goals_Scored_Prev_Season, Away_Avg_Goals_Conceded_Prev_Season, Home_CumulativePoints, Away_CumulativePoints, Home_Rolling_Avg, Away_Rolling_Avg, and a Target_Team perspective for binary labeling. Hyperparameter tuning was performed via grid search, and I transformed the static inputs into sequences of length five for the RNN. Our experiments indicate that XGBoost achieves the highest accuracy (66%), while Random Forest and the Ensemble model follow closely. The RNN performance is slightly lower (62%), suggesting that advanced architectures or imbalance remedies might be required to improve minority-class recall. These results highlight the benefits of extensive feature engineering yet show that more robust methods are needed to further enhance predictive accuracy.

---

## Overview
- Dataset: Kaggle-based Premier League match results (2010–2023)
- Models: Random Forest, XGBoost, RF+XGB Ensemble, Simple RNN
- Feature Engineering: team form, cumulative points, rolling averages, rank differences
- Accuracy: XGBoost (66%), RF (64%), RNN (62%)

---

## Requirements
pandas
numpy
scikit-learn
xgboost
tensorflow
matplotlib

---

## How to Run
1. Clone the repo  
   `git clone https://github.com/soomorita/premier-league-prediction.git`
2. Open `notebook/match_prediction.ipynb` in Jupyter or Google Colab
3. Run all cells

---

## References
1. Kaggle. *Premier League Matches Dataset.* Retrieved 2024/12/9, from  
https://www.kaggle.com/datasets/evangower/premier-league-matches-19922022

---

## Author
Soya Morita  
The Chinese University of Hong Kong (2024)  
[GitHub](https://github.com/soomorita)
