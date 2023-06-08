# Causality Analysis : Air Quality and Chronic Obstructive Pulmonary Disease (COPD)

## Data Overview

- U.S. Chronic Disease Indicators: Chronic Obstructive Pulmonary Disease
- CDC: Daily Census-Tract PM2.5 Concentrations
- CDC: Daily Census-Tract Ozone Concentrations

### External datasets
Common purpose: To address the causal impact of confounding variables while drawing out the causal relationship between smoking and COPD prevalence.

- <a href="https://ghgdata.epa.gov/ghgp/main.do#/listFacility/?q=Find%20a%20Facility%20or%20Location&st=&bs=&et=&fid=&sf=11001100&lowE=-20000&highE=23000000&g1=1&g2=1&g3=1&g4=1&g5=1&g6=0&g7=1&g8=1&g9=1&g10=1&g11=1&g12=1&s1=1&s2=1&s3=1&s4=1&s5=1&s6=1&s7=1&s8=1&s9=1&s10=1&s201=1&s202=1&s203=1&s204=1&s301=1&s302=1&s303=1&s304=1&s305=1&s306=1&s307=1&s401=1&s402=1&s403=1&s404=1&s405=1&s601=1&s602=1&s701=1&s702=1&s703=1&s704=1&s705=1&s706=1&s707=1&s708=1&s709=1&s710=1&s711=1&s801=1&s802=1&s803=1&s804=1&s805=1&s806=1&s807=1&s808=1&s809=1&s810=1&s901=1&s902=1&s903=1&s904=1&s905=1&s906=1&s907=1&s908=1&s909=1&s910=1&s911=1&si=&ss=&so=0&ds=E&yr=2011&tr=current&cyr=2011&ol=0&sl=0&rs=ALL"> Greenhouse gas emission </a>
- <a href="https://www.kaggle.com/datasets/capcloudcoder/us-wildfire-data-plus-other-attributes?select=Wildfire_att_description.txt"> Wildfire </a>
- <a href="https://www.census.gov/data/datasets/time-series/demo/popest/2010s-state-total.html"> Population Density </a>
- <a href="https://ghdx.healthdata.org/record/ihme-data/united-states-smoking-prevalence-county-1996-2012"> Smoking Prevalence </a>

---

Project: Investigating the Impact of Air Quality and Geographic Factors on Chronic Disease Prevalence

Conducted an in-depth analysis to explore the relationship between air quality, geographic factors, and the prevalence of chronic obstructive pulmonary disease (COPD) among adults.

Collected and processed various datasets including COPD prevalence, air quality measurements (ozone and PM2.5 concentrations), smoking prevalence, greenhouse gas emissions, wildfire occurrences, and population density.

Performed exploratory data analysis (EDA) to gain insights into the distribution and patterns of the data, including visualizations of COPD prevalence, air quality measurements, smoking rates, and wildfire occurrences across different states.

Investigated confounding variables such as smoking prevalence and greenhouse gas emissions, and their potential impact on COPD prevalence and air quality.

Employed unconfoundedness techniques to estimate the causal average treatment effect (ATE) of bad air quality on COPD prevalence.

Utilized inverse propensity weighting (IPW) to adjust for confounding variables and estimate the ATE.

Developed a linear regression model to predict COPD prevalence based on air quality measures, smoking rates, wildfire occurrences, and population density.

Assessed model performance and interpretability, utilizing statistical measures such as R-squared and coefficients.

Summarized and interpreted the results, providing a clear statement about causality and the estimated effect of bad air quality on COPD prevalence.

Emphasized the need for further research and potential limitations, including the possibility of unaccounted confounders.

## Introduction

COPD is a chronic lung disease characterized by airflow obstruction. This project aims to provide an efficient and accurate system for COPD analysis, which can assist healthcare professionals in diagnosis and treatment planning. The project utilizes machine learning techniques, data preprocessing, and visualization tools to analyze patient data and predict COPD progression.

## Features

- Data preprocessing: Clean and preprocess patient data, including medical records, lung function tests, and demographic information.
- Feature extraction: Extract relevant features from the preprocessed data, such as lung function parameters, smoking history, and comorbidities.
- Machine learning models: Develop and train predictive models using various algorithms, including random forests, support vector machines, and neural networks.
- Visualization: Create interactive visualizations to explore and analyze the data, helping healthcare professionals gain insights into COPD patterns and trends.
- Evaluation: Assess the performance of the models using metrics such as accuracy, precision, recall, and area under the receiver operating characteristic curve (AUC-ROC).
- Deployment: Deploy the trained models as a web application or API, enabling real-time COPD prediction for new patient data.


## Research Question 1 - Causal Inference

Does low air quality cause the onset of Chronic Obstructive Pulmonary Disease (COPD)?

### Conclusion

- Identified the causal effect of air quality on the prevalence of Chronic Obstructive Pulmonary Disease
- Bad air quality causes the prevalence of COPD, the states with bad air quality can improve their legislation that regulates air pollutants generated from transportations, manufacturers, or place more air filtering technologies to control air pollutants generated from wildfires. So that individuals could be less exposed to ozone and PM 2.5 concentration which also decreases the prevalence of COPD.
- Identified our treatment and outcome by merging air quality and COPD prevalence dataset and by adding confounding variables we were able to improve our model quality and certainty in our causal inference decision. 
- For future studies, we could have found the relationship between genetic factors and prevalence of COPD or obtain census data that contains information of personal demographics of each state.

## Research Question 2 - GLM & Random Forest

Can we predict whether people have COPD from geographical location and race/ethnicity?

### Conclusion

- Results of Bayesian and Frequentist models produced different results for all the races; however, both Bayesian and Frequentist model produced very similar results for longitude and latitude.
- Demographic features such as race had little to no feature importance, which means that geographical data alone suffice to predict COPD. i.e. Excluding racial features will have little to no impact to the accuracy of the model.
- Using random forests, we’ve seen that location can predict COPD. Hence, we can use classification techniques (i.e. k-NN, hierarchical clustering) to first cluster locations based on common geographical attributes (i.e. rural/urban, climate, humidity, etc.). Then, it will be possible to identify relationships between a combination of geographical attributes and the prevalence of COPD or other respiratory diseases.
- Future studies can test if residents in rural areas with dusty winds and/or factory air pollutants are more prone to respiratory diseases than those in urban areas. 


