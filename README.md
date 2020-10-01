# Titanic
 The required Titanic Project you have to do before they can call you a Data Scientist.
 
 In all seriousness, I've wanted to enter a kaggle competition for a long time and this seemed like a great place to start.
 
 ## Project Overview:
 - Achieved 78% accuracy on the testing set. It's difficult to know how good this is as the leaderboard is filled with people with 100% accuracy/overfit models.  
 - Data was acquired from the ongoing kaggle competition [here.](https://www.kaggle.com/c/titanic/data)
 - Extensive EDA and feature engineering. 
 - Use of Logistic Regression, Gradient Boosting, and Support Vector Clustering.
 - Hyperparameter optimization with GridSearchCV and RandomizedSearchCV.
 - Exploration of Feature Importances
 - Model stacking ensemble method. 
 - Hot takes on James Cameron Movies.
 
 ## Code and Resources Used:
 - **Python Version:** 3.7
 - **Packages:** pandas, numpy, sklearn, matplotlib, seaborn, lightgbm, [mlxtend](http://rasbt.github.io/mlxtend/)  
 - [Ken Jee's Youtube Video  about the Titanic Dataset](https://www.youtube.com/watch?v=I3FBJdiExcg)
 
 ## Features:
- **'survival':** 0 = No, 1 = Yes. This is our target feature.
- **'pclass':** Ticket class. 1 = 1st, 2 = 2nd, 3 = 3rd.
- **'sex':** Gender
- **'Age'** 
- **'sibsp':** # of siblings / spouses aboard the Titanic. 
- **'parch':** # of parents / children aboard the Titanic.  
- **'ticket':** Ticket number 
- **'fare':** Passenger fare 
- **'cabin':** Cabin number. 
- **'embarked':** Port of Embarkation: C = Cherbourg, France Q = Queenstown, Ireland S = Southampton, U.K..
 
 ## Data Cleaning:
 - Created "Family" feature by adding 'SibSp' and 'Parch'
 - Made "Alone" feature if person had no family onboard. 
 - Parsed the titles of people on board to create "Title" feature
 - Assigned titles to different groups
 - Made "numeric ticket" feature if ticket featured a number. 
 - Grouped cabins into "cabin group" feature. 
 - Filled missing 'Age' and 'Fare' values with medians.
 - Filled missing 'Embarked' values with the mode.
 
 
 ## EDA:
 Some highlights from EDA. There's a ton of it within the Jupyter notebook. 
 
 ## Model Building:
 First, I used one hot encoding on categorical features and scaled the numerical data. 
  
 I opted to use cross validation so that this model could generalize well--in case we ever need a model to predict other early 20th century shipwreck survivors.
  
 Models used:<br>
-**Logistic Regression** - I always like to use this as a baseline as long as the data cooperates. <br>
-**LightGBM Classifier** - I've gotten great results anytime I've used this in a classification problem, regardless of complexity. <br>
-**Support Vector Classifier** - I wanted to give this a shot after seeing Ken Jee use it on his project. <br>
 
 ## Model Performance:
 **<ins>Initial Runs on Training Set</ins>**<br>
 **LR:** 82.83%<br>
 **GB:** 82.83%<br>
 **SVC: 83.16%**<br>
 
 **<ins>After Hyperparameter Optimization</ins>**<br>
 **LR:** 83.05%<br>
 **GB: 84.62%**<br>
 **SVC:** 83.39%<br>
 
 Models were stacked together and the ensemble model scored **77.51%** on the testing set. 
 
 
 
 
