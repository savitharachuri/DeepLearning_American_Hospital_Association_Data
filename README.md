# DeepLearning American Hospital Association Data

### Project Description

This project utilizes American Hospital Association (AHA) survey data to analyze hospital staffing levels, market concentration, and hospital clustering. The objective is to leverage machine learning techniques to classify hospitals based on staffing adequacy and identify market competition levels using the Herfindahl–Hirschman Index (HHI). The analysis aids in understanding hospital workforce management and competition within different geographical regions.

### Methodology

- Data Preprocessing:
AHA survey data from 1996 to 2020 was processed, selecting relevant features such as number of beds, inpatient days, expenses, and payroll data.
Missing values were handled by replacing NaNs with zero where necessary to maintain data integrity.
- Deep Learning and Machine Learning Models for Staffing Classification:

The dataset was divided into training and test sets (2005–2018 data) to predict whether a hospital is understaffed.
Various classification models were tested, Deep Learning with TensorFLow framework and Machine Learning models including GaussianNB, BernoulliNB, KNeighborsClassifier, SVC, MultinomialNB, and VotingClassifier.
The VotingClassifier with soft voting achieved the highest accuracy (~90%) in classifying hospital staffing adequacy.

- Hospital Market Clustering & HHI Calculation:

K-Means Clustering was applied using hospital geographic coordinates (latitude and longitude) to identify distinct hospital clusters.
The HHI index was calculated based on the total number of beds in each cluster to measure market competition.
A topographical map visualization was created using Folium to display hospital clusters and their respective HHI values.

- Results

The VotingClassifier model successfully classified hospitals as understaffed with 90% accuracy.
Deep Learning classification achieved the R-squared metric 92%.
K-Means clustering identified 16 hospital clusters, each with a calculated HHI index to assess market competition.
Geospatial visualization provided insights into hospital distribution and competition levels across regions.

- Recommendations
Integrate Additional Datasets: Combining AHA data with CMS (Centers for Medicare and Medicaid Services) impact files and Electronic Health Records (EHRs) could improve predictive accuracy for hospital workforce and financial insights.
Refine Staffing Models: Future work should focus on department-level staffing predictions to optimize resource allocation, particularly in rural hospitals facing critical understaffing issues.
Policy and Decision-Making Support: Policymakers and healthcare administrators can leverage these insights to improve hospital workforce planning and resource distribution, ensuring better healthcare service availability.
