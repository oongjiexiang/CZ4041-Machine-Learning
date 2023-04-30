# CZ4041-Machine-Learning

This repository contains the code that generates the final prediction output to submit to [Kaggle Elo Merchant Recommendation competition](https://www.kaggle.com/competitions/elo-merchant-category-recommendation/) as the project for Nanyang Technological University's (NTU) Machine Learning (CZ4041) course. 5 members (GitHub repo collaborators) worked on this 14-week project.

# Summary
Elo competition is a regression problem that aims to predict the loyalty score of a card based on the card's merchants and its purchase details, and evaluates on RMSE score. However, it has 4 significant challenges:
1. Feature are anonymised, making feature engineering difficult to be interpreted
2. Inconsistency due to stochasticity of splitting the dataset. Despite K-Fold Cross Validation method, the attainable RMSE score spans a wide range, so the best model on the validation set may perform worse in Kaggle Private Leaderboard
3. Overly imbalanced data: 1.1% train data have loyalty scores about -30, instead of the others that normally center at 0
4. Huge raw feature list, but the features require aggregation so that the prediction of the `test.csv` file has the same number of rows as the intended output format (i.e. loyalty scores of all the test `card_id`s are predicted). Some test rows also have null values.

To address these challenges, strategies adopted in the pre-machine learning phase are as follows:
- Preprocessing: imputation with mode, investigating data correlation
- Feature engineering: 

# How to Read this Repo

