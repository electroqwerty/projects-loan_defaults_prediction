# Loan Default Prediction - Capstone Project

## Project Overview

This repository hosts a machine learning project focused on predicting loan defaults. It's part of a proof of concept (POC) for a startup targeting retail banking risk assessment. The primary dataset used is `applications_train.csv`, with an emphasis on selecting key features, developing predictive models, and thorough data analysis. The main goal is to build models that perform well in terms of F1 score, F2 score, and ROC-AUC.

## About This Sprint

This project is part of a capstone for a data science program, where the objective is to iteratively build and implement a plan for a large dataset based on business objectives. The task involves translating business requirements into a machine learning solution, making necessary assumptions along the way.

## Relevant Technical Skills

- Pandas
- Numpy
- Visualization Libraries (Matplotlib, Seaborn, or others)
- Converting Business Requirements to ML-Driven Solutions
- Statistical Analysis (correlations and other relations between variables, and other EDA elements)
- Data Wrangling for Machine Learning (Train-test split, cross-validation)
- Supervised and/or Unsupervised Machine Learning Algorithms (Scikit Learn, gradient boosting libraries)
- Model Selection Analysis
- Model Evaluation (Relevant performance metrics, visualizations)
- Hyperparameter Tuning
- Statistical Inference (confidence intervals, hypothesis tests)
- Proficient Use of Jupyter Notebooks

## Context

You and your friend have come up with a startup idea to provide risk evaluation as a service for retail banks. Your friend handles sales and operations, while you are responsible for product development, including planning, data analysis, and building the solution. You identified machine learning as a crucial component of your offering, as it can capture statistical patterns in bank loan defaults.

To start, you downloaded a [dataset](https://storage.googleapis.com/341-home-credit-default/home-credit-default-risk.zip) from Home Credit Group and discussed with your friend to create a POC product with different models. This ensures a robust and diversified offering for potential clients. You aim to analyze the dataset thoroughly and predict interesting features, allowing your friend to focus on securing meetings with banks.

## Directory Structure

- `main_notebook.ipynb`: Central Jupyter notebook for detailed analysis, feature selection, and modeling.
- `project_datasets_overview.ipynb`: Exploratory Data Analysis (EDA) of the provided datasets.
- `feature_selection.ipynb`: Notebook covering feature selection processes, including techniques like SHAP, BORUTA, and RFECV.

## Key Aspects

- **Focus on applications_train Dataset**: The analysis centers around this dataset.
- **Comprehensive Feature Analysis**: Includes advanced techniques for feature selection.
- **Model Diversity**: Exploration of various models, primarily XGBoost and CatBoost, with hyperparameter tuning.

## Improvements & Future Directions

- **Comprehensive Statistical Testing**: Expand the scope of statistical analysis for deeper understanding of data relationships.
- **Iterative Modeling Approach**: Adopt a more iterative and experimental strategy.
- **Diverse Model Exploration**: Incorporate additional models such as Random Forest, Neural Networks, or Ensemble methods.
- **In-depth Feature Analysis**: Delve deeper into SHAP analysis for better-informed feature engineering.
- **Extensive Hyperparameter Tuning**: Employ advanced techniques for hyperparameter tuning.
- **Advanced Feature Engineering**: Experiment with automated feature engineering tools like AutoFeat.
- **Precision in Handling Missing Values**: Implement sophisticated imputation techniques.
- **Experimenting with Categorical Data**: Leverage CatBoost's ability to naturally process categorical data.
- **Increased Use of Visualizations**: Enhance data storytelling with more visual aids.
- **Leverage Additional Datasets**: Integrate more data related to significant features identified.
- **Unified Dataset Modeling**: Combine all available datasets for a comprehensive analysis.
- **Temporal Analysis**: Conduct temporal analysis to uncover trends over time.
- **Validation on External Datasets**: Test models on external datasets for generalizability.
- **Cost-Sensitive Learning**: Implement cost-sensitive approaches considering the financial cost of misclassifications.
- **Post-Modeling Analysis**: Perform thorough post-modeling analysis including error analysis and scenario testing.

## Notebooks Description

### Primary Analysis Notebook for Client Default Prediction

**main_notebook.ipynb**

This notebook serves as the central piece of analysis, focusing on the applications_train.csv dataset. Key steps from the plan document are followed, with certain tasks delegated to supplementary notebooks for clarity.

**Contents:**

- **Dataset Characteristics**: Initial exploration of the dataset, understanding its structure and characteristics.
- **Target Class Frequencies and Data Types**: Analysis of class distributions and data type categorizations.
- **Correlation and Statistical Analysis**: In-depth examination of feature correlations and statistical significance in relation to the target variable.
- **Feature Selection and Engineering**: Detailed process of handling missing values, addressing high cardinality, and optimizing feature selection.
    - **External Notebooks**: Advanced feature selection techniques like RFECV, BORUTA, and SHAP analysis are covered in separate notebooks.
- **Benchmark Models**: Initial model evaluations using LazyClassifier with and without SMOTE, providing baseline performances.
- **Model Development**: Building and tuning models using XGBoost and CatBoost, including:
    - **SMOTE Application**: Addressing class imbalance.
    - **XGBoost Modeling**: Developing models with custom scorer focusing on F2 score and ROC AUC.
    - **Hyperparameter Tuning**: Extensive tuning using RandomizedSearchCV.
    - **CatBoost Modeling**: Examining different configurations of CatBoost models.
    - **Feature Filtering**: Utilizing SHAP values from both XGBoost and CatBoost to refine the feature set.
    - **SHAP Analysis and Comparison**: Comparative analysis of SHAP values to emphasize differences in feature importance.

### Feature Selection Notebook

**feature_selection.ipynb**

This notebook details the procedures of feature selection using RFECV and BORUTA. The features selected through these methods are utilized in the main analysis notebook for further modeling.

**Contents:**

- **RFECV**: Conducted twice with different evaluation metrics to emphasize recall for class one while maintaining a balanced output.
- **BORUTA**: Recommended retaining 71 features from an initial set of 150, whereas RFECV suggested only 4.
- **Feature Weights**: Potential use of feature weights to increase the importance of features identified by RFECV.
- **Results**: Prominently displayed under distinct headers, with detailed procedures minimized for readability.

### Project Datasets Overview

**project_datasets_overview.ipynb**

This notebook provides a general overview of the included datasets for this project. It includes initial exploration, checking characteristics, and detailed examination of selected features.

**Contents:**

- **Dataset Characteristics**: Overview of dimensions, missing values, counts, and distributions.
- **Selected Features**: Detailed examination based on their value to the analysis.
- **Exploratory Data Analysis (EDA)**: Broad context information about the datasets to inform further analysis.

### License

This project is made available under the MIT License, supporting open-source collaboration and knowledge sharing.
