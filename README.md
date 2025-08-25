# Healthcare Provider Fraud Detection

##  Project Overview
This project focuses on detecting **fraudulent healthcare providers** using **Medicare claims data**. Fraudulent billing leads to billions in losses annually, and our project applies **machine learning techniques** to flag suspicious claims and providers. The work integrates multiple datasets, performs data preprocessing, feature engineering, exploratory analysis, and develops predictive models to support **fraud audits**.

Key Contributions:
- Integrated **inpatient, outpatient, beneficiary, and fraud label datasets** (558,000+ records, 55 features).
- Created engineered features like **claim duration, chronic condition counts, and provider patterns**.
- Applied **Decision Tree classifier with hyperparameter tuning** for interpretability and performance.
- Benchmarked results against Random Forest models.
- Achieved **90% accuracy, 88% recall, and 91% precision** in detecting fraud.


##  Project Structure
- `BA5200 healthcare_provider_fraud_detection_final_draft.ipynb` → Main Jupyter Notebook with data cleaning, feature engineering, model training, and evaluation.
- `Healthcare Provider Fraud Detection Project Report.pdf` → Full project documentation including methodology, results, and references.
- `BA5200 Project PPT.pptx` → Project presentation summarizing objectives, approach, and findings.
- `README.md` → This file.

##  Installation & Setup

### Requirements
- Python 3.8+
- Jupyter Notebook
- Libraries:
  ```bash
  pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn


### Dataset
The dataset consists of four main files:
- **InpatientData.csv** – Hospital admission claims.
- **OutpatientData.csv** – Outpatient claims.
- **BeneficiaryData.csv** – Demographics, chronic conditions, coverage.
- **Train-Labels.csv** – Fraud labels (Yes/No).


##  Running the Project
1. Open Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Run the notebook `BA5200 healthcare_provider_fraud_detection_final_draft.ipynb`.
3. Steps performed:
   - Merge datasets (inpatient, outpatient, beneficiary, labels).
   - Clean and preprocess (missing values, date conversions, encoding).
   - Feature engineering (claim duration, chronic condition count, is_dead, etc.).
   - Train/test split and hyperparameter tuning.
   - Evaluate models (Decision Tree & Random Forest).


## Results
- **Decision Tree (depth=13)**:
  - Accuracy: 90%
  - Recall: 88%
  - Precision: 91%
  - F1-score: 89%
  - ROC-AUC: ~0.91
- **Key Indicators of Fraud**:
  - Long claim durations
  - High reimbursement amounts
  - Multiple chronic conditions
  - Repeated physician use
  - Claims filed after patient death

##  Challenges & Limitations
- Imbalanced dataset (fewer fraudulent cases).
- Missing/incomplete fields like **date of death** and chronic condition flags.
- Risk of overfitting with deep models.
- Synthetic/curated nature of dataset may not reflect real-world complexity.


##  Ethical Considerations
- **Transparency**: Decision Tree chosen for interpretability.
- **Fairness**: Ensured race, gender, and age did not bias predictions.
- **False positives**: Focused on precision to minimize mislabeling non-fraudulent providers.
- **Human oversight**: Model designed to assist, not replace, auditors.


## References
- Chen, J., Sun, Y., Chen, X., & Chen, L. (2019). *Clinical data mining in healthcare: A comprehensive review.* Journal of Medical Systems.
- Katz, G. E., Butte, A. J., & Ghassemi, M. (2019). *The importance of feature engineering in healthcare data science.* Journal of Clinical Informatics.
- X. Doe et al. (2022). *Machine Learning in Clinical Decision Support: Current Trends and Challenges.* Journal of Healthcare Informatics.


## Team
- Karunakar Uppalapati
- Lenin Goud Athikam
- Saketha Kusu
- Varshitha Reddy Davarapalli
- Rashmitha Eri
- Kavya Pachchava
