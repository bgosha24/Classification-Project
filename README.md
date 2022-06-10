# Classification-Project

In this project I tried out the Titanic competition on Kaggle. My first submission was able to predict survivors with a 75% accuracy which is surprisingly only within the top 85% of results. After playing around with GridSearch and classifiers other than just Logistic Regression I was able to pump up that number to a 77% accuracy and get into the top 60% of all submissions. Even copying the best parameters for the best model for a top 2% performer on the leaderboard for this competition only increased my model's performance to 77.99%. This made me reconsider how big the difference in classifying power is between models.

Lessons learned:

- Having a clean dataset with thoughtful feature engineering is more important than optimizing models as it yields a larger jump in performance. I tried to use cross_val_score to find models that perform best on this dataset and despite trying lots of different param combinations with GridSearchCV I was only able to get a 2% increase.

- 
