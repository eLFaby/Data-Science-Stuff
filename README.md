# Models<br>

<h2>Multinomial Naive Bayes:</h2> <br>
Used for Sentiment Analysis where: <br>
Positive sentiment detection: 45 / 51 <br>
Negative sentiment detection: 19 / 50 <br>
Neutral sentiment detection: 13 / 30 <br>

So the model is great at detecting Positive sentiment but not so great at detecting the rest. Posible cause could be the dataset since it contains only about 500 rows.


<h2>Linear Regression and Decision Tree Classifier:</h2> <br>
For this code I used a wine quality dataset<br>
Used Linear Regression to predict the PH levels <br>
Used DTC to predict the quality <br>

<h2>Random Forest Regressor</h2>
<h3>Does education correlate to a higher income?</h3> <br>
Mean Bachelor`s salary: 95177.0 <br>
Mean Master`s salary: 130112.0 <br>
Mean PhD salary: 165772.0 <br>
Mean High Schooler salary: 36707.0 <br>
The difference between a PhD and a High School student:  129065.0 <br>
<br>
<h3>What are the lowest and highest paid jobs?</h3><br>
The Lowest paid jobs are: Receptionist, Junior Sales Associate with a salary of 25000 <br>
The Highest paid jobs are: Chief Technology Officer, CEO, Financial Manager with a salary of 250000<br>
<br>
Created a Random Forest Regressor model that takes age, gender, education, years of experience as inputs and predicts a salary.<br>

<h2>XGBoost Regressor:</h2><br>
Used on a small housing prices dataset <br>
Mean absolute error of the model is around 800k while the cheapest house is 1.75M and the most expensive one is 13.3M