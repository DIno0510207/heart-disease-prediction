# Heart Disease Prediction
Used the UCI Machine Learning [Heart Disease](https://archive.ics.uci.edu/dataset/45/heart+disease) dataset.

**Test set metrics**<br>
Accuracy     : 0.8689<br>
Precision    : 0.8846<br>
Recall       : 0.8214 (Sensitivity)<br>
Specificity  : 0.9091<br>
F1 Score     : 0.8519<br>
ROC AUC      : 0.9307<br>
<img width="936" height="390" alt="image" src="https://github.com/user-attachments/assets/e4a46f2b-6126-4028-a03d-41fd33640ba0" />

## Features
The Cleaveland Database was used from the dataset consisting of 303 records and these features were used for training:
1. age: age in years
2. sex: sex (1 = male; 0 = female)
3. cp: chest pain type
   - Value 1: typical angina
   - Value 2: atypical angina
   - Value 3: non-anginal pain
   - Value 4: asymptomatic
4. trestbps: resting blood pressure (in mm Hg on admission to the hospital)
5. chol: serum cholestoral in mg/dl
6. fbs: (fasting blood sugar > 120 mg/dl)  (1 = true; 0 = false)
7. restecg: resting electrocardiographic results
   - Value 0: normal
   - Value 1: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV)
   - Value 2: showing probable or definite left ventricular hypertrophy by Estes' criteria
8. thalach: maximum heart rate achieved
9. exang: exercise induced angina (1 = yes; 0 = no)
10. oldpeak = ST depression induced by exercise relative to rest
11. slope: the slope of the peak exercise ST segment
    - Value 1: upsloping
    - Value 2: flat
    - Value 3: downsloping
12. ca: number of major vessels (0-3) colored by flourosopy
13. thal: 3 = normal; 6 = fixed defect; 7 = reversable defect
14. num: diagnosis of heart disease (angiographic disease status)
    - Value 0: < 50% diameter narrowing
    - Value 1: > 50% diameter narrowing

## Things done
1. Imputation of missing values using KNN
2. Creation of new domain-aware features
3. Creation of new categorical bins
4. EDA with Correlation heatmap, pairplot and crosstab
5. One-hot / Label encoding of features as per requirement
6. PCA projection of feature space
7. Hyperparameter tuning of the models with `hyperopt`
8. Comparison of tuned models with approximately good parameters
9. Create a pipeline for Ensemble learning with LogisticRegression as meta learner
10. Calibration of the model with CalibratedClassifierCV
