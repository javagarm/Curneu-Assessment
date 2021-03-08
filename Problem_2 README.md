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

## BloodPressure
<a href="https://imgbb.com/"><img src="https://i.ibb.co/cQYV0yy/t7.png" alt="t7" border="0"></a>
We can see that minimum is 0 which may be considered as no Blood Pressure,which is quite impossible to believe. 
<a href="https://ibb.co/R33jWm7"><img src="https://i.ibb.co/fkkD75Q/t8.png" alt="t8" border="0"></a>
## Understanding Distribution
The distribution of BloodPressure among patients is unimodal (This is not a bimodal because BP=0 does not possible
 and it is Outlier) and bell shaped, centered at about 65 with most of the data between 60 and 90, A range of roughly 100,
 and outliers are present on the lower end(BP ==0).

Note :- BoxPlot of both categories shows that there is a little association of BP with Diabetic VS Non-Diabetic patients.
 We can also see that some outliers are present.

It looks like there are few Outliers at both higher end and lower end. But at higher end maximum BP is 122, 
So it is considerable. Now at lower end BP near 25 is not possible. So i will treat missing value with medium 
and then i will also treat outliers.

## SkinThickness
<a href="https://imgbb.com/"><img src="https://i.ibb.co/4FV8FqS/t9.png" alt="t9" border="0"></a>
We can see that minimum is 0 which may be considered as no Skinthickness,which is quite impossible to believe. 
<a href="https://ibb.co/BCnCCkf"><img src="https://i.ibb.co/KrKrrn5/q1.png" alt="q1" border="0"></a>

## Understanding Distribution
The distribution of SkinThickness among patients is looking like Bimodal (But i think,
 This is not a bimodal because ST=0 which is not possible so far and it may effect distribution, and it is bell shaped,
 centered at about 20 with most of the data between 15 and 45, A range of roughly 60, and outliers are present on the lower end(ST ==0).

Note :- BoxPlot of both categories shows that there is a little association of ST among Diabetic VS Non-Diabetic patients.

## Insulin
<a href="https://ibb.co/ccmw8nK"><img src="https://i.ibb.co/rGW3prK/q2.png" alt="q2" border="0"></a>
We can see there are many outliers. So i will fill 0 with Median of Insulin. I will also treat Outliers after removing zero.¶

## BMI
<a href="https://ibb.co/vhfQyc4"><img src="https://i.ibb.co/KDBL45x/q3.png" alt="q3" border="0"></a>
Outliers are considerable, So i will replace zero with mean.¶

## DPF
<a href="https://ibb.co/808cFb1"><img src="https://i.ibb.co/VtBmXxf/dpf.png" alt="dpf" border="0"></a>
Now we are done with missing value and Outliers. Let us take a look at data and then move ahead with other steps.¶


## Let us take a closer look at data by doing a quick VISUALIZATION
Well, Pregnancies, Insulin, DBF and Age having skewed distribution.
 We know most of the machine learning models uses assumpton of normality so these variables might need to be scaled, 
But we may consider the assumption to be true according Central Limit Theorem that if number of observation is large 
we can consider the distribution to be normal or bell shaped. Removing Outliers may also help us to achieve normal distribution 
of that variable.It looks like Glucose, BP and BMI variables have some outliers.

Variables are not correlated strongly with each other.

## Let us Plot pairplot according to outcome
data points are spread non linear, Fitting tree based models might help us to get better accuracy or SVC with Non Linear Decision Boundry.
<a href="https://imgbb.com/"><img src="https://i.ibb.co/6mXTyJF/fffffff.png" alt="fffffff" border="0"></a>
## 
"Correlation"
Nice, Variables are not much associated linearly.
<a href="https://ibb.co/nDc4PKs"><img src="https://i.ibb.co/wKW8c2N/a1.png" alt="a1" border="0"></a>
## ON Comparing All Models SVC has the maximum Accuracy
<a href="https://ibb.co/6ZQGrsL"><img src="https://i.ibb.co/W3C7GKj/11111.png" alt="11111" border="0"></a>
<a href="https://ibb.co/gR3m19n"><img src="https://i.ibb.co/9rNcXgM/aaa11111.png" alt="aaa11111" border="0"></a>
  