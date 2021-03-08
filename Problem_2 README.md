# Curneu-Assessment
Task 2 
                                           Diabetes Database Prediction
## Introduction
               The objective of the dataset is to diagnostically predict whether or not a patient has diabetes, 
 based on certain diagnostic measurements included in the dataset. Several constraints were placed on the selection 
 of these instances from a larger database. In particular, all patients here are females at least 21 years old

## Basic Summary of Data
               Data is related to healthcare Industry having 768 observations with 9 variable. Target variable is Outcome.
 It looks like there is no missing value, and boolean, float , integers are different datatypes available.
 Well descriptive analysis shows that variable Glucose, BoodPressure,SckinThickness, Insulin and BMI have minimum value 0 
 which does not make any sense, these values are either missing or outliers, I will be treating them later. 
 I can see in Pregnancies column, minimum is 0 (May be this is sign for no pregnancy) which is considerable,
 But maximum month of pregnancy is 17 which does not make any sense, I will be dealing later. 
 Variance among different predictor variable is varying at large scale , Scaling data will be helpful for Predective modelling.
 
## The columns in this dataset are:
           Pregnancies: Number of times pregnant , Glucose: Plasma glucose concentration a 2 hours in an oral glucose tolerance 
 test , BloodPressure: Diastolic blood pressure (mm Hg) , SkinThickness: Triceps skin fold thickness (mm) ,
 Insulin: 2-Hour serum insulin (mu U/ml) , BMI: Body mass index (weight in kg/(height in m)^2) , 
 DiabetesPedigreeFunction: Diabetes pedigree function , Age: Age (years) , Outcome: Class variable (0 or 1)

<a href="https://ibb.co/tZxvt1J"><img src="https://i.ibb.co/Xy3KgGC/t1.png" alt="t1" border="0"></a>