## Predictive Analysis of Student Academic Performance Using Classification Models
### Author
**Zegedam Zegeye**
### Executive Summary
This project aims to evaluate various classification models to predict student academic performance and identify the key factors that contribute to student failure. By analyzing these factors, schools can implement targeted interventions to help improve student outcomes.

### Rationale
Understanding the reasons behind student failure is critical for educators, policymakers, and stakeholders. Identifying key factors that influence student performance will enable educators to design targeted interventions that can support at-risk students and improve overall academic outcomes while also optimizing resource allocation by identifying students who need additional support early on.

### Research Question
What are the most significant factors contributing to student failure, and how can classification models be used to predict academic performance?

### Data Sources
The dataset includes information collected through school reports and questionnaires, encompassing a wide range of features such as student grades, demographics, social factors, parental involvement, and school-related attributes. For this analysis, we'll be exploring Math grades as they are a standart learning material across the world. 

The link to the data source can be found here from Kaggle: https://www.kaggle.com/datasets/dillonmyrick/high-school-student-performance-and-demographics?resource=downloadLinks

citation: P. Cortez and A. Silva. Using Data Mining to Predict Secondary School Student Performance. In A. Brito and J. Teixeira Eds., Proceedings of 5th FUture BUsiness TEChnology Conference (FUBUTEC 2008) pp. 5-12, Porto, Portugal, April, 2008, EUROSIS, ISBN 978-9077381-39-7.

### Methodology
* **Data Preprocessing:** Cleaning and preparing the data for analysis.

* **Feature Selection:** Identifying the most relevant features that impact student performance.

* **Model Evaluation:** Training and evaluating four classification models - Logistic Regression, Support Vector Classifier (SVC), K-Nearest Neighbors (KNN), and Decision Tree.

* **GridSearchCV:** Optimizing hyperparameters to improve model performance.

* **Feature Importance Analysis:** Extracting and interpreting feature importance from the best-performing model.

### Results
Baseline score using Dummy Classifier: 0.63

After evaluating four classification models—Logistic Regression, Support Vector Classifier (SVC), K-Nearest Neighbors (KNN), and Decision Tree—on the given dataset, the following results were obtained:
| **Model**                 | **precision** | **recall** | **F1-score** | **average fit time** |
|---------------------------|---------------|------------|--------------|----------------------|
| Logistic Regression       | 0.92          | 0.93       | 0.92         | 0.017                |
| Decision Tree             | 0.88          | 0.88       | 0.88         | 0.005                |
| Support Vector Classifier | 0.88          | 0.88       | 0.88         | 0.006                |
| K-Nearest Neighbors       | 0.87          | 0.86       | 0.87         | 0.009                |

__Logistic regression:__ Was the best model with an average train score of 0.973 and a test score of 0.929. Despite the longer fit time of 0.017 seconds, the good performance of the test represents a good balance between fitting the training data.

__Decision Tree:__ Achieved a perfect train score of 1.000 but had an average lower test score of 0.88, indicating potential overfitting.It had the lowest average fit time of all models at 0.005 seconds.

__Support Vector Classifier (SVC):__ Obtained a perfect train score of 1.000 and also performed similarly on the test data with an average score of 0.88.  Its average fit time was the second lowest at 0.006 seconds.

__K-Nearest Neighbors (KNN):__  Similarly achieved a perfect train score of 1.000 but had the lowest test score of 0.87, suggesting overfitting. Its average fit time was 0.009 seconds.

The Logistic Regression model emerged as the best-performing model with a test score of 0.92. The key factors identified as contributing to student failure are:

| Importance Features             |
|---------------------------------|
| Father's job status             |
| Father's education level        |
| Quality of family relationships |
| Study time (less than 2 hours)  |
| Weekend alcohol consumption     |

Based on these findings, schools can implement targeted interventions to address these issues and improve student outcomes.

### Next Steps
* **Implement Intervention Programs:** Develop and deploy targeted intervention programs focusing on the identified key factors.
* **Further Research:** Conduct longitudinal studies to monitor the effectiveness of interventions and refine them as needed.
* **Expand the Dataset:** Incorporate additional data sources including other subjects

* **Model Refinement:** Continue to refine and test new machine learning models to improve predictive accuracy.
* **Policy Recommendations:** Provide actionable insights and policy recommendations to educational institutions and policymakers based on the findings.

### Outline of project
Detailed technical investigation can be found here: [Jupyter Notebook](https://github.com/Ziggy-Z/Capstone-Project/blob/main/Capstone_Project_20.1.ipynb)