# Attrition Alert System
A employee retention risk alert model for HR department

## Overview 
The goal of this project was to develop a model that enables the client’s company to predict whether an employee is likely to leave, as well as to uncover the key factors contributing to their resignation.

This project utilized data from a survey conducted by the HR department, which sampled employees. The final **Random Forest prediction model** achieved an AUC of 93.56%, precision of 91.51%, recall of 88.76%, F1-score of 90.11%, and accuracy of 96.76%. The model identified **`last_evaluation`**, **`number_project`**, **`tenure`**, and **`overworked`** as the most important factors influencing employees' decisions to stay or leave the company.

## Business Understanding 
By gaining these insights, the company can better understand the underlying issues and take proactive steps to improve employee retention and job satisfaction, and save money and time training new employees. 

## Data Understanding
The dataset consisted of approximately 15,000 survey responses and 10 features. Among these, 3,008 were identified as duplicates and were dropped for future model building. The features included information on employees' working hours, tenure, salary, promotion status, satisfaction level, and last evaluation score. Approximately 16% of the data came from employees who had already left the company.
<img alt=“Satisfaction-Tenure-Attrition” src=/images/workHrs-projectNum-left.png>
<img alt=“WorkHours-Promotion-Attrition” src=/images/workHrs-promotion.png>
The upper two charts show the relationship between the number of projects and monthly work hours. They reveal that employees who are assigned too many projects, resulting in an average work hour significantly higher than their peers, are more likely to leave the company.

The lower chart highlights the relationship between monthly work hours and promotion status, showing that employees who worked long hours but did not receive a promotion almost all left the company.

Since the satisfaction level might introduce data leakage, a new feature, 'overworked', was created to substitute and reflect the relationship between working hours and satisfaction level.

## Modeling and Evaluation 
A random forest model comprising 100 decision trees was used to determine feature importance in who would tip generously or not. The below plot shows that trip duration, distance, and the cost of a fare were the Top 3 most important factors in determining a generous tipper from a non-generous one. The overall model performed with 86% accuracy and 72% precision. 

Horizontal bar chart showing feature importance of random forest model.
## Conclusion
This model can benefit Taxi Drivers in knowing if they will be tipped generously or not; however, running a parametric model to determine how much each variable will influence the actual price of the tip. In the future, adding more information on a rider’s past tipping behavior may also be beneficial in helping the stakeholder address their business problem. 

---
[Data](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv "Provided by Kaggle")  |[Proposel](/PACE_Strategy.md "")  |[Python Notebook](https://www.kaggle.com/code/yvetteliuyang/attritionalertsystem "A link to the Kaggle Notebook. An .ipynb file is included in the files folder for reference.")  |[Presentation]()  
