# PREDICTING H1N1 VACCINES
## Overview
![MD_Anderson_01](https://user-images.githubusercontent.com/100761559/182134640-d1480c05-f10c-4f0e-ae16-a7843a13960b.jpg)

Our Client is a medical organization situated in Reno,Nevada. The organization works hand in hand with the government when it comes to the distribution of medical supplies including vaccines within the Reno city in Nevada. From the recent outbreak of the Corona Virus and the recent developments which led to the discovery of the vaccine,the organization wants to get a better understanding of how the general population will respond to the vaccine and how likely individuals are to get vaccinated.

## Business Understanding
Since data on Covid-19 is not readily available, The medical organization wants you to use past data on H1N1 influenza virus which is on different people’s backgrounds, opinions, and health behaviors. Using the data on H1N1 vaccine they want you to determine: 

1. if more people got vaccinated or not vaccinated
2. which age group is most likely to get vaccinated, 
3. the impact a doctors reccomendation has on a respondent's decision on whether to get vaccinated or not 
4. the distribution of vaccination by gender. 
5. They also want you to come up with an algorithm that can predict whether someone got the H1N1 vaccine. 

From this they hope to get a better understanding of how these characteristics have been associated with personal vaccination patterns and will provide guidance for future public health efforts.

## Data Understanding and Methodology
For the project we were provided with data on over 10,000 individuals  and the characteristics associated with personal vaccination patterns.
Each row in the dataset represents one person who responded to the National 2009 H1N1 Flu Survey.The data was split into:
- Training Features : This contained the training input/independent variables. It has 36 columns.
- Training Labels : This contained the training target/dependant variables. It has 2 columns h1n1_vaccine and seasonal_vaccine of the binary variable types.In our anaysis i will be using the H1N1 vaccine target variable only.
- Test Features: This contained the test input/independent variable. It has 36 columns. But there weren't any target/dependent variable for the test features

For the analysis i performed Exploratory analysis, built and evaluated some classification models

## Exploratory Data Analysis
### The Distribution of the Target Labels
![Distribution of Target Labels](https://user-images.githubusercontent.com/100761559/182145071-99891081-f317-401a-b857-74888b3af0cb.png)

### Distribution of vaccinated by Gender
![Distribution of vaccinated by Gender](https://user-images.githubusercontent.com/100761559/182145087-b754af37-f9bf-4b1f-b1f7-6b6bb7fdb90e.png)

### Which Age Group is most likely to get vaccinated
![Age Group](https://user-images.githubusercontent.com/100761559/182145111-8e7351d5-2932-461e-a03f-5fcd61800b47.png)

### Impact of a Doctor's Recommendation when Determining Whether to get Vaccinated
![Impact of a doctors recommendation when deciding to get vaccinated](https://user-images.githubusercontent.com/100761559/182145155-4e4a1434-688f-4670-8111-c3e88a27a63d.png)

## Data Modeling
For the data modeling, i built and evaluated classification models on Logistic Regression, Decision trees and K-Nearest Neighbors.
The evaluation metrics i used in my modeling were the accuracy score and the AUC score. The accuracy score tells us what percentage of the predictions will our model get right while the auc score tells us about the performance of the model (a measure of separability) by telling us how good our model is when it comes to distinguishing between classes.
1. The KNN models accuracy scores showed that the model was overfitting as we were getting better scores on the training and performing poorly on the testing. we got an AUC score of 73% for the baseline knn model and 72% for the final model.
2. The decision tree models accuracy scores also showe that the model was overfitting as we were getting better scores on the training and performing poorly on the testing. We got an AUC score of 64% for the baseline decision tree model this gave the worst AUC score while a score of 78% for the final decision tree model this gave the second best AUC score.
3. The Logistic regression model gave accuracy scores that were coomparable with there only being a difference of 0.002 between the train score and the test score.It also gave us the highest AUC score of 82%.

### Final Model
When building the final model, the metric i picked to use when choosing the model to fit the final model on was the AUC scores. The model that provided the best AUC score was Logistic regression model. 


