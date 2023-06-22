# Project-Luna<br>

I'm just testing some stuff, don't know if i will ever update this README.<br>
Goal: Create an A.I. with increasing complexity<br>
If I'm being realistic, this will never happen... hopefully along the way I will learn something.


UPDATE 05/06 

THERE IS NOTHING TO UPDATE. 
Did some 'research' though so yea, i'm a bit smarter now, for a short period ofc. I am reverting back to monke in due time.




UPDATE 07/06 

Done 2 models... wait, that sounds wrong, let me reformulate. I have done... I mean, I CREATED 2 models trained to predict the sentiment of a message. The models are done using XGBClassifier and MultinomialNB.
Now I shall attempt to dissappear...



UPDATE 11/06

What I have learned so far: 
- Preprocessing and checking the dataset first before using are very important steps.
- The complexity of a model has nothing to do with it's accuracy, in fact, sometimes a complex model performs worse than a simple one.
- In my case, the Multinomial Naive Bayes model was way easier to implement and test and it demanded less preprocessing, less computer resources and less time to run.
    The Accuracy Difference of the split models was 0.0113, meaning that MultinomialNB had a 0.0113 worse score in accuracy than XGBoost Classifier<br>
    Mean Squared Error Difference of the split models: -0.0555<br>
    Mean Absolute Error Difference of the split models: 0.0511<br>
    So basically, both models' analytics were similar
