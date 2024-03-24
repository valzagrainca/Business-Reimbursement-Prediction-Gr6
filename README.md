# Predicting Business Reimbursements using Machine Learning

## University and Course Information
- **University:** University of Pristina
- **Faculty:** Faculty of Electrical and Computer Engineering
- **Level:** Master's
- **Lecture:** Machine Learning
- **Lecturer:** Prof.Dr.Ing. Lule Ahmedi, PhD.c Mërgim H. HOTI
- **Students:** Valëza Grainca and Artan Thaqi

## Dataset Details
- **Source:** [ATK Open Data](https://www.atk-ks.org/en/open-data/)
- **Description:** The dataset comprises reimbursement requests and approvals for businesses operating in Kosovo
- **Size:** 4018 rows
- **Attributes:** 14
- **Format:** Excel

## Overview
This project aims to develop a machine learning model capable of predicting the reimbursement amounts for businesses. By leveraging historical data on business expenses and reimbursements, the model will learn patterns and relationships to make accurate predictions. This predictive tool can assist businesses in budgeting, financial planning, and optimizing reimbursement processes.

## Phase 1
### Key Steps
1. **Data Cleaning:**
   - **Data Quality Check:** Evaluate the overall quality of the dataset, including data types, consistency, and completeness.
   - **Data types:**
     - **Viti:** Categorical - Ordinal
     - **Muaji:** Categorical - Ordinal
     - **Sektori:** Categorical - Nominal
     - **Komuna:** Categorical - Nominal
     - **Numri i Kërkesave:** Numerical - Discrete
     - **Vlera e Kërkura:** Numerical - Continuous
     - **Numri i Kërkesave të Aprovuara:** Numerical - Discrete
     - **Vlerat e Aprovuara:** Numerical - Continuous
     - **Tatimpaguesve në kategorinë A:** Categorical - Nominal (Binary)
     - **Tatimpaguesve në kategorinë B:** Categorical - Nominal (Binary)
     - **Tatimpaguesve në kategorinë C:** Categorical - Nominal (Binary)
     - **Mesatarja e Ditëve të Kthimit:** Numerical - Continuous
     - **Lloji i Formularit të Deklarimit:** Categorical - Nominal
   - **Check for Null Values:** Identify and handle missing values appropriately. In this dataset, there are no null values, so no method is applied to handle them.
   - **Find and Remove Outliers:** Detect outliers using z-score. Remove or adjust outliers to prevent them from skewing the model's predictions.

     **Before Removing Outliers**

     ![Before Removing Outliers](https://github.com/valzagrainca/Business-Reimbursement-Prediction-Gr6/assets/46811308/4cd84e91-dd00-463f-a74d-b8765e364a18)

     **After Removing Outliers**

     ![After Removing Outliers](https://github.com/valzagrainca/Business-Reimbursement-Prediction-Gr6/assets/46811308/c8110479-18e2-43e4-8d8b-ff98baf1c6d3)

   - **Apply SMOTE (Synthetic Minority Over-sampling Technique):** Dealing with imbalanced classes, apply SMOTE to oversample the minority class and balance the dataset, enhancing the model's ability to learn from minority instances effectively. This technique targets the 'Sektori' as an imbalanced class. We can see the result before and after applying the SMOTE technique.

   **Before SMOTE**

   ![Before SMOTE](images/BeforeSMOTE.png)

   **After SMOTE**

   ![After SMOTE](images/AfterSMOTE.png)

   - **Identify Skewed Data:** Analyze the distribution of numerical features to identify skewed data. As we see in our numerical columns, the data is right-skewed.

   ![Skewed Data 1](https://github.com/valzagrainca/Business-Reimbursement-Prediction-Gr6/assets/46811308/cbfd929d-7d64-4d5c-ace2-827d9acc7135)
   ![Skewed Data 2](https://github.com/valzagrainca/Business-Reimbursement-Prediction-Gr6/assets/46811308/7d4f0beb-a053-43a1-8fd3-34abdd636bcd)
   ![Skewed Data 2](https://github.com/valzagrainca/Business-Reimbursement-Prediction-Gr6/assets/46811308/853df3d5-7f3b-4e15-a6f8-26fa5c4d0430)

