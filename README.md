# Heart-Disease-Prediction

Detailed explanation in the blog [priyanka.malladi.hashnode.dev](https://priyankamalladi.hashnode.dev/predicting-heart-disease-using-machine-learning-models-ck8459rcp04qlzns1esgi1k7r)

## Introduction

Heart disease is a term covering any disorder of the heart.
> One in every four deaths in the U.S. is related to heart disease. One person dies every 37 seconds in the United States from cardiovascular disease.

Machine learning can play an essential role in predicting Heart disease presence.

The **data** I used in this project is from the Cleveland database from  [UCI Machine Learning Repository. ](https://archive.ics.uci.edu/ml/datasets/Heart+Disease) 

## Problem Definition
Given clinical parameters about a patient, can we predict whether or not they have heart disease?

## Heart Disease Data Dictionary

The following are the features we'll use to predict our target variable (heart disease or no heart disease).

1. age - age in years 
2. sex - (1 = male; 0 = female) 
3. cp - chest pain type 
    * 0: Typical angina: chest pain related decrease blood supply to the heart
    * 1: Atypical angina: chest pain not related to heart
    * 2: Non-anginal pain: typically esophageal spasms (non heart related)
    * 3: Asymptomatic: chest pain not showing signs of disease
4. trestbps - resting blood pressure (in mm Hg on admission to the hospital)
    * anything above 130-140 is typically cause for concern
5. chol - serum cholestoral in mg/dl 
    * serum = LDL + HDL + .2 * triglycerides
    * above 200 is cause for concern
6. fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false) 
    * '>126' mg/dL signals diabetes
7. restecg - resting electrocardiographic results
    * 0: Nothing to note
    * 1: ST-T Wave abnormality
        - can range from mild symptoms to severe problems
        - signals non-normal heart beat
    * 2: Possible or definite left ventricular hypertrophy
        - Enlarged heart's main pumping chamber
8. thalach - maximum heart rate achieved 
9. exang - exercise induced angina (1 = yes; 0 = no) 
10. oldpeak - ST depression induced by exercise relative to rest 
    * looks at stress of heart during excercise
    * unhealthy heart will stress more
11. slope - the slope of the peak exercise ST segment
    * 0: Upsloping: better heart rate with excercise (uncommon)
    * 1: Flatsloping: minimal change (typical healthy heart)
    * 2: Downslopins: signs of unhealthy heart
12. ca - number of major vessels (0-3) colored by flourosopy 
    * colored vessel means the doctor can see the blood passing through
    * the more blood movement the better (no clots)
13. thal - thalium stress result
    * 1,3: normal
    * 6: fixed defect: used to be defect but ok now
    * 7: reversable defect: no proper blood movement when excercising 
14. target - tell us whether person have disease or not (1=yes, 0=no) (= the predicted attribute)

Once exploring the data, We'll try to use machine learning to predict our target variable based on the 13 independent variables.

##Splitting:
This is where you'll split your data into a training set and a test set.
Use  training set to train your model and test set to test it.

### Model choices

Now we've got our data prepared, we can start to fit models. We'll be using the following and comparing their results.

1. Logistic Regression - [`LogisticRegression()`](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
2. K-Nearest Neighbors - [`KNeighboursClassifier()`](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)
3. RandomForest - [`RandomForestClassifier()`](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)

## Evaluations..
The confusion matrix is used to evaluate the accuracy of the model.


