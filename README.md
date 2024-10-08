# Water Pump Functionality Prediction

## Overview
This project aims to develop a predictive model for identifying the functionality status of water pumps in Tanzania. Using data from Taarifa and the Tanzanian Ministry of Water, the model classifies water pumps into three categories: functional, needing repair, and non-functional. This solution assists the Tanzanian government in prioritizing maintenance efforts, optimizing resource allocation, and ensuring reliable access to clean water for communities across the country.

## Business and Data Understanding

### Stakeholder Audience
Our primary stakeholder is the government of Tanzania, responsible for managing and maintaining water infrastructure nationwide. The goal is to enhance the efficiency and effectiveness of maintenance operations, ensuring consistent access to reliable and clean water for all communities.

### Dataset Choice
The dataset includes a comprehensive range of features related to water pump functionality, such as extraction type, management type, water quality, and quantity. This data, sourced from Taarifa and the Ministry of Water, provides insights into pump conditions and usage patterns essential for accurate predictions.

## Modeling

### Feature Selection and Engineering
Extensive feature engineering was performed to identify and create relevant variables impacting water pump functionality. We tested various subsets of features to ensure the model effectively captured all critical information.

### Model Development and Tuning
- **Initial Model**: We began with a baseline model and iteratively refined it to improve performance.We used both Logistic Regression and Decision Trees and compared performance
- **Hyperparameter Tuning**: We fine-tuned the Decision Tree Classifier with a focus on:
  - **Weights**: Adjusting class weights to handle dataset imbalance and ensure balanced performance across all classes.
  - **Max Depth**: Setting the maximum depth to prevent overfitting while capturing necessary data patterns.
  - **Criterion**: Evaluating different criteria (Gini and entropy) for optimal node splitting.

### Model Selection and Evaluation
- **Classification Models**: We evaluated various classification algorithms, including Decision Trees and Logistic Regression. The Decision Tree Classifier was selected based on superior performance metrics.
- **Metrics Comparison**: We compared metrics such as accuracy, recall, precision, and F1-score for different models and datasets (both with and without certain features) to determine the most effective model.

### Handling Class Imbalance
Techniques such as SMOTE were used to address class imbalances, ensuring robust performance across all categories, particularly for minority classes.

## Evaluation
The model was evaluated using key performance metrics, including accuracy, recall, precision, and F1-score. The Decision Tree Classifier demonstrated high performance across all metrics, validating its effectiveness in predicting pump functionality.

## Predictive Recommendations

Based on our analysis, here are key recommendations for improving water pump functionality:

1. **Investigate Zanzibar South (Region Code 11):**  
   Address region-specific challenges affecting pump performance for better maintenance.

2. **Strengthen Bariadi's Local Government Authority:**  
   Support Bariadi’s LGA with enhanced training, resources, and funding to improve pump management and maintenance.

3. **Tailor Maintenance by GPS Height:**  
   Customize maintenance schedules based on pump elevation to address altitude-related issues.

4. **Focus on Older Pumps:**  
   Implement proactive maintenance strategies for older pumps to extend their lifespan and prevent failures.

5. **Improve Seasonal and Insufficient Water Supply:**  
   Enhance maintenance practices for pumps with seasonal or insufficient water supply to ensure consistent availability.

6. **Train Communities for Handpump Maintenance:**  
   Provide training for communities to effectively maintain handpumps, reducing failure rates.

7. **Promote Regular Payment for Water Services:**  
   Encourage consistent payment for water services to ensure sustainable maintenance funding.

8. **Allocate Resources Based on Population:**  
   Prioritize maintenance resources in high-population areas to manage increased wear and tear.

These recommendations aim to enhance pump functionality, optimize resource allocation, and ensure reliable water access across Tanzania.


### Contexts for Model Predictions
- **Useful Contexts**: The model is highly beneficial in scenarios requiring prompt maintenance decisions, such as in remote or rural areas with limited repair services.
- **Less Effective Contexts**: It may be less effective in rapidly changing conditions or where historical data does not accurately reflect current situations.

### Suggestions for Improving Accuracy
- **Data Accuracy**: Ensure up-to-date and accurate data on pump conditions and maintenance histories. Some columns, like `amount_tsh`, were dropped due to high missing values.
- **Feature Engineering**: Introduce additional features related to pump usage patterns, maintenance history, and environmental conditions to enhance model performance.

## Conclusion
The Decision Tree Classifier, finely tuned through an iterative process, provides a reliable solution for classifying water pumps into functional, repair-needed, and non-functional categories. This model supports the Tanzanian government in improving maintenance efficiency and resource allocation, ensuring consistent water availability across the country. Its interpretability and robust performance make it a valuable tool for decision-making and future infrastructure management.

The project has successfully developed a high-performing predictive model that addresses a critical infrastructure challenge, delivering tangible benefits for the Tanzanian government and its citizens. The systematic approach to model development, hyperparameter tuning, and evaluation has ensured that the chosen model meets the stakeholder's needs.

## Links
- [Presentation Slides](https://github.com/leonardkoyio/Phase-3-Project-_v1/blob/main/Deliverables/Predictive%20Maintenance%20of%20Water%20Pumps%20in%20Tanzania-Presentation.pdf)
- [Jupyter Notebook](https://github.com/leonardkoyio/Phase-3-Project-_v1/blob/main/Deliverables/Predictive%20Maintenance%20of%20Water%20Pumps%20in%20Tanzania-%20Notebook.pdf)
- [Sources](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/data/)


## Repository Structure and Navigation

This repository contains the following folders and files:

- **`data/`**: Contains the dataset files used for training and testing the model.
  - `train_data.csv`: The CSV file with training data.
  - `test_data.csv`: The CSV file with testing data.

- **`Deliverables/`**: Includes key project deliverables.
  - `Predictive Maintenance of Water Pumps in Tanzania- Notebook.pdf`: The final Jupyter Notebook with detailed analysis and results.
  - `Predictive Maintenance of Water Pumps in Tanzania-Presentation.pdf`: The PDF version of the project presentation.
  - `Predictive Maintenance of Water Pumps in Tanzania-Presentation.pptx`: The pptx version of the project presentation.

- **`figures/`**: Contains visualizations generated during the analysis.
  - Various PNG files of charts and graphs used for documentation.
  - `Confusion Matrix.png`: confusion matrix final model
  - `ROC_Curve.png`: ROC Curve final model
  - `Top features.png`: Top features final model


- **`index.ipynb`**: The main Jupyter Notebook that contains the project’s code, methodology, and analysis.

- **`README.md`**: This file, providing an overview of the project, data, modeling, evaluation, and instructions for navigating the repository.

### Instructions for Use

1. **Data**: Access the dataset files in the `data/` folder for training and testing your model. Ensure you use the appropriate file for your specific needs.

2. **Notebook**: Open `index.ipynb` in Jupyter Notebook or JupyterLab to view the project's code and analysis. This notebook includes all steps of the data science process.

3. **Deliverables**: Review `Predictive Maintenance of Water Pumps in Tanzania- Notebook.pdf` for a comprehensive report of the analysis and `Predictive Maintenance of Water Pumps in Tanzania-Presentation.pdf` for the summarized presentation slides.

4. **Figures**: Check the `figures/` folder for saved visualizations used in the project documentation.

Feel free to explore the files and folders to understand the project's components and how they interconnect.


