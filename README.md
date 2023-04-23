# Udacity-Capstone-Project

# Overview
The Udacity Microsoft Azure Machine Learning Engineer Nanodegree Program includes this project. In this project, we ran AutoML on the Kaggle heart failure clinical records dataset.csv dataset, deployed the best model as a RESTful API Webservice, and used endpoints in Microsoft Azure Machine Learning Studio to communicate with the deployed model. For this project, proficiency with Azure Machine Learning Studio Cloud and related technologies is necessary. This is the Microsoft Azure Machine Learning Engineer Nanodegree Program's capstone project.

### Project Set Up

For this project to run a Jupyter Notebook and a compute cluster for the machine learning experiments, a compute instance must be created. Manual selection of the dataset is required.AutoML and HyperDrive were used in two experiments. The best model run, metrics, and a deployed model that communicates with the deployed model via a RESTful API Webservice.

### Dataset

Name: heart_failure_clinical_records_dataset.csv

This dataset contains the following features: age, anaemia, creatinine, diabetes, ejection_fraction, high_blood_pressure, platelets, serum_creatinine, sex, smoking and time. The target is DEATH_EVENT.

When the heart cannot pump enough blood to meet the body's needs, heart failure results. The electronic medical records of patients with the required symptoms, physical characteristics, and clinical laboratory test results were used to build this dataset. These data were used for biostatistical analysis to reveal patterns and relationships that would have gone unnoticed by medical professionals. Based on information from a patient's medical records, machine learning can forecast the patient's prognosis.

In this categorization issue, my goal is to determine whether a patient's symptoms will result in mortality. The "DEATH_EVENT" variable is the target.
13 clinical characteristics
age: The patient's age in years Red blood cells or hemoglobin levels falling off (boolean) high blood pressure: a boolean value of true if the patient has hypertension Blood creatinine phosphokinase (CPK) enzyme concentration (mcg/L) boolean value indicating whether the patient has diabetes Blood that leaves the heart with each contraction is ejected in a certain proportion, or ejection fraction. the number of platelets in a milliliter of blood, or platelets. binary sex: woman or male Blood serum creatinine concentration (mg/dL): serum sodium: The quantity of sodium in the blood (in mEq/L) from serum. smoking:(boolean) whether the patient smokes or not Follow-up timeframe in days [target] death event: boolean value indicating if the patient passed away during the follow-up period.

### Auto ML 

<img width="1433" alt="Screenshot 2023-04-23 at 14 57 12" src="https://user-images.githubusercontent.com/110788191/233844729-e0330887-713f-4269-8d94-a905d37ec249.png">

<img width="1434" alt="Screenshot 2023-04-23 at 14 57 31" src="https://user-images.githubusercontent.com/110788191/233844739-b3ac8612-ac55-4054-a8f2-8d90ce71b8af.png">

### Auto ML Best Model
<img width="1438" alt="Screenshot 2023-04-23 at 15 02 03" src="https://user-images.githubusercontent.com/110788191/233844744-cb8560df-fd08-4bc4-83a1-3b4b95215211.png">

### ACI Deployment
<img width="1435" alt="Screenshot 2023-04-23 at 16 13 24" src="https://user-images.githubusercontent.com/110788191/233844980-a5013112-6770-4208-85f9-5c9760cb5f1d.png">

### Deployment Call
<img width="1426" alt="Screenshot 2023-04-23 at 16 14 00" src="https://user-images.githubusercontent.com/110788191/233845007-c3c5b4e3-0054-4008-a849-3fe2fbdfe237.png">

### Deployment Status
<img width="1437" alt="Screenshot 2023-04-23 at 16 14 34" src="https://user-images.githubusercontent.com/110788191/233845036-2eaf8244-49f4-4c40-8f9d-ab8d3df0b43c.png">

### Model Ednpoint Deployment

<img width="1436" alt="Screenshot 2023-04-23 at 15 05 54" src="https://user-images.githubusercontent.com/110788191/233844858-463f9d54-b075-4955-8f25-0ab7e8194b34.png">

### HyperDrive
<img width="1439" alt="Screenshot 2023-04-23 at 15 03 19" src="https://user-images.githubusercontent.com/110788191/233844813-9cc8ade4-fb2a-4860-9157-30afb273bd00.png">

### HyperDrive Sweep

<img width="1440" alt="Screenshot 2023-04-23 at 15 04 48" src="https://user-images.githubusercontent.com/110788191/233844831-e9dd8cf3-e272-4abf-8b55-3a37f5b19d2b.png">
