# Detecting Healthcare Provider Fraud and Abuse Using Unsupervised Learning

## Project Overview:
This project aims to identify potential fraud and abuse among healthcare providers using the Medicare Inpatient Hospitals by Geography and Service dataset. The dataset includes information on hospital discharges, payments, and submitted charges for Medicare Part A beneficiaries, organized by geography and Medicare Severity Diagnosis Related Group (DRG).

By detecting fraudulent patterns and abuse in Medicare claims, this project helps healthcare organizations and insurers mitigate financial losses, reduce fraud-related costs, and improve resource allocation. Early identification of anomalies can also support regulatory compliance, ensure fair payment practices, and protect patients from unethical provider behavior, ultimately enhancing the sustainability and efficiency of healthcare systems.

### Key Objectives:
- **Exploratory Data Analysis (EDA):** Understand the dataset, identify key patterns, and visualize distributions to gain insights into the behavior of healthcare providers.
- **Feature Engineering:** Develop relevant features from the dataset that can enhance the effectiveness of unsupervised learning models in detecting anomalies.
- **K-Nearest Neighbors (KNN) and Principal Component Analysis (PCA):** Apply these unsupervised learning techniques to detect potential outliers and patterns that may indicate fraudulent or abusive behavior.
- **Anomaly Detection:** Identify providers whose billing practices significantly deviate from the norm, which could suggest fraud or abuse.

## Data Source:
The dataset used in this project is the **Medicare Inpatient Hospitals by Geography and Service** dataset. It provides information on hospital discharges, payments, and submitted charges by IPPS hospitals for Original Medicare Part A beneficiaries. The dataset can be found at: https://data.cms.gov/resources/medicare-inpatient-hospitals-methodology 

### Data Glossary:
- **Total Discharges:** The number of discharges billed by the provider for inpatient hospital services. Hospital discharge occurs when a patient leaves the hospital after treatment.
- **Covered Charges:** Charges for services that are covered by a health plan. Covered charges are the amount your health plan pays for, subject to any limits if the services are provided outside of the plan's network.
- **Total Covered Charge Amount:** The sum of all covered charges billed by the provider.
- **Average Covered Charges:** Calculated as the total covered charge amount divided by the total discharges. It represents the average amount billed for covered services per discharge.
- **Payment:** The amount a hospital actually receives for providing patient care. This includes payments from Medicare, Medicaid, private insurers, and the patient.
- **Average Total Payments:** The total payments divided by the total discharges, representing the average payment received per discharge.

## Project Workflow:

1. **Data Collection & Understanding:**
   - Load and inspect the dataset.
   - Conduct Exploratory Data Analysis (EDA) to understand key trends and relationships. 

2. **Feature Engineering:**
   - Create new features to capture the essence of potential fraudulent activities, such as ratios of submitted charges to payments and geographical charge variations.
   - Normalize and scale the data for better performance of unsupervised algorithms.

3. **Unsupervised Learning:**
   - **K-Nearest Neighbors (KNN):** Identify anomalies in the data by measuring the distance of each provider's practices from its nearest neighbors.
   - **Principal Component Analysis (PCA):** Reduce dimensionality to highlight the most important features contributing to potential fraud or abuse.

4. **Anomaly Detection:**
   - Apply the KNN and PCA models to detect outliers in the data.

### Technology and Package Used:
This project was developed using Python. The following Python packages were used in this project:
- **pandas:** For data manipulation and analysis.
- **numpy:** For numerical computing.
- **matplotlib & seaborn:** For data visualization.
- **scikit-learn:** For implementing machine learning algorithms, including KNN and PCA.
- **pyod:** For outlier detection in unsupervised learning.

