# Introduction: 

      In this project, we were building the ML models to practise so-called NLP for sentiment analysis of the popular service called Alexa which is virtual assistant technology by Amazon. 
      We will train ML models to predict whether the review is positive or negative and try to find insights to find out which factors can possibly influence the overall user's experience of using the Amazon Alexa service.


# Objectives: 

    Our goals:

        1. To find insights in the reviews of the users
    
        2. To develop a Deep Learning model that predicts whether the feedback is a positive or negative one


#  Description:  

    1. Type of problem: classification.

    2. Variables: 1 Numerical, 3 Categorical:

          1. rating: the amount of stars in rating (1 - 5)
  
          2. date: the date of the review
  
          3. variation: types of Amazon Alexa models and configuration
  
          4. verified_reviews: the text review of the users

    3. Target: feedback (INT):

          1. feedback : 0 - negative; 1 - positive

    4. Steps we made

          1. Importing a dataset
  
          2. EDA
  
          3. Feature engineering
          
                1. Drop unnecessary variables
    
                2. Encoding variations:          
    
                3. Train/test split:
    
                    > Train - 3 years
    
                    > Test - 2 years 
    
                4. Encoding verified reviews:
    
                    > CountVectorizer
    
                4. Balancing Dataset
    
                5. Training ML models
    
                6. fine-tuning hyperparameters
    
                    > RandomizedSearchCV
    
                5. Model evaluation and results analysis

    5. ML Algorithms we used:

            1. Logistic regression
         
            2. RandomForest

            3. SVC

            4. XGB

            5. GradientBoosting

            6. Naivebayes

            7. DecistionTree

            8. KNeighbors

    6. Evaluation metrics we used:

        1. F1 score

        2. Roc-auc 

        3. Confusion Matrix  

        4. Precision

        5. Recall

        6. Accuracy

# Conclusion

##  Data Analysis

    After completing the data analysis step, we found several insights. 

        1. We got the not balanced dataset

        2. All reviews in the dataset were done in 2018 year

        3. More than 90% of all reviews were written in July

        4. 75% of all reviews were made on 28, 29 and 30th day which is the end of the month, but there were a really little amount of reviews on the 31st days of each month. We assume that is just because not every month has a 31st day in it 

        5. The majority of all reviews were made at the beginning (Monday) and the end (Saturday, Sunday) of the week.

        6. more than 70% of the dataset consists of 5 star ratings which means that the majority of reviews were on the positive side.

        7. Black Dot is the most popular variation among all others

        8. The Black Dot and Charcoal variations are receiving higher ratings compared to others

        9. Black Dot variation also has the biggest amount of low ratings (1, 2, 3 stars).

        10.Black Dot, Charcoal Fabric and Configuration: Fire TV Stick are three variations with the biggest amount of positive feedback.

        11.Black Dot, Black and Black Spot are getting more negative feedback compared to others

        12.If the product has rating 1 or 2 it will be the negative feedback, on the other hand, if the rating is equal or more than 3 stars, it will probably be the positive feedback

        13.There are no null values in the dataset.

        14.Love, Thing, Music are one of the frequently used words in the positive feedbacks

        15.Siri, product, terrible are one of the frequently used words in the negative feedbacks

        

   ## Training & Evaluating ANN

   

     > Because we are working with NLP, we need to encode Variations and Verified_reviews

     > We have tested 8 popular models with the same data and same preprocessing steps to then compare them and choose only fixed amounts to tune the hyperparameters. 

     > After testing 8 models, we chose only 3 best models according to the accuracy metrics 

     > Then, we used cross-validation and started to fine-tune hyperparameters to boost the performance 

     > lastly, We have evaluated the models we built using several metrics including: 

           1. F1 score
  
           2. Roc-auc 
  
           3. Confusion Matrix 
  
           4. Precision
  
           5. Recall 
  
           6. Accuracy

         

    By analyzing all metrics we can tell that: 

        1.It seems that the overall performance of the models is higher for the not-balanced dataset

        2.We need to tune hyperparameters for the models in this project, because after finetuning of hyperparameters by RandomSearchCV the overall performance and accuracy has raised compared to the models without tuned hyperparameters

        3.We assume that XGBoostClassifier is the best choice here, because it shows both high and stable performance regarding Accuracy, Recall, Precision and ROC-AUC.

        

       

   # THANKS!!! :)
