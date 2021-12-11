![image](https://user-images.githubusercontent.com/82011523/145692633-5b8b49ec-a697-4645-a93e-977c5a4dc2f8.png)


# NLP_health_promotion_theory

## Purpose

The purpose of this study was to determine whether Natural Language Processing (NLP) trained on open-ended comments can be used to identify theoretical constructs associated with health behaviors.

## Theoretical Framework

The Health Action Process Approach (HAPA) suggests that the adoption, initiation, and maintenance of health behaviors must be explicitly conceived as a process that consists of at least a motivation phase and a volition phase (Schwarzer et al., 2014). Key constructs of the motivational phase include risk perceptions (i.e., perceived chances of an adverse health outcome) and positive outcome expectancies (i.e., positive health benefits), while one key construct of the volitional phase includes coping planning (i.e., a plan developed to cope with a challenging situation). 

## Participants

Participants were recruited via members of the [Mississippi Partnership for Comprehensive Control Control](https://msdh.ms.gov/msdhsite/index.cfm/43,0,292,426,html) Consortia. Eligibility included being diagnosed with a chronic health condition (e.g., cancer, diabetes, or cardiovascular disease).

## Data

A Qualtrics survey was developed to educate community members on the health benefits of diet and exercise as well as provide them with an opportunity to respond to questions in an open-ended format.  We adapted the questions from the original [evidence based materials](https://www.researchgate.net/publication/265972461_Multilingual_Brief_Interventions_Guided_by_HAPA). The questions gauged (1) their perceived risk to various health outcomes, (2) potential benefits associated with a healthy lifestyle, and (3) a plan developed to cope with a challenging situation that interferes with being active or consuming a healthy meal. The data were coded to reflect the constructs listed above.  In total, there were over 1000 comments. Rows with missing data and irrelevant comments were removed. 

## Statistical Analysis

The NLTK package in Python was used to train three different machine learning models (i.e., Naive Bayes, Decision Tree, and Random Forest). The data was pre-processed by removing stop words, converting text to numerical data (i.e., countvectorizing), creatting a bag-of-words to reduce redundancy, and split data into training and testing samples. Estimates of accuracy were computed for the training and testing samples and average estimates of percision, recall, and F1 were computed for the testing samples.   

## Results

Accuracy for the testing sample ranged from 0.733 for Naive Bays to 0.85 for Random Forest.  Average precision, recall and f1-scores were highest for Random Forest.  See the tables below. 

![image](https://user-images.githubusercontent.com/82011523/145693130-e73674b4-6e62-4a82-9249-663feab2021f.png)

![image](https://user-images.githubusercontent.com/82011523/145693136-0cfb165d-ab6f-410a-b663-6002d4e667d1.png)

![image](https://user-images.githubusercontent.com/82011523/145693143-b814be8d-60c5-40fb-b65f-b6f44bdacbf0.png)

## Summary

On average model accurace was highest for the Decision Tree and Random Forest models.  However, estimates of accuracy for the training samples were high (~98%) suggesting over fitting.  Over fitting may suggest that the models may not be generalizable to other samples.  This project could be extended by exploring other Python packages such as Spark-NLP or apply deep learning, which may perform better.   

