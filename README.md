# Diabetes Readmittance

<center><img src="https://images.unsplash.com/photo-1532938911079-1b06ac7ceec7?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1000&q=80" style="zoom:60%;" /> </center> 

Read the full report [here](https://dannydhkim.github.io/DiabetesReadmittance)

## Motivation

Hospital readmissions are incredibly damaging on multiple fronts: healthcare cost, patient health, and time spent. By diagnosing which factors contribute to the hospital readmission rate, we will be able to tackle the problem head-on to bring about a huge boon to an already congested healthcare system in the United States. We especially focus on diabetes because there is relatively little research focused on hospitalized diabetes patients even though the burden of the cost of constant returns are rising significantly. By predicting whether or not a patient will be readmitted in the future, medical professionals can be alerted to prevent future readmissions by changing their treatment or expectations with a patient. 

## Data Acquisition

The data was acquired by using the UCI machine learning repository database. The dataset is described to be 10 years of clinical care at 130 US hospitals with 50 features representing patient and hospital outcomes. For further detail, check the reference below.

## Results

| Model               | Cross Validation Score | Precision | Recall | AUC Train | AUC Test | Fit Time |
| ------------------- | ---------------------- | --------- | ------ | --------- | -------- | -------- |
| Linear SVM (w/ SGD) | 55.21%                 | 0.70      | 0.10   | 0.51      | 0.51     | 15.5s    |
| Decision Tree       | 60.21%                 | 0.58      | 0.53   | 0.59      | 0.71     | 0.818s   |
| KNN                 | 56.48%                 | 0.57      | 0.38   | 0.51      | 0.65     | 7.6s     |
| Naive Bayes         | 59.99%                 | 0.56      | 0.58   | 0.52      | 0.60     | 6.33s    |
| Logistic Regression | 61.91%                 | 0.62      | 0.45   | 0.54      | 0.61     | 1.92s    |
| Random Forest       | 62.89%                 | 0.62      | 0.48   | 0.54      | 0.63     | 0.672s   |
| XGBoost             | 63.62%                 | 0.62      | 0.53   | 0.55      | 0.64     | 37.6s    |

<center><img src="Figures\ROC_Curve_Analysis.png" alt="Precision-Recall_Curve_Analysis" style="zoom:67%;" /> </center>

<center><img src="Figures\Feature_Importances.png" alt="Feature_Importances" style="zoom: 80%;" /> </center>

## Conclusion

**Winner - XGBoost Model**

My recommendation for a hospital is to have a system that monitors (at least) the top 5 most important features of patients. Changing the workflow to double check and give extra care to these patients so that they do not have to be readmitted could prevent future work and patient health being compromised.

## References

Felix, Holly C., et al. “Why Do Patients Keep Coming Back? Results of a Readmitted Patient Survey.” *Social Work in Health Care*, vol. 54, no. 1, 2015, pp. 1–15., doi:10.1080/00981389.2014.966881. 

“In Focus: Preventing Unnecessary Hospital Readmissions.” *Commonwealth Fund*, www.commonwealthfund.org/publications/newsletter-article/focus-preventing-unnecessary-hospital-readmissions. 

Strack, Beata, et al. “Impact of HbA1c Measurement on Hospital Readmission Rates: Analysis of 70,000 Clinical Database Patient Records.” *BioMed Research International*, vol. 2014, 2014, pp. 1–11., doi:10.1155/2014/781670. 