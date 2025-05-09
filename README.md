# Attrition Alert System
A employee retention risk alert model for HR department

## Overview 
The goal of this project was to develop a model that enables the client’s company to predict whether an employee is likely to leave, as well as to uncover the key factors contributing to their resignation.

This project utilized data from a survey conducted by the HR department, which sampled employees. The final **Random Forest prediction model** achieved an AUC of 93.56%, precision of 91.51%, recall of 88.76%, F1-score of 90.11%, and accuracy of 96.76%. The model identified **`last_evaluation`**, **`number_project`**, **`tenure`**, and **`overworked`** as the most important factors influencing employees' decisions to stay or leave the company.

## Business Understanding 
By gaining these insights, the company can better understand the underlying issues and take proactive steps to improve employee retention and job satisfaction, and save money and time training new employees. 

## Data Understanding
The dataset consisted of approximately 15,000 survey responses and 10 features. Among these, 3,008 were identified as duplicates and were dropped for future model building. The features included information on employees' working hours, tenure, salary, promotion status, satisfaction level, and last evaluation score. Approximately 16% of the data came from employees who had already left the company.

<img alt="Work Hours by Project Numbers" src=/images/workHrs-projectNum-left.png>
<img alt="Promotion vs Work hours" src=/images/promotion-workHrs.png>
The upper two charts show the relationship between the number of projects and monthly work hours. They reveal that employees who are assigned too many projects, resulting in an average work hour significantly higher than their peers, are more likely to leave the company.

The lower chart highlights the relationship between monthly work hours and promotion status, showing that employees who worked long hours but did not receive a promotion almost all left the company.

Since the satisfaction level might introduce data leakage, a new feature, 'overworked', was created to substitute and reflect the relationship between working hours and satisfaction level.

## Modeling and Evaluation 
Logistic Regression, Decision Tree, and Random Forest models were developed for this project. Among them, the Random Forest model achieved the highest AUC score.
The model identified evaluation score, number of projects, tenure, and overworked as the most important features for predicting employee attrition.
The Random Forest model achieved a precision of 91.51%, recall of 88.76%, F1-score of 90.11%, and accuracy of 96.76%.

<img alt="Featrue Importances" src=/images/feature-importances.png>
Horizontal bar chart showing feature importance of decision tree and random forest model.

## Conclusion
Excessive workloads combined with insufficient recognition are key drivers of employee attrition.
Retention of long-tenured, high-performing employees is critical to organizational stability.
Implementing effective workload management and formal recognition strategies is recommended to mitigate attrition risks.

---
[My name is Yvette](https://yvette-yl.github.io/ "Welcome to My Profile")  |  [Proposel](/PACE_Strategy.md "")  |  [Python Notebook](/attritionalertsystem.ipynb "")  |  Presentation  | 
