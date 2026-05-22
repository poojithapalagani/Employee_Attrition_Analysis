# Employee_Attrition_Analysis
Employee Attrition Prediction & workplace Analysis Report

1. Introduction
Employee attrition is a critical challenge for organizations, leading to increased recruitment costs, productivity loss, and knowledge gaps. This project aims to analyze employee data to understand key drivers of attrition and build machine learning models to predict which employees are at risk of leaving.
________________________________________
 2. Objective
•	Predict employee attrition (Yes/No) using classification models 
•	Identify key factors influencing employee turnover 
•	Segment employees using clustering techniques 
•	Provide actionable business insights for retention strategies 
________________________________________
 3. Dataset Overview
•	Total Records: 20,000 
•	Total Features: 29 
•	Target Variable: attrition (Yes/No) 
The dataset includes:
•	Demographic features (age, gender, marital status) 
•	Job-related features (department, job role, job level) 
•	Behavioral features (overtime, projects, training) 
•	Satisfaction metrics (job satisfaction, work-life balance) 
________________________________________
 4. Data Preprocessing
•	Removed irrelevant columns: 
o	employee_id 
o	join_date 
•	Converted target variable: 
o	Yes → 1, No → 0 (for analysis) 
•	Separated features into: 
o	Numerical features (scaled using StandardScaler) 
o	Categorical features (encoded using OneHotEncoder) 
•	Performed train-test split: 
o	80% training, 20% testing 
o	Used stratified sampling to maintain class balance 
________________________________________
 5. Exploratory Data Analysis (EDA)
 5.1 Attrition Distribution
•	No: ~60% 
•	Yes: ~40% 
 Indicates moderate class imbalance
________________________________________
 5.2 Department-wise Attrition
•	Marketing and HR showed slightly higher attrition rates 
________________________________________
 5.3 Overtime Impact
•	Employees working overtime had higher attrition (~42.7%) 
•	Indicates workload stress as a major factor 
________________________________________
 5.4 Correlation Insights
Key negative correlations with attrition:
•	Job Satisfaction 
•	Environment Satisfaction 
•	Work-Life Balance 
 Lower satisfaction leads to higher attrition
________________________________________
 6. Model Building
 6.1 Logistic Regression
•	ROC-AUC: ~0.59 
•	F1-score (Attrition): ~0.50 
 Moderate performance, struggled to capture complex patterns
________________________________________
 6.2 Random Forest
•	Default model biased toward majority class 
•	Very low recall for attrition class 
________________________________________
 6.3 Improved Model (Threshold Tuning)
•	Adjusted decision threshold from 0.5 → 0.3 
•	Improved recall significantly: 
Metric	Value
Recall (Attrition)	93%
F1-score	~0.57
 Model now captures most employees at risk
________________________________________
 7. Feature Importance Analysis
Top predictors identified:
1.	Monthly Income 
2.	Age 
3.	Distance from Home 
4.	Years at Company 
5.	Years with Current Manager 
6.	Training Frequency 
7.	Number of Companies Worked 
8.	Years Since Last Promotion 
9.	Number of Projects 
10.	Education 
________________________________________
 Business Interpretation
•	Lower salary → higher attrition 
•	Long commute → increased stress 
•	Lack of promotion → dissatisfaction 
•	High job switching history → instability 
________________________________________
🔹 8. Clustering Analysis
•	Applied KMeans clustering 
•	Optimal clusters determined using silhouette score 
 Silhouette Scores:
•	Best k = 2 (score ≈ 0.0995) 
________________________________________
 Cluster Results:
•	Cluster 0: 14,823 employees 
•	Cluster 1: 5,177 employees 
 Attrition Rate:
•	Cluster 0 → ~39.75% 
•	Cluster 1 → ~39.40% 
________________________________________
 Interpretation
•	Clustering did not produce distinct high-risk groups 
•	Attrition patterns are spread across the dataset 
•	Suggests attrition depends on multiple combined factors 
________________________________________
 9. Key Insights
•	Employee satisfaction is a major driver of attrition 
•	Overtime increases likelihood of leaving 
•	Compensation and career growth are critical 
•	No clear employee segments based on clustering 
________________________________________
 10. Business Recommendations
1.	Improve work-life balance 
2.	Reduce overtime workload 
3.	Provide regular promotions and career growth 
4.	Review compensation for at-risk employees 
5.	Focus on employee engagement programs 
6.	Monitor high-risk employees using predictive model 
________________________________________
 11. Conclusion
This project successfully demonstrated an end-to-end machine learning pipeline for employee attrition prediction. While baseline models showed limited performance, threshold tuning significantly improved recall, making the model useful for business decision-making. Clustering analysis indicated that attrition is influenced by multiple factors rather than distinct employee segments.

