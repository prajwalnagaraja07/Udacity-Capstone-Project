# Udacity-Capstone-Project

# Overview
The Udacity Microsoft Azure Machine Learning Engineer Nanodegree Program includes this project. In this project, we ran AutoML on the Kaggle heart failure clinical records dataset.csv dataset, deployed the best model as a RESTful API Webservice, and used endpoints in Microsoft Azure Machine Learning Studio to communicate with the deployed model. For this project, proficiency with Azure Machine Learning Studio Cloud and related technologies is necessary. This is the Microsoft Azure Machine Learning Engineer Nanodegree Program's capstone project.

Video Link: https://www.youtube.com/watch?v=MpZwirP52K0

### Project Set Up

For this project to run a Jupyter Notebook and a compute cluster for the machine learning experiments, a compute instance must be created. Manual selection of the dataset is required.AutoML and HyperDrive were used in two experiments. The best model run, metrics, and a deployed model that communicates with the deployed model via a RESTful API Webservice.

<img width="903" alt="image" src="https://user-images.githubusercontent.com/110788191/234421170-b2c98a01-5a05-46e3-b4fa-5906ae521f75.png">


### Key Steps

### Authentication

Platforms and systems can run automatically and without interruption thanks to a sort of authentication termed a "Service Principal". Access to resources in Microsoft Azure is authenticated and authorized via a service principal, a type of Azure Active Directory (AAD) application. It depicts a machine-generated thing, such a program or a script.
Service Principals are typically used in instances when human involvement would be impracticable or would slow down the process, such as automated scripts, DevOps pipelines, or other systems requiring programmatic access to Azure services. You can use a Service Principal to grant the necessary permissions and access to certain resources without using a human user account, helping to maintain the system's security and integrity.

Within Azure resources, Service Principals can be given particular responsibilities and permissions, giving them more precise control over what tasks they can complete. This means that Service Principals are only given the rights necessary to carry out their assigned tasks, lowering the risk of unwanted access. These permissions are set based on the principle of least privilege.

In conclusion, employing Service Principals for authentication and automation can assist preserve security and reduce the need for human intervention in some situations, all while ensuring an uninterrupted flow of operations.

### HyperDrive

Azure Machine Learning's HyperDrive function aids in automating the process of hyperparameter tuning for machine learning models. The parameters known as hyperparameters, which include learning rate, batch size, and regularization strength, control how a machine learning model behaves and performs. For a particular machine learning algorithm and dataset, HyperDrive assists in determining the best possible combination of hyperparameter values, which can greatly enhance the performance of the model.

1. Create a search area for your hyperparameters using HyperDrive. This search space specifies the ranges or possible values for each hyperparameter you want to modify. This makes it possible for you to tune using a variety of hyperparameter values.

2. You can choose the sample technique to be used while examining the hyperparameter search space. You can select which sampling technique should be used to sample the hyperparameter combinations during the tuning process using Azure Machine Learning's multiple sampling methods, which include Random sampling, Grid sampling, and Bayesian sampling.

3. Define primary metric: Prior to tuning the hyperparameters, you must identify the key statistic you wish to improve, such as accuracy or AUC. Using this key measure, HyperDrive assesses the best model.

4. Select an estimator: Select the machine learning model that you want to tune as an estimator, and specify how it should be trained using the hyperparameter values. To accomplish this, a training script must normally be defined, along with instructions on how to pass hyperparameters to the script during training.

5. Run a HyperDrive experiment: In Azure Machine Learning, you may launch a HyperDrive experiment that automates the hyperparameter tuning procedure. HyperDrive trains the model with several hyperparameter configurations throughout the experiment, exploring the hyperparameter search space using the designated sampling technique while logging the performance data for each configuration.

6. Identify the best-performing hyperparameter configuration based on the primary metric after the HyperDrive experiment is complete by evaluating the data. Choose the best set of hyperparameter values by analyzing and comparing the performance of various hyperparameter configurations using the tools and visualizations offered by Azure Machine Learning.

7. Use and deploy the best model: After determining the optimal hyperparameter setup, you can use Azure Machine Learning to publish the trained model as a web service, making it accessible for prediction in real-world settings. For simple versioning, monitoring, and maintenance, you may also register the best model in the Azure Machine Learning model registry.

By automating the search for the ideal hyperparameter settings, assisting you in finding the top-performing machine learning models for your particular tasks, and speeding up the model building and deployment process, HyperDrive in Azure Machine Learning makes the process of hyperparameter tuning simpler.

### AutoML

Automated Machine Learning, often known as Azure AutoML, is a service offered by Microsoft Azure that streamlines the creation, training, and deployment of machine learning models without the need for advanced data science or machine learning knowledge. It makes AI capabilities more widely available to a wider group of users, including business analysts and domain experts, by streamlining the machine learning workflow and democratizing access to it.

Machine learning models are automatically selected, preprocessed, and optimized by Azure AutoML using a graphical user interface (GUI) and automated algorithms, making it simpler for users to create high-performing models without writing a lot of code. Among Azure AutoML's essential elements are:

### Data preparation: 
Azure AutoML makes it simple for users to import, purge, and preprocess data from a variety of sources, including CSV files, SQL databases, and Azure Blob storage. For customers to better understand their data and spot any concerns with data quality, it has built-in data visualization and data profiling tools.

### Model selection and training: 
Azure AutoML automatically chooses the best machine learning algorithm from a variety of choices based on the input data and task type, such as classification, regression, or time-series forecasting. The performance of the models is then assessed using methods like cross-validation after they have been automatically trained using various hyperparameter combinations.

### Evaluation and interpretation of the model: 
Azure AutoML offers metrics and visualizations to assist customers in assessing the effectiveness of trained models and choosing the top model for their particular use case. Additionally, it offers elements for model interpretability, such as feature importance, that aid users in understanding the significance of various aspects in the model's predictions.

### Monitoring and deployment: 
After a model is chosen, Azure AutoML enables customers to quickly and easily deploy it as a web service, allowing them to include the trained model into their applications. Additionally, it gives users the ability to monitor and manage their models in production by tracking the usage and performance of deployed models.

Azure AutoML enables customers to build fully automated machine learning pipelines that handle everything from model development through data preparation automatically. This makes machine learning efficient and consistent by allowing users to build reusable, scaleable procedures for various use cases.

Overall, Azure AutoML makes it easier for users of all skill levels to design, train, and deploy machine learning models, driving the adoption of machine learning across a range of industries and domains.

1. The best trained model is delivered into production during a model's deployment so that it can be used by others. The VotingEnsemble model, which has the highest accuracy of 0.94607, is the best model discovered during the AutoML run. By enabling authentication and using Azure Container Instance (ACI), which quickly deploys compute instances to deploy models, we configured the deployment settings while deploying the model. Additionally, using it is really straightforward.

2. A vital step in the process before enabling Application Insights is enabling logging. A technology that aids in finding abnormalities and visualizing performance is called application insights. It can be changed with the SDK and activated before or after the deployment. In this project, we extend the Python SDK with particular commands to provide application insights after deployment. Python script that has been changed to display logs.

3. The excellent tool Swagger makes it easy to create, describe, and use RESTful API webservices that are installed in Azure Machine Learning Studio. It goes on to explain the many categories of HTTP requests that an API can handle, in this case Post, Get, and Update. The endpoints area of Azure offers a swagger.json that is used to build a website. This localhost webpage describes a deployed model's HTTP endpoint. The homepage displays the contents of the API for the best model along with the various HTTP queries that are supported after the swagger.sh and serve.py scripts have been executed.

4. Finally, an HTTP API is used to consume the deployed service. In order to submit data, we start an input request, in this example using the HTTP Post request method. Another request approach to get data from a web server is an HTTP GET request. As a result, Azure now has a two-way flow of authorized information. The URI and key are modified to match the primary key for our service in order to consume deployed services, and a RESTful URI is generated after deployment. The output is produced when the endpoint.py script is executed following change.

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

### Future Improvement
A useful technique for evaluating a deployed model's performance and confirming that it adheres to expectations is benchmarking. A popular command-line tool for measuring response time in seconds and assessing model effectiveness is Apache Benchmark (ab).

The ideal model can be found by experimentation, but it's vital to take cost considerations into account, especially when running models on a Virtual Machine (VM). Finding the ideal setup requires balancing various elements, including resource costs, parallel processing, and experiment duration.

A container orchestration technology called Kubernetes might be useful for managing resources and scaling up or down in response to demand. When more data is added to the existing dataset, it can also aid in the efficient deployment and utilization of resources, thereby lowering costs.

Monitoring and logging: Setting up reliable systems for tracking the performance of the deployed model can provide us insights into how it behaves and point out areas where it can be improved.

Automated testing: By include automated testing in the deployment pipeline, performance regressions and other problems can be discovered early on, allowing for prompt correction.

Techniques for optimization: Investigating optimization methods like model quantization, model trimming, or hardware acceleration might enhance the performance of the deployed model while consuming less resources.

Cost management while preserving performance can be achieved by routinely reviewing and improving resource utilization, such as by shrinking virtual machines or configuring Kubernetes clusters more effectively.

Security considerations: To protect sensitive information and preserve compliance, it is essential to make sure that the benchmarking and experimentation processes follow security best practices, such as data protection, access controls, and secure communication.

In conclusion, benchmarking, trying out various models, utilizing tools like Kubernetes, and taking into account additional elements like monitoring, automated testing, optimization techniques, cost optimization, and security considerations can all help to ensure that a deployed model performs to expectations.
