# Covid-19-Death-Predictor
This project explores a machine learning approach to predict the risk level of COVID-19 patients based on their symptoms, medical history, and chronic conditions. The goal is to support healthcare providers in efficiently distributing resources during the pandemic.  

## Project Hypothesis  
The hypothesis of this project was that **patients with chronic diseases are more prone to severe COVID-19 complications**. The analysis confirmed this hypothesis, demonstrating that chronic conditions like cardiovascular disease, diabetes, and chronic respiratory disease significantly increase the risk of severe illness.  

## Context  
COVID-19 is caused by a newly discovered coronavirus, primarily affecting the respiratory system. While most patients experience mild symptoms, individuals with underlying medical conditions are more likely to develop severe complications, requiring intensive care or hospitalization. Efficient resource management has been a critical challenge throughout the pandemic. By predicting high-risk patients early, healthcare providers can better allocate resources such as ventilators, ICU beds, and medications.  

## Objective
The objective of this project is to build a machine learning model that predicts whether a COVID-19 patient is at high risk based on their current symptoms, status, and medical history. This model aims to assist healthcare authorities in identifying and prioritizing high-risk patients to optimize resource allocation.  

## Dataset Overview
The dataset was provided by the **Mexican government** and contains anonymized information on **1,048,576 patients** across **21 features**. These features include patient demographics, medical history, COVID-19 test results, and treatment outcomes.  

### Key Features:
- **Sex**: 1 for female, 2 for male  
- **Age**: Patient's age  
- **Classification**: COVID-19 test result  
  - `1-3`: Positive COVID-19 diagnosis (different degrees)  
  - `4+`: Negative or inconclusive test  
- **Patient Type**:  
  - `1`: Returned home  
  - `2`: Hospitalized  
- **Pneumonia**: Air sacs inflammation (`1`: Yes, `2`: No)  
- **Pregnancy**: Whether the patient is pregnant  
- **Chronic Conditions**:  
  - **Diabetes**  
  - **Chronic Obstructive Pulmonary Disease (COPD)**  
  - **Asthma**  
  - **Hypertension**  
  - **Cardiovascular Disease**  
  - **Chronic Renal Disease**  
  - **Obesity**  
  - **Other Diseases**  
- **Immunosuppression**: Whether the patient is immunosuppressed  
- **Tobacco Usage**: Whether the patient is a smoker  
- **Intubed**: Whether the patient was connected to a ventilator  
- **ICU**: ICU admission status  
- **Date Died**: Date of death (`9999-99-99` if alive)  

### Missing Data 
- Boolean features: `1` for "yes", `2` for "no"  
- Missing data coded as `97` or `99`  

## Model Development 
The model uses patient data to predict high-risk cases. Given the class imbalance and the presence of chronic conditions in severe cases, the model prioritizes features like age, chronic diseases, and respiratory conditions.  

### Project Outcomes  
- **Confirmed Hypothesis**: Patients with chronic diseases are indeed more prone to severe outcomes.  
- **Model Performance**: Evaluation metrics focus on **precision-recall** to account for the imbalanced dataset, ensuring reliable predictions for high-risk patients.

## Dataset can be downloaded from
https://www.kaggle.com/datasets/meirnizri/covid19-dataset/data

## Usage
1. **Clone the Repository**  
   ```bash  
   git clone https://github.com/your-username/covid19-risk-prediction.git  
   cd covid19-risk-prediction  
