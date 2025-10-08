HOME LOAN ELIGIBILITY ANALYSIS

OVERVIEW:

This project analyses historical home loan application data to predict applicant eligibility. Key factors such as income, credit history, employment, loan amount, and property type are examined to uncover patterns influencing loan approval. 

By applying data analytics and machine learning, the project help banks make faster, data-driven decisions, manage risk, and optimize loan offerings, while providing applicants with insights to improve their chances of approval.

OBJECTIVES:
- Explore and understand the loan dataset.
- Clean and preprocess raw data for analysis.
- Identify important factors influencing loan approval.
- Build predictive models to classify loan applications as Approved/Not Approved.
- Compare models and recommend the best-performing approach.

SIGNIFICANCE OF OBJECTIVE:
- Faster & Consistent Approvals: Reduce manual evaluation time and human bias.
- Risk Management: Identify low-risk vs high-risk applicants to minimize defaults.
- Improved Customer Experience: Provide pre-approval insights and guidance.

PROJECT BENEFITS:
- Risk Management: Reduce loan defaults by identifying risk profiles.
- Faster Loan Processing: Automate eligibility checks and minimize human error.
- Better Loan Products: Tailor offerings based on applicant insights.
- Applicant Guidance: Suggest improvements for better approval chances.
- Foundation for Predictive Analytics: Enable future models for demand forecasting and personalized products.
  
DATASET:
Example Fields:
- applicant_id
- age
- gender
- marital_status
- annual_income
- employment_type (e.g., Salaried, Self-employed)
- years_in_current_job / years_in_business
- employer_name / business_name
- credit_score
- existing_loans_amount
- total_debt
- debt_to_income_ratio
- property_value
- property_type (e.g., Residential, Commercial)
- property_location (city, state, or coordinates)
- down_payment_amount
- loan_amount
- loan_tenure_years
- residency_status (e.g., Resident, NRI)
- nationality
- employment_stability_years
- proof_of_income_submitted (Yes/No)
- property_documentation_submitted (Yes/No)
- property_legal_clearance (Yes/No)

METHODOLOGIES:
1.	Data Collection
- Collect home loan dataset from Kaggle / sample bank records.
- Load data into Python (pd.read_csv) and saved a raw copy.
- Record source and columns for reproducibility.
  
2.	Data Cleaning
- Handle missing values, duplicates, and inconsistent entries.
- Impute numerical features with median and categorical features with mode.
- Save cleaned dataset for further analysis (data/processed/).

3.	Exploratory Data Analysis (EDA)
- Visualize distributions of applicant income, loan amount, credit history, and loan status.
- Explore relationships between features and loan approval outcomes.
- Document key insights to guide feature engineering.

4.	Feature Engineering
  Create new features such as:
- TotalIncome = ApplicantIncome + CoapplicantIncome
- Debt-to-Income ratio (DTI) = LoanAmount / TotalIncome
- Binary signals like Has_Coapplicant and Good_Credit_High_Income.
- Apply transformations to reduce skew (e.g., log transform of loan amount).
- Verify feature usefulness through summary statistics and plots.
  
5.	 Modeling — Logistic Regression
- Fit Logistic Regression as a baseline model.
- Examine feature coefficients to understand their impact on approval.
- Evaluate accuracy, precision, recall, and F1-score.

Logistic Regression Accuracy: 83.7%

Logistic Regression F1-Score: 89%

6.	Modeling — Random Forest
- Train Random Forest to capture non-linear relationships and interactions.
- Check feature importance to identify key factors influencing eligibility.
- Tune hyperparameters (n_estimators, max_depth) for improved performance.

Random Forest Accuracy: 86.1%  
Random Forest F1-Score: 91%

7.	Model Evaluation
- Calculate metrics: accuracy, precision, recall, and F1-score.
- Visualize confusion matrix to understand approval/rejection errors.
- Select evaluation metrics based on business impact considerations.
  
8.	 Model Comparison
- Compare Logistic Regression vs Random Forest on test performance metrics.
- Visualize results through tables and charts for clarity.
- Consider interpretability vs accuracy to guide the final decision.
  
9.	Final Recommendation
- Recommend the most suitable model balancing accuracy and interpretability.
- Suggest future improvements: adding features, trying boosting models, and monitoring in production.
- Optionally create Power BI dashboard for stakeholder-friendly visualizations.

TOOLS AND TECHNOLOGIES:
- Programming: Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Joblib).
- Programming Environment: Jupyter Notebook, Git & GitHub.   
- Data Visualization: Power BI 
- Data Storage: CSV / SQL database.
- Documentation: Jupyter Notebooks, Markdown reports.

PROJECT WORKFLOW:

Raw Data → Data Cleaning → EDA → Feature Engineering → Model Building (Logistic Regression & Random Forest) → Model Evaluation → Model Comparison → Final Report

Deliverables
- Cleaned and preprocessed dataset ready for analysis.
- Jupyter Notebook containing EDA, feature engineering, and model building steps.
- Predictive model for home loan eligibility.
- Visualizations and insights highlighting key factors influencing loan approvals.
- Summary report with actionable recommendations.

Conclusion
-  The Home Loan Eligibility Analysis project successfully demonstrates how data analytics and machine learning can streamline the loan approval process for financial institutions.
-  After collecting, cleaning, and exploring the dataset, two predictive models — Logistic Regression and Random Forest Classifier — were developed and evaluated to predict whether a loan application would be approved.
-  The Random Forest model achieved higher accuracy and stronger recall compared to Logistic Regression, indicating better generalization and improved capability to correctly identify approved loan cases.
-  The Random Forest model is selected as the final model due to its superior accuracy (86%) and recall (99% for approved cases).
-  It is recommended for use in pre-screening applicants before manual evaluation, ensuring faster and more reliable loan decisions.
















