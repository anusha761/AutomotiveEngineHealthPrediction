# Machine-Learning-Based Health Classification of Automotive Engines for Predictive Maintenance  
> This project focuses on building a machine learning model to classify the health condition of automotive engines based on sensor and performance data. The goal is to distinguish engines in good condition (label = 1) from those in bad condition (label = 0) using real-time telemetry data. By identifying the key indicators which put engines at risk of failure early, this solution supports predictive maintenance strategies — reducing downtime, preventing breakdowns, and improving vehicle reliability. The project integrates feature engineering, statistical selection methods, and machine learning models to deliver a data-driven approach to health monitoring within the automotive domain.


## Table of Contents
- [General Information](#general-information)
- [Conclusions](#conclusions)
- [Technologies Used](#technologies-used)
- [Contact](#contact)


## General Information
- The project addresses a critical challenge in the automotive industry: identifying degrading engines before failure occurs. This is vital for large fleets, service providers, and vehicle owners aiming to reduce unexpected breakdowns and optimize maintenance schedules.
- A binary classification model was developed to predict the health condition of automotive engines using key telemetry signals such as engine RPM, fuel pressure, coolant temperature, and friction-related thermal data.
- The process involved thorough data preprocessing, feature selection using p-values and VIF, model evaluation using ROC-AUC (instead of just accuracy), and comparison across different classifiers.
- Logistic regression was initially used for its interpretability, and XGBoost was later applied to improve prediction performance.
- The dataset comprises sensor readings and performance indicators for multiple engines, with the target variable indicating whether an engine is in good (1) or bad (0) health.


## Conclusions

1. **Key Features Selected**  
   Using logistic regression and statistical filtering, the following six features were selected:
   - Engine RPM: Lower RPM is associated with bad engine health  
   - Fuel Pressure: Higher pressure indicates stress or inefficiency  
   - Coolant Pressure: Healthy coolant pressure supports good engine condition  
   - Coolant Temperature: Warm operating temperatures (not cold) reflect stable performance  
   - Friction Heat Product: Higher friction and thermal stress correlate with bad health  
   - Intercept: Baseline health probability when features are at average levels

2. **Modeling Approach**  
   - **Logistic Regression** was used as the baseline model for its simplicity and interpretability.  
   - Feature coefficients aligned with engineering principles, adding credibility to the results.  
   - The XGBoost** model improved the ROC-AUC score to **0.70**, indicating better classification of engine health status.
   - Accuracy alone was insufficient due to class imbalance; **ROC-AUC** was used for a balanced assessment.


4. **Business Impact**  
   - Early classification of engine health enables **predictive maintenance**, reducing costly breakdowns.  
   - The approach supports smarter fleet management, operational efficiency, and enhanced customer satisfaction.  
   - The model serves as a blueprint for integrating Machine Learning into automotive diagnostic systems.


## Technologies Used
- pandas - version 2.2.2  
- numpy - version 1.26.4  
- matplotlib - version 3.7.1  
- seaborn - version 0.13.2  
- scikit-learn - version 1.3.1   
- XGBoost - version 2.1.4  
- statsmodels - version 0.14.1  


## Contact  
Anusha Chaudhuri – [anusha761] 
