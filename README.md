# Job Post Classification: Identifying Real vs. Fake Jobs

## Overview

Employment scams have surged significantly. CNBC reported that the number of employment scams doubled from 2017 to 2018. The current economic landscape, worsened by the COVID-19 pandemic, has heightened unemployment rates and reduced job availability, creating fertile ground for scammers. Desperate job seekers are being targeted, with scammers exploiting their vulnerability to steal personal information such as addresses, bank details, and social security numbers.

As a university student, I've received numerous scam emails offering attractive job opportunities, only to demand money or investments later. This project leverages Machine Learning and Natural Language Processing (NLP) techniques to tackle this issue.

## Project Stages

This project utilizes job posting data from Kaggle, categorized as either real or fake. The methodology involves five key stages:

1. **Problem Definition:** Establishing the project overview, statement, and metrics.
2. **Data Collection:** Gathering the necessary dataset.
3. **Data Cleaning and Exploration:** Preprocessing the data for analysis.
4. **Modeling:** Developing predictive models.
5. **Evaluation:** Assessing model performance.

## Problem Statement

The goal is to develop a classifier that can distinguish between real and fake job postings. The final model will integrate outputs from two different models: one handling numeric data and the other handling text data.

## Metrics

Two primary metrics will evaluate model performance:

- **Accuracy:** Measures the ratio of correctly classified instances to total instances.
- **F1-Score:** Balances precision and recall, crucial due to the importance of correctly identifying both real and fake jobs.

## Data Analysis

### Data Exploration

The dataset, sourced from Kaggle, contains 17,880 observations and 18 features, including text, binary, and integer data types. Key variables include job ID, title, location, department, salary range, company profile, job description, requirements, benefits, and more.

### Data Cleaning

Certain columns, like department and salary range, with significant missing values, were dropped. The focus was narrowed to US-based job postings, ensuring all data was in English. The cleaned dataset comprised 10,593 observations and 20 features, with a 93% to 7% ratio of real to fake jobs.

### Exploratory Analysis

- **Location Analysis:** Identified states and cities with higher occurrences of fake jobs.
- **Employment Type and Education:** Analyzed the distribution of fake jobs across job types and required education levels.

### Text Processing

Combined text fields (e.g., title, location, company profile) into a single field and analyzed character counts, noting differences between real and fake job postings.

## Algorithms and Techniques

The project employs:

- **Naive Bayes:** As the baseline model, suitable for its ability to compute conditional probabilities.
- **SGD Classifier:** For its flexibility in supporting various loss functions and penalties, critical for handling class imbalances.

Both models are evaluated on accuracy and F1-scores, with the final model being a combination of text and numeric data analyses.

## Benchmark and Methodology

- **Benchmark Model:** Naive Bayes with an accuracy of 0.971 and an F1-score of 0.744.
- **Implementation:** Data is split into training and test sets, with text data converted into a term-frequency matrix. The final model, selected based on performance metrics, combines results from both numeric and text analyses.

## Results

### Model Evaluation

The SGD classifier outperformed the baseline Naive Bayes model, achieving an accuracy of 0.974 and an F1-score of 0.79. The final model was chosen based on these improved metrics.

### Confusion Matrix

The confusion matrix revealed that the model accurately identified real jobs 99.01% of the time but was less effective at identifying fake jobs, with a 73.5% accuracy. This underscores the challenge of class imbalances in machine learning.

## Reflection and Improvements

This project highlights the importance of addressing employment scams through advanced techniques. Key insights include the prevalence of fraudulent jobs in specific locations and among entry-level positions. The text preprocessing phase was particularly challenging due to the diverse data formats.

## Future Improvements

To enhance model performance, addressing the dataset imbalance is crucial. Techniques like SMOTE (Synthetic Minority Over-sampling Technique) can generate synthetic samples for the minority class, potentially improving the identification of fake jobs.
