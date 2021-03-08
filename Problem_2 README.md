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


<a href="https://ibb.co/tZxvt1J"><img src="https://i.ibb.co/Xy3KgGC/t1.png" alt="t1" border="0"></a>  <a href="https://ibb.co/ThnZ1Gg"><img src="https://i.ibb.co/x5cyYb7/t2.png" alt="t2" border="0"></a>

Since it looks like there is no missing values. But in descriptive statistics we have seen that some variables have minimum = 0 
and pregnancy variable has maximum = 17 which is not making sense. So let us explore these variables 
and treat them accordingly

Eventhough the Datatypes are perfect , But we can change Outcome to boolean datatype which will have an impact
 in -Space Complexity

## Data Cleaning and Preprocessing is Done for each attribute

## Pregnancies
  
<a href="https://imgbb.com/"><img src="https://i.ibb.co/QKzTCwr/t3.png" alt="t3" border="0"></a>
 We can see that minimum is 0 which may be considered as no Pregnancy, But maximum is 17 which is quite impossible to believe. 
Let us see distribution and also boxplot for outliers
<a href="https://ibb.co/vBL1zpX"><img src="https://i.ibb.co/H2G7g6h/t4.png" alt="t4" border="0"></a>

## Understanding Distribution Of Pregnancies
The distribution of Pregnancies in data is unimodal and skewed to the right, centered at about 1 with 
most of the data between 0 and 15, A range of roughly 15, and outliers are present on the higher end.

Note :- BoxPlot of both categories shows that People with higher pregnancy months have higher risk of Diabetes
 (There is not statistical evidence, May be i will be testing a hypothesis)


## Glucose
<a href="https://imgbb.com/"><img src="https://i.ibb.co/QMJT732/t6.png" alt="t6" border="0"></a>
We can see that minimum is 0 which may be considered as no Glucose,  which is quite impossible to believe. 
Let us see distribution and also boxplot for outliers
<a href="https://ibb.co/jfHNvdt"><img src="https://i.ibb.co/bm70gxt/t5.png" alt="t5" border="0"></a>

## Understanding Distribution Of Glucose Level
The distribution of Glucose level among patients is unimodal and roughly bell shaped, centered at about
115 with most of the data between 90 and 140, A range of roughly 150, and outliers are present on the lower end(Glucose ==0).

Note :- BoxPlot of both categories shows that People with higher Glucose level have higher risk of Diabetes 
(There is not statistical evidence, May be i will be testing a hypothesis ) We can also see that
 some outliers are present on non diabetic patient observation.