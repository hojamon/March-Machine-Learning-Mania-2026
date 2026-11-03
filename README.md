# March Machine Learning Mania 2026

Solution for the Kaggle competition [March Machine Learning Mania 2026](https://www.kaggle.com/competitions/march-machine-learning-mania-2026).
The task is to predict win probabilities for the NCAA basketball tournaments (men's and women's).

## Result

🥉 **Bronze Medal**: Rank 181 / 3,462 teams 

## Solution Overview

- **Features:** season stats, opponent-adjusted stats, momentum over the last 10 games, Elo ratings, strength of schedule, conference strength, historical win rates by seed matchup, and Massey Ordinals (men's only)
- **Models:** ensemble of Logistic Regression / GBM / XGBoost / LightGBM, trained separately for men and women
- **Season weighting:** recent seasons weighted more heavily (decay = 0.97)
- **Calibration:** probabilities calibrated with goto_conversion
