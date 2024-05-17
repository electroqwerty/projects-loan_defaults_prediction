# Loan Default Prediction - Capstone Project (Second Submission)

## Project Overview

This repository hosts the revised version of a machine learning project focused on predicting loan defaults. It's part of a POC for a startup targeting retail banking risk assessment. The work primarily uses the `applications_train.csv` dataset, with emphasis on selecting key features, developing predictive models, and thorough data analysis. The main goal is to build models that perform well in terms of F1 score, F2 score, and ROC-AUC. This update brings improvements in methods and new findings compared to the initial submission.

## Directory Structure

- `new_Main Analysis.ipynb`: Central Jupyter notebook for detailed analysis, feature selection, and modeling.
- `new_included_datasets_overview.ipynb`: EDA Overview of datasets provided.
- `new_feature_selection_notebook.ipynb`, `new_xgboost models and hyperparameter tuning .ipynb`: Notebooks covering feature selection and model tuning processes. Note: hyperparameter tuning did not yield good results, notebook is there for reference, not to be conisdered as key part of the analysis. I wanted to showcase that this was done but with small benefits. Additionally, I suggest loading the feature selection notebook with jupyter lab, as the outputs of operations are long. In jupyter lab there is possibility of easily collapsing header space bellow. I suggest this to go through notebook more easily. The 'Results' parts are separate headers that you can easily navigate to. 
- `new_Plan MD.md`: Required document outlining the plan and approach for the analysis.
- `new_all old catboost from failed attempt.ipynb`: A notebook from the initial submission for reference.
- `local_deployment.zip`: Contains the local deployment setup for a web-facing POC part of the project.

## Key Aspects

- **Focus on `applications_train` Dataset**: The analysis is centered around this dataset.
- **Comprehensive Feature Analysis**: Includes techniques like SHAP, BORUTA, and RFECV (detailed in separate notebooks).
- **Model Diversity**: Exploration of various models, primarily XGBoost and CatBoost, with  hyperparameter tuning.
- **Cloud Deployment Challenges**: Although the initial plan included Google Cloud deployment, due to challenges, `this requirement was not fulfilled.`

----

- Currently, I'm still working on the deployment aspect of this project. There's a chance I might have a functioning deployment ready for review by the time of our project correction. If this happens, I'll reach out on Discord to discuss including it in the presentation. I've decided to submit the core part of the project now to keep things moving forward since my initial attempt wasn't successful. As a placeholder for the intended Cloud deployment, I'm including the local deployment setup from my previous submission. This should give you an idea of the user interface I had in mind. You can find everything needed for this in `local_deployment.zip`. Just extract the contents and follow the instructions to get it running.

### Running the Project Locally

- **Environment**: Activate the `(base)` conda environment.
- **Server Start**: In the main directory, run: `uvicorn app:app --reload` to start the FastAPI server.
- **Access Interface**: Visit `http://127.0.0.1:8000/static/index.html` in a browser to use the model.

### Web Interface Features

- **User-Friendly**: Easy input of feature values.
- **Random Data Generation**: Option to create random data for predictions.

## Improvements & Future Directions

1. **Comprehensive Statistical Testing**: Expand the scope of statistical analysis to include more robust tests, enabling a deeper understanding of the underlying data relationships and distributions.
    
2. **Iterative Modeling Approach**: Adopt a more iterative and experimental modeling strategy.
    
3. **Diverse Model Exploration**: While XGBoost and CatBoost have shown promising results, incorporating additional models (such as Random Forest, Neural Networks, or Ensemble methods) could provide valuable  insights and potentially uncover different aspects of the data.
    
4. **In-depth Feature Analysis**: Delve deeper into SHAP analysis to gain more nuanced insights into feature interactions and importance, leading to better-informed feature engineering and selection.
    
5. **Extensive Hyperparameter Tuning**: Employ a more exhaustive approach to hyperparameter tuning, possibly using advanced techniques.
    
6. **Advanced Feature Engineering**: Experiment with automated feature engineering tools like AutoFeat, which might uncover hidden relationships and enhance model accuracy.
    
7. **Precision in Handling Missing Values**: Investigate and implement more sophisticated methods for dealing with missing data, such as imputation techniques tailored to the specific characteristics of each feature.
    
8. **Experimenting with Categorical Data**: Test how CatBoost handles categorical features without explicit label encoding, leveraging its ability to naturally process categorical data.
    
9. **Increased Use of Visualizations**: Incorporate more visual aids to enhance data storytelling and provide clearer insights into the analysis process and results.
    
10. **Leverage Additional Datasets**: Investigate and integrate more data, especially from datasets related to the most significant features identified. This could be a second phase of the project, focusing on enriching the analysis with more diverse data sources.

11. **Unified Dataset Modeling**: Consider the challenge of combining all available datasets into one comprehensive dataset for analysis. This approach can provide a more holistic view, although it may introduce complexities in data preprocessing and feature alignment.
    
12. **Temporal Analysis**: If the datasets include time-based data, conducting a temporal analysis could uncover trends and patterns over time, which might be crucial for predicting defaults.
    

13. **Validation on External Datasets**: To test the generalizability of the models, consider validating them on external datasets that are similar in nature but not part of the original training set.
    
14. **Cost-Sensitive Learning**: Implement cost-sensitive learning approaches, especially if the financial cost of different types of misclassifications (false positives vs. false negatives) varies significantly.
    
15. **Post-Modeling Analysis**: After model development, perform a thorough post-modeling analysis, including error analysis and scenario testing, to understand where and why the model might fail.
