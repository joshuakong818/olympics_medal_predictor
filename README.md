# Is it Possible to Predict Who Will Win Gold at The Olympics? 

By [Joshua Kong](https://github.com/joshuakong818)

## Executive Summary

Through feature selection, feature engineering and classification models this project aims to identify gold medal winners in the Olympics.

---

## Problem Statement

The summer and winter Olympics are held every four years. During each of the games, there are world-class athletes competing to medal in events. Records are broken, the unprecendented becomes a reality, and heroes are born. What if it were possible to predict gold medal winners in future games that have not taken place yet.

__How might data science improve the athlete partnership and endorsement selection processes by shedding competitive advantage granting insights?__

---
## Data

For this project, a dataset from Kaggle (https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results) providing 120 years of historical Olympics information  was used.

#### Data Dictionary:
|Feature|Type|Dataset|Description|
|---|---|---|---|
|**id**|*integer*|olympics data|Unique identifier for athlete| 
|**sex**|*object*|olympics data|Gender of athlete|
|**age**|*integer*|olympics data|Age of athlete|
|**height**|*integer*|olympics data|Height of athlete in centimeters|
|**weight**|*integer*|olympics data|Weight of athlete in kilograms|
|**noc**|*object*|olympics data|National Olympic Committee 3-letter code|
|**games**|*object*|olympics data|Year and season|
|**year**|*object*|olympics data|Year|
|**season**|*object*|olympics data|Summer of Winter|
|**city**|*object*|olympics data|Host city|
|**sport**|*object*|olympics data|Event|
|**medal**|*object*|olympics data|Gold, Silver, Bronze, or No Medal| 

---
## EDA

NaNs were noted in age, height, weight, and medal fields. The mean for all values in age, height, and weight, respectively, was used to replace NaNs. The NaNs in medal, which represented an athlete not medaling, were replaced with string 'No' to be more descriptive. Qualitative fields, sex, noc, games, season, city,and sport fields were dummied so those features could be used in modeling. Custom columns for gold, silver, bronze, and no medal were also created as binary fields for modeling purposes.

---
## Limitations & Next Steps

---

There is plentiful code and data that can be implemented to improve the project. For example, the use of interaction terms to increase model accuracy or gridsearching on hyperparameters to achieve higher accuracy scores and more true positives. Additionally, incorporating a multi-class predictor to predict gold, silver, bronze, and no medals would make this project more comprehensive and give more insights. It would also be interesting to incorporate other features not in the historical olympics dataset like athletes' hometown, state, 40 speed to determine whether features like those will have a positive impact on the model.

Going forward, continuing to train and test models with current Olympics data could prove to be insightful and result in stronger models. Additionally, KNN, AdaBoost, and SVC models need to be troubleshooted for data in this project. Implementing more sophisticated statistics concepts and visuals will help to make project more compelling.



---

## Modeling
---

Logistic Regression, Decision Trees, Bagged Decision Trees, and Random Forests models were tested to get to the best accuracy score. Decision tree and bagged decision trees model performed identically and resulted in the best blend of good test scores, training scores, and true positives. The decision trees will be the prescribed model as bagging, which is an additional process, did not improve model performance. 

The logistic regression model was unable to predict any true positives (gold medal winner). As mentioned above, decision trees and bagged decision trees models performed identically. The results for random forest model were relatively close to the decision trees models' results, but slightly worse.

---
# Conclusion

According to the accuracy and F1 scores, the decision trees model should be able to predict a gold medal winner with 100% certainty. I am highly doubtful about this percentage. Additional work and testing must be done to ensure model was fitted and is predicting correctly as anticipated.
