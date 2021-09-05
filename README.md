# **<p align="center">Alphabet Soup Charity Analysis</p>**

### **<p align="center">A Machine Learning analytics report designed to predict the success or failure of organizations funded by the Alphabet Soup Charity.</p>**

---
## Overview
This report will enumerate how effective a Deep-Learning Neural Network can be at predicting the success or failure of a organization that was provided a loan via the Alphabet Soup Charity. The results section below shows the process used to create our machine learning model and what steps were taken to ensure its best performance. Lastly, the Summary section provides the results of our testing followed by recommendations for how a different model could solve this problem better and why.

---
## **<p align="center">Results - Data Preprocessing</p>**
---

<p align="center">
   <img width="900" height="200" src="https://github.com/Jamesrx33/Neural_Network_Charity_Analysis/blob/main/Resources/Images/Dataframe.png?raw=true">
</p>

* **Target Variable:** The target variable of our analysis was "Is_Successful"
  - This was a binary variable: 1 for yes, 0 for no. 
* **Feature Variables:** Our feature variables were: Application_Type, Affiliation, Classification, User_Case, Organization, Status, Income_Amt,Special_Considerations and Ask_Amt 
* **Dropped Variables:** The EIN and Name vaiables were neither seen as the target nor meanful features and were therefore removed from our analysis

---
## **<p align="center">Results - Compiling, Training and Evaluating the Model</p>**

<p align="center">
   <img width="500" height="300" src="https://github.com/Jamesrx33/Neural_Network_Charity_Analysis/blob/main/Resources/Images/Model_Shape.png?raw=true">
</p>

---

* **Model Shape:** Our model had 240 neurons, three hidden layers, we chose Relu as our activation functions for each hidden layer and Sigmoid for our output layer.
  - We doubled the number of initial neurons (120) to increase predictive power
  - We added a hidden layer to provide another stream of analysis and improve performance
  - We chose the Relu and Sigmoid activation functions because they do well with binary classifications
* **Goal:** Our goal for the model was to achieve 75% accuracy in our predictions, we were able to do so
* **Optimization Steps:** In order to obtain 75% accuracy, we needed to do the following optimizations:
  - **Remove Noise:** After preprocessing, we identified 12 variables that contributed very little to the models variance amd removed them
  
  <p align="center">
   <img width="500" height="300" src="https://github.com/Jamesrx33/Neural_Network_Charity_Analysis/blob/main/Resources/Images/Variance%20Graph.png?raw=true">
</p>

  - **Remove Outliers:** The "ASK_AMT" variable had a large number of outliers, we reduced them by filtering out requests for less than $8,000. Below is a box and whisker plot indicating the outliers -- this is in incriments of e^9(~8,100)

  <p align="center">
   <img width="500" height="300" src="https://github.com/Jamesrx33/Neural_Network_Charity_Analysis/blob/main/Resources/Images/Box-And-Whisker.png?raw=true">
</p>

---
## Summary
---

After optimization, our model was able to make predictions with a 75.3% accuracy with .53 overall loss. Where as this is an acceptable outcome, we had to remove close to 20% of the data (in outliers) to achieve it. It is for this reason that we would like to suggest an alternative model as a point of comarison


* **Suggested Alternative Model:** Logistic Regression
  - A logistic regression model would be a low-cost alternative to the Neural Network
  - Logistic regression excels at binary classification over non-linear data, like what we have in the Alphabet Soup Charity data

---

## Reference Documentation - [Source Code Repository](https://github.com/Jamesrx33/Neural_Network_Charity_Analysis), [Download .zip file](https://github.com/Jamesrx33/Neural_Network_Charity_Analysis/archive/refs/heads/main.zip)
