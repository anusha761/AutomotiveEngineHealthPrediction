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

1. Engine RPM
Coefficient = –0.4040

- Higher engine RPM is associated with a lower probability of good engine health. Bad engines in the dataset tend to operate at unusually high RPMs, possibly due to:

- Poor idle control,

Compensatory behavior by the ECU (engine control unit),

Or mechanical inefficiencies causing unstable engine behavior. Thus, elevated RPM may serve as a symptom of engine distress, rather than high performance.

2. Fuel Pressure
Coefficient = +0.2704

Higher fuel pressure is linked to a greater probability of good engine health. This suggests that well-functioning engines maintain consistent and adequate fuel pressure to ensure efficient combustion. Conversely, lower fuel pressure could be symptomatic of:

Fuel pump degradation,

Injector clogging,

Or compensation in faulty engines.

Coolant Pressure
Coefficient = –0.0548

Higher coolant pressure is slightly associated with lower engine health. This could indicate:

Overheating due to poor coolant flow,

Blocked passages or a clogged radiator,

Or pressure buildup from ineffective heat dissipation.

Lubricant Oil Temperature
Coefficient = –0.1662

Higher oil temperatures reduce the likelihood of good engine health. This reflects elevated internal friction, possible inadequate lubrication, or thermal stress — all of which are indicators of engine wear or inefficiency. Healthy engines tend to operate within a stable and safe oil temperature range.

Coolant Temperature
Coefficient = –0.0523

Increased coolant temperature is mildly associated with lower engine health. While some increase in coolant temperature is normal during engine operation, excessive levels may point to:

Overheating,

Thermostat failure,

Or clogged coolant flow.

Thus, this variable acts as a subtle risk factor.

Oil Pressure per RPM (Lubricant Oil Pressure / Engine RPM)
Coefficient = +0.3014

A higher oil pressure per unit of RPM is strongly associated with good engine health. This feature reflects an engine's ability to maintain oil pressure effectively as it operates at higher speeds, suggesting a well-maintained lubrication system and good mechanical integrity. It emerged as one of the most important predictors in the model.

Oil Pressure per RPM was a derived feature. It emerged as a good positive predictor of engine health, indicating that engines capable of sustaining oil pressure across RPMs tend to be in better condition.

Protective Indicators (associated with good engine health):

High oil pressure per RPM

Adequate and stable fuel pressure

Risk Indicators (associated with poor engine health):

Elevated engine RPM (crossing 1400 rpm)

High lubricant oil temperature (crossing 77 units)

High coolant temperature and pressure (crossing 80 units and 4 units respectively)

Note: Units for temperature and pressure were not explicitly defined in the dataset. All thresholds are based on relative trends observed in the data.
   

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
