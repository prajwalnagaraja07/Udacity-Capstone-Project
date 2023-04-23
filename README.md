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
