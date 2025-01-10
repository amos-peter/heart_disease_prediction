# heart_disease_prediction
A data analytics project using machine learning to predict heart disease risk. Developed as part of WQD7003 group project.

##### WQD7003 Data Analytics

# **Project: Heart Disease Prediction**

### Prepared by: Group 5   



| Matric No | Name |
|:-------   |:------- |
| 22051081  | Tan Kai Ying |
| 22088840  | Nur Nazifa binti Zhamri |
| 22099603  | Ong Xi Yan |
| 22102674  | Muhd Izani bin Zulkifli |
| 23056781  | Amos Peter |

## **Crisp-DM**
* 1.0 Business Understanding
* 2.0 Data Understanding
* 3.0 Data Pre-processing
* 4.0 Exploratory Data Analytics
* 5.0 Modeling
* 6.0 Evaluation
* 7.0 Deployment

#### **1.1 Background**

Heart disease is a leading cause of mortality worldwide, imposing
a significant burden on healthcare systems and individuals. Early detection and prevention are essential to mitigate its impact. As of the 2022 update, the demand for accurate predictive tools to assess heart disease risk is growing. In response, we propose the "Heart Disease Prediction" project, which utilizes data analytics and machine learning techniques to develop a predictive system. This system aims to offer timely risk assessments, personalized interventions, and improved patient outcomes, addressing the pressing need for proactive measures in preventing heart disease.

#### **1.2 Problem Statement**

In assessing the current situation, it is evident that heart disease stands as a prominent global health concern, necessitating urgent and effective preventive measures. The existing healthcare landscape requires advanced tools to enhance early detection and intervention strategies. The availability of data analytics and machine learning techniques presents a valuable.

#### **1.3 Business Goals**

*  To develop a predictive model with a minimum accuracy of 90% to identify individuals at risk of heart disease for early intervention.
*   To create a personalized risk assessment system that factors in individual health, lifestyle, and demographic variables to optimize preventive strategies.

#### **1.4 Data Mining Goals**

*   Gather and preprocess a comprehensive dataset, ensuring data quality, handling missing values, and preparing it for analysis.
*   Develop a predictive model with a high level of accuracy in identifying individuals at risk of heart disease.

#### **2.1 Gathering and Describing Data**

The dataset, sourced from the Centers for Disease Control and Prevention (CDC), is an integral component of the Behavioral Risk Factor Surveillance System (BRFSS), which annually conducts telephone surveys to gather vital health information from U.S. residents. Established in 1984 with 15 states, the BRFSS has expanded its coverage to encompass all 50 states, the District of Columbia, and three U.S. territories, performing over 400,000 adult interviews each year, thus establishing itself as the world's largest continuously conducted health survey system. The most recent dataset, which includes data from 2023, was selected for this project due to its health factors and questions that directly or indirectly influence heart disease. Furthermore, two versions of the dataset are available: one with missing values (NaNs) and one without, providing comprehensive data for analysis and modeling.

<br>

Link: https://www.cdc.gov/brfss/annual_data/annual_2022.htm

Kaggle link: https://www.kaggle.com/datasets/kamilpytlak/personal-key-indicators-of-heart-disease/data

The table below shows all variables and their descriptions.

<br>


| No.  | Variables           | Description                                                             |
| :--  | :-------            | :------------------------------------------------                       |
| 1.   | State               | The state in which the individual resides.                              |
| 2.   | Sex                 | Gender of the individual.                                               |
| 3.   | GeneralHealth       | Self-assessment of general health.                                      |
| 4.   | PhysicalHealthDays  | Days with physical health issues in the past 30 days.                   |
| 5.   | GeneralHealth       | Self-assessment of general health.                                      |
| 6.   | LastCheckupTime     | Self-reported frequency and intensity of physical activity or exercise. |
| 7.   | SleepHours          | Average hours of sleep per night.                                       |
| 8.   | RemovedTeeth        | History of tooth removal.                                               |
| 9.   | HadHeartAttack      | History of heart attacks.                                               |
| 10   | HadAngina           | History of chest pain.                                                  |
| 11.  | HadStroke           |   History of stroke.                                                    |
| 12.  | HadAsthma           | History of breathing problems.                                          |
| 13.  | HadSkinCancer       | History of skin cancer.                                                 |
| 14.  | HadCOPD             | History of lung disease.                                                |
| 15.  | HadDepressiveDisorder | History of depression.                                                |
| 16.  | HadKidneyDisease    | History of kidney problems.                                             |
| 17.  | HadArthritis        | History of joint pain.                                                  |
| 18.  | HadDiabetes         | History of high blood sugar.                                            |
| 19.  | DeafOrHardOfHearing | Hearing impairment or deafness.                                         |
| 20.  | BlindOrVisionDifficulty | Visual impairment or difficulty with vision.                        |
| 21.  | DifficultyConcentrating | Trouble in focusing.                                                |
| 22.  | DifficultyWalking   | Trouble walking.                                                        |
| 23.  | DifficultyDressingBathin | Trouble with self-care.                                            |
| 24.  | DifficultyErrands   | Trouble with daily tasks.                                               |
| 25.  | SmokerStatus        | Current or former or non-smoker status.                                 |
| 26.  | ECigaretteUsage     | Use of e-cigarettes.                                                    |
| 27.  | ChestScan           | History of chest imaging.                                               |
| 28.  | RaceEthnicityCategory | Racial and ethnic background.                                         |
| 29.  | AgeCategory         | Categorization of the individual's age into age ranges.                 |
| 30.  | HeightInMeters      | The individual's height is in meters.                                   |
| 31.  | WeightInKilograms   | The individual's weight is kilograms.                                   |
| 32.  | BMI                 | Body mass index.                                                        |
| 33.  | AlcoholDrinkers     | Alcohol consumption.                                                    |
| 34.  | HIVTesting          | History of HIV testing.                                                 |
| 35.  | FluVaxLast12        | Recent flu shot in last 12 months.                                      |
| 36.  | PneumoVaxEver       | History of pneumonia vaccination.                                       |
| 37.  | TetanusLast10Tdap 	 | Tetanus shot in the last 10 years.                                      |
| 38.  | HighRiskLastYear    | High-risk status in the previous year.                                  |t| 39.  | CovidPos 	         | COVID-19 positive status.                                               |sovidPos 	COVID-19 positive status.


