<!-- This README is intended for use in a portfolio repository to accompany the project assets from the BITS Pilani MSc Artificial Intelligence and Data Science programme. It describes the context, objectives and methodology of a customer‑segmentation project built on the Brazilian E‑commerce public dataset. Feel free to adapt the language to suit your own voice and update any sections (for instance results or future improvements) based on your actual findings. Keep the tone professional and emphasise the business relevance of the work. -->
Customer Segmentation for Brazilian Online Retail
1 Overview

This project addresses a common challenge in online retail: a one‑size‑fits‑all marketing approach fails to account for diverse customer behaviour. By leveraging the Brazilian E‑Commerce Public Dataset (Olist) from Kaggle, we built a data‑driven customer segmentation model that groups customers into meaningful segments based on purchasing patterns, payment methods and review history. The goal is to enable marketing teams to deploy targeted campaigns, improving engagement and repeat purchase rates while optimising marketing spend.

2 Business Goal

The primary objective is to develop a machine‑learning‑based segmentation model that:

Accurately identifies distinct customer groups using behavioural and transactional attributes.
Supports personalised marketing and retention strategies by assigning each customer to a segment with a clear behavioural persona (e.g. high‑value loyalists, bargain hunters, dormant buyers).
Improves customer satisfaction and revenue through tailored messaging rather than generic campaigns.
3 Data Source
Dataset: Brazilian E‑Commerce Public Dataset (Olist).
Scope: ~100 k orders with customer profiles, order payments, product information, seller data and customer reviews.
Access: Available on Kaggle – Olist Brazilian E‑Commerce dataset
.

The dataset offers a comprehensive, multi‑table view of the Brazilian marketplace, making it suitable for building real‑world customer personas.

4 Tools and Technologies
Programming: Python (Jupyter / Colab)
Libraries: pandas, numpy, scikit‑learn, matplotlib, seaborn
Development environment: Google Colab / Jupyter Notebook, Visual Studio Code
Business intelligence: Tableau / Power BI for dashboarding
5 Project Workflow

The project followed a typical data‑science lifecycle with the following phases:

Data Acquisition & Integration:
Download dataset via Kaggle API.
Load multiple tables (orders, customers, payments, reviews).
Validate schemas and join keys to merge tables into a unified data frame.
Data Cleaning & Pre‑processing:
Handle missing values, duplicates and outliers.
Normalise formats (dates, categories) and encode categorical variables.
Exploratory Data Analysis (EDA):
Visualise distributions, trends and anomalies using Matplotlib/Seaborn.
Identify behavioural patterns across customers, orders and reviews.
Feature Engineering:
Derive RFM (Recency, Frequency, Monetary) metrics.
Aggregate review scores and payment information.
Create customer‑level features to capture purchasing behaviour.
Clustering Model Development:
Apply clustering algorithms such as K‑Means, Hierarchical Clustering and DBSCAN.
Tune parameters using the Elbow Method and Silhouette Score.
Compare cluster stability across models.
Cluster Evaluation & Interpretation:
Validate clusters using internal metrics (Silhouette Score, Davies–Bouldin Index).
Map clusters to business personas (e.g. high‑value loyalists, bargain hunters, dormant customers).
Document actionable insights for marketing and product teams.
Dashboard & Reporting:
Develop interactive dashboards in Tableau or Power BI to summarise findings.
Present cluster profiles, key KPIs and campaign suggestions to business stakeholders.
6 Approach & Methodology
Data Preparation – We began by downloading the dataset via the Kaggle API, loading each table into pandas DataFrames and merging them into a consolidated customer‑order view. During this step we performed data quality checks, handled missing values, removed duplicates and corrected data types.
Feature Engineering – To capture meaningful customer behaviour we engineered RFM features (recency, frequency, monetary value) along with aggregate review scores, payment method counts and average order values. Categorical variables were encoded appropriately.
Model Selection – Multiple clustering algorithms were trialled. We started with K‑Means (tuned via the Elbow Method), then compared performance against Hierarchical Clustering and DBSCAN. Silhouette Score and Davies–Bouldin Index guided the choice of the final model.
Cluster Interpretation – Each cluster was profiled by analysing RFM statistics and other features. For example, one cluster contained high‑value loyalists with frequent purchases and positive reviews, while another comprised price‑sensitive casual buyers with low purchase frequency and higher return rates. These personas informed targeted marketing strategies.
Communication – A final presentation deck summarised the problem, methodology, results and recommendations. Dashboards built in Tableau/Power BI allow business stakeholders to interact with the clusters and derive insights.
7 Project Assets

This repository (when created) should include the following artefacts:

Notebook / Script: The Python notebook (*.ipynb) or exported script used for data loading, EDA, feature engineering and clustering model development. In this case, a Python script (data_dynamics_apex_project_v5_1.py) converted from the original Colab notebook captures the full workflow.
Report: A PDF document explaining the problem statement, business goal, data source, methodology, results and conclusions (e.g. DataDynamics_Apex_Project_Trem1.pdf).
Presentation: A slide deck summarising the project and recommendations for the business audience (e.g. DataDynamics_Apex_1.pptx).
Schema / Data dictionary: An optional Excel or PDF file describing each field in the dataset.
README.md: This README file.

Please avoid uploading large raw datasets. Since the Olist dataset is publicly available on Kaggle, include a link and instructions for users to download it themselves.

8 How to Run This Project
Clone or download this repository.
Create a Python virtual environment and install dependencies using the provided requirements.txt (to be generated if needed).
Download the Brazilian E‑Commerce dataset from Kaggle using the Kaggle API (kaggle datasets download -d olistbr/brazilian-ecommerce). Unzip the files into a data/ directory.
Run the notebook (.ipynb) or Python script. Follow the code sections for data cleaning, feature engineering and clustering. Adjust parameters if you wish to experiment with different models.
Open the Tableau/Power BI dashboards (if provided) to explore the clusters interactively.
9 Future Improvements
Model evaluation: Experiment with additional clustering algorithms such as Gaussian Mixture Models and spectral clustering, and evaluate using cross‑validation or external labels if available.
Feature enrichment: Incorporate more behavioural signals such as customer service interactions or product categories to refine personas.
Deployment: Package the segmentation pipeline into a reusable module or API for integration with marketing platforms.
Dashboard enhancements: Build a web‑based dashboard (e.g. using Streamlit) for interactive analysis without requiring Tableau/Power BI.
10 License and Acknowledgements

This project is for educational purposes as part of the BITS Pilani MSc Artificial Intelligence and Data Science programme. The dataset is provided by Olist and available under their respective terms on Kaggle. All code and documents here are released for demonstration; please respect the dataset's licence when using it in your own work.
