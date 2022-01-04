# Performing QDA, LDA, Logistic Regression and KNN on Auto Dataset 

## Dataset: 
Dataset used is Auto Data Set in ISLR library in R. 

#### Format:

A data frame with 392 observations on the following 9 variables.

mpg :
miles per gallon

cylinders : 
Number of cylinders between 4 and 8

displacement :
Engine displacement (cu. inches)

horsepower :
Engine horsepower

weight :
Vehicle weight (lbs.)

acceleration :
Time to accelerate from 0 to 60 mph (sec.)

year :
Model year (modulo 100)

origin :
Origin of car (1. American, 2. European, 3. Japanese)

name :
Vehicle name

The orginal data contained 408 observations but 16 observations with missing values were removed.

## EDA:

### Histograms:
![hist_ques3](https://user-images.githubusercontent.com/46763031/148008682-1f3faf11-8f9a-4618-831e-8c4505a7075b.png)

The histograms of variables look alright, and no variable seems to be highly left or right skewed.

### Boxplots:
![barplot_ques3](https://user-images.githubusercontent.com/46763031/148008722-7aeaf50a-3a6e-4b2a-aa12-32a39735a0ba.png)

### Scatter-Plots:
![scatter_ques3](https://user-images.githubusercontent.com/46763031/148008752-734e6e41-1307-40e1-a0d6-4f3b0dd9af82.png)

![scatter2_ques3](https://user-images.githubusercontent.com/46763031/148008765-79488b74-306b-4260-822c-004b016da5b2.png)

From the plots above it can be told that cylinder, displacement, horsepower and weight are highly negatively related to our feature mpg01.

### Co-relation Plot: 

![corelation_ques3](https://user-images.githubusercontent.com/46763031/148008799-26c99fc3-ebbb-4ddb-93b1-5e95b91f1341.png)

Co-relation plot confirms our finding from scatter plot. Cylinder, displacement, horsepower and weight are highly negatively related to our feature mpg01. Acceleration, Year and Origin are positively co-related to our response feature.

## LDA:
Linear Discriminant analysis is a true decision boundary discovery algorithm. It assumes that the class has common covariance and it’s decision boundary is linear separating the class.

I get the accuracy of 85.8% and error rate of 14.1% from LDA model with cylinders, displacement, horsepower and weight as predictor.

## QDA:
QDA (Quadratic Discriminant Analysis) is used to find a non-linear boundary between classifiers. Unlike LDA, QDA assumes Different covariance for each of the response classes.

I got the accuracy of 84.6% and error rate of 15.3% from QDA model with cylinders, displacement, horsepower, and weight as predictor.

## Logistic Regression: 
Logistic Regression uses linear regression with the addition of sigmoid function which helps in returning output in between 0-1 range. Here as i have two categorical features 0
and 1, if the logistic regression returns value lower than 0.5 I’ll classify that as 0 and it returns value more than that then I’ll classify that as 1.

I got the accuracy of 84.6% and error rate of 15.3% from QDA model with cylinders, displacement, horsepower and weight as predictor. This is same as QDA accuracy and error.

## KNN: 

k = 1 : gives Accuracy of 83.3 and Error rate of 16.6.
k = 5 : gives Accuracy of 84.6 and Error rate of 15.3.
k = 10 : gives Accuracy of 83.3 and Error rate of 16.6.




