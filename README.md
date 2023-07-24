# The Models<br>
I will explain how each algorithm works in short after all the results.
<h2>Multinomial Naive Bayes:</h2> <br>
Used a dataset containing 2 columns: 'message' and 'sentiment' where the 'message' column contains text messages and the 'sentiment' column contains it's sentiment, so either 'positive', 'negative' or 'neutral'<br>
The dataset's size is somewhere around 500 rows.<br><br>
Preprocessing the dataset before-hand with whitespace, links and special characters removal, the text was lower-cased.<br>
I have also added part of speech tags, with no influence on the model whatsoever (possible reason is the fact that Naive Bayes does not work well with strongly related values as explained in the algorithms explanation section) <br><br>
<h4>Results:</h4>
Now I have used the preprocessed dataset for Sentiment Analysis and the results are as follows: <br><br>
Positive sentiment detection: 45 / 51 <br>
Negative sentiment detection: 19 / 50 <br>
Neutral sentiment detection: 13 / 30 <br>

So the model is great at detecting Positive sentiment but not so great at detecting the rest. Posible cause could be the dataset's size being too small.

<h4>Metrics: </h4>
Accuracy of the split model: 0.818 <br>
Accuracy of the full model: 0.971 <br>
Mean Squared Error of the split model: 0.648 <br>
Mean Squared Error of the full model: 0.25 <br>
Mean Absolute Error of the split model: 0.261 <br>
Mean Absolute Error of the full model: 0.039 <br>

<h2>Linear Regression and Decision Tree Classifier:</h2> <br>
For this code I used a wine quality dataset that contains 12 columns<br>
Using a correlaton matrix, the strongest interactions are between:<br>
- Fixed acidity with density and citric acid<br>
- Free sulfur dioxide with total sulfur dioxide<br>
Used Linear Regression to predict the PH levels. <br>
Used DTC to predict the quality. <br>
<h4>Results:</h4>
By inputting all components, quality can be predicted using the Decision Tree Classifier model, for example: <br>
wine_qt = [[7.2, 0.3, 0.3, 2.1, 0.065, 8, 18, 0.996, 3.2, 0.6, 9.5]] <br>
quality=clf.predict(wine_qt)<br>
The predicted Quality using the Decision Tree Classifier is:  [5]<br><br>
'fixed acidity','volatile acidity' and 'residual sugar' can be inputted to predict the pH level using the Linear Regression model, for example: <br>
wine_ph=[[7.5, 0.5, 0.2]] <br>
phlevel=model.predict(wine_ph) <br>
The predicted PH using the Linear Regression model is:  [3.35933173] <br>
<h4>Metrics:</h4> 
Mean Squared Error:  0.0 <br>
Mean Absolute Error:  0.0 <br>
Accuracy:  1.0 <br>

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
Mean absolute error of the model is around 800k while the cheapest house is 1.75M and the most expensive one is 13.3M<br><br>



# A basic explaination of how the algorithms work<br>
<h3>How Naive Bayes' algorithm works: </h3> <br>
The multinomial Naive Bayes is a simple probabilistic classifier that applies Bayes' theorem.<br>
Naive stands for the assumption of features being independent from each other.<br>  
It uses the multinomial distribution (e.g. estimating the probability of a given set of outcomes occuring).<br>  
To further explain the multinomial concept: it could be used to show the results of rolling a dice (6 possible outcomes), in contrast, a coin has 2 which implies a binomial distribution.<br>
While the example above still holds true, in a multinomial distribution the outcomes represent frequencies of events rather than single occurrences.<br><br>

<h4>The Bayes' theorem:</h4>
Is based on the probability of a hypothesis, given the data and some prior knowledge.<br>

A simple explanation:<br>
The probability of a baby having a certain eye color based on the parents' eye colors.<br>

Ultimately, the algorithm is best used when the features are NOT strongly dependent of eachother or when there are NO complex relationships between the features and target variable. <br>

Suitable for:<br>
- Simple to moderate complexity datasets.<br>

Best used for:<br>
- Text classification tasks (NLP, spam classification, sentiment analysis...)<br>


<h4>Gaussian Naive Bayes:</h4>
Best used for:<br>
- Classification tasks, where the features are continuous and can be modeled by a gaussian distribution (normally distributed features).<br>
- Numeric sensor readings, measurements...<br>

