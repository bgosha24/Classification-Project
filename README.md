# Classification-Project

Summary

In this project I tried out the Titanic competition on Kaggle. My first submission was able to predict survivors with a 75% accuracy which is surprisingly only within the top 85% of results. After playing around with GridSearch and classifiers other than just Logistic Regression I was able to pump up that number to a 77% accuracy and get into the top 60% of all submissions. I was quite unsatisfied with these results and tossed it up to my lack of model tuning expertise. However, even after copying the parameters of a top 2% performer on the leaderboard (83% accuracy) my model's performance only increased to 77.99%. This made me reconsider how big the difference in classifying power is between models and that maybe I need to look at other optimization options.

After reconsidering some features of the dataset I decided to make some changes in my approach to feature engineering. Instead of dropping columns I decided to try to either fill or create new features that would replace them.


Lessons learned:

- Having a clean dataset with thoughtful feature engineering is more important than optimizing models as it yields a larger jump in performance. I tried to use cross_val_score to find models that perform best on this dataset and despite trying lots of different param combinations with GridSearchCV I was only able to get a 2% increase which may take me from the 85th percentile to the 25th on the leaderboard, but definitely doesn't do much for my ability to predict survivors on the Titanic.

- If a feature seems to be useless or too hard to interpret, it is best to break it up into digestible features. This was the case for me when I changed the Cabin feature into cabin_adv which is cabin letters and cabin_multiple which signifies a passenger with multiple cabins.

- Some features are meant to be paired up as they are heavily correlated. The Sibling/Spouse and Parent/Child features were combined to give room to 2 new features named FamilySize and Alone

- Some numerical features could be used to create categorical features. I used age to determine if a passenger was a child (15 and younger) or an adult.

- Don't rush into model selection and instead explore the dataset and see how you can make it as easy as possible for model to digest.

