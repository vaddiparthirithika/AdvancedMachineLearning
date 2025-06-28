#Easy Visa - Visa Approval Prediction using Advanced Machine Learning

##Problem Statement

The objective of this project is to develop a machine learning classification model to:

- Facilitate and automate the visa approval process.
- Recommend whether a visa application should be **Certified** or **Denied**.
- Identify key drivers that influence the decision to **approve or reject** a visa application.

---

##Data Dictionary

| Feature                 | Description |
|-------------------------|-------------|
| `case_id`               | Unique ID for each visa application |
| `continent`             | Continent of the applicant |
| `education_of_employee` | Education level of the employee |
| `has_job_experience`    | Whether the applicant has prior job experience (Y/N) |
| `requires_job_training` | Whether the applicant requires job training (Y/N) |
| `no_of_employees`       | Company size in terms of number of employees |
| `yr_of_estab`           | Year of establishment of the employer’s company |
| `region_of_employment`  | Region in the US where the job is located |
| `prevailing_wage`       | Average wage paid to similar workers in the same location |
| `unit_of_wage`          | Wage unit (Hourly/Weekly/Monthly/Yearly) |
| `full_time_position`    | Whether the job is full-time (Y/N) |
| `case_status`           | Target variable – Certified or Denied |

---

##Tools & Technologies Used

- **Python**  
- **Libraries**: `pandas`, `numpy`, `seaborn`, `matplotlib`, `scikit-learn`, `imblearn`
- **Models**:  
  - Decision Tree  
  - Random Forest  
  - Bagging  
  - AdaBoost  
  - Gradient Boosting
- **Techniques**:  
  - Hyperparameter tuning with GridSearchCV & RandomizedSearchCV  
  - SMOTE (oversampling) & RandomUnderSampler (undersampling)  
  - Evaluation using F1-score, Accuracy, Precision, Recall, Confusion Matrix

---

##Exploratory Data Analysis

- Balanced and imbalanced dataset behavior analyzed
- Features like education level, wage unit, region of employment, and experience show significant impact
- SMOTE oversampling applied to address class imbalance

---

##Model Performance (Original Dataset - Test F1 Score)

| Model                  | Performance |
|------------------------|-------------|
| Gradient Boosting      | Best |
| Random Forest          | High |
| Bagging Classifier     | Good |
| AdaBoost               | Moderate |
| Decision Tree          | Basic |

---

## Key Drivers of Visa Certification

- **Education**: Bachelor's or Master's preferred  
- **Job Experience**: Having prior experience significantly improves chances  
- **Prevailing Wage**: Certified applicants had a median wage of ~$72k  
- **Wage Unit**: Yearly wages are preferred over hourly  
- **Region of Employment**:  
  - **Mid-West** has highest approval rates  
  - Bachelor's: South & West regions  
  - Master's: Northeast & South  
  - Doctorate: West & Northeast  
- **Continent of Origin**:  
  - Higher certifications: Europe, Africa, Asia  
  - More denials: South & North America, Island regions

---

## Patterns in Visa Denials

- High School degree = higher denial probability  
- Hourly wage applicants are rarely approved  
- Lack of job experience contributes to rejection  
- Applicants from island regions show high denial rates  

---

## Business Recommendations

- Focus outreach on applicants with **Graduate degrees**, **job experience**, and **yearly wages**.
- Improve visa support for skilled candidates from Europe, Asia, and Africa.
- Encourage employers in the Mid-West and Northeast to streamline visa applications.
- Introduce training programs or partnerships to upskill high school degree holders.
- Enhance digital automation tools to aid in early filtering of high-potential applicants.

---

## Files Included

- `easy_visa.ipynb` – Notebook with full pipeline
- `easy_visa.html` – Exported view-only version of the notebook
- `README.md` – Project documentation
-  Input Dataset

---

## How to Run

1. Clone this repository or download the `.ipynb` file
2. Open in **Google Colab** or **Jupyter Notebook**
3. Install dependencies (if needed):  
   `pip install pandas numpy scikit-learn imblearn seaborn matplotlib`
4. Run cells sequentially

---

## Future Enhancements

- Explore XGBoost or LightGBM for model improvement
- Build a web dashboard using Streamlit for visa application prediction
- Perform country-level analysis if location data is extended
