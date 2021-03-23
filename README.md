# nfl-scores-and-betting-models
Using SVM and XGBoost Classification models to predict NFL mid-season Moneyline bets.

Using NFL season data for the previous 5 years, I built classification models to predict the probability of which team will win or lose.
- The model performs slightly better on choosing losers.
- The model was designed for mid-season, weeks 3-15 as they tend to have more consistent strategy.

Inputs needed for the completed model: Teams playing, Home Team, Spread, and the average points scored for the home and separately, the away team.

The results of the XGBoost Model are - 
train score: 0.824
test score: 0.800

The results of the SVM model are -
train score: 0.89
test score: 0.77

As the XGBoost model has a slightly better fitting, I proceeded to pickle this model.  

I then ran .predict_proba to have the ability to filter for higher confidence predictions. 
- When filtering to a 20% threshold of the prediction there is a boost in accuracy to 89% for win, and 95% for loss prediction. 
- Note that only certain games in a week will meet this threshold.  This tool has not been tested in season with bets, but could be a useful tool with some more tuning. 
