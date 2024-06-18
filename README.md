# Solar Power Prediction Using Machine Learning

## Overview
This repository contains code and documentation for predicting AC power output from solar plants using various machine learning models. The project aims to optimize energy forecasting through data-driven approaches, leveraging solar panel data and weather sensor observations.

## Problem Statement
The primary objective is to develop robust models capable of accurately predicting AC power generation in two solar power plants based in India. This involves analyzing the impact of parameters such as irradiation, ambient temperature, and module temperature on power output.

## Dataset Description
The dataset was sourced by filling an agreement form Under the guidance of profesor A V Subramanyam
- **Generation Data:** Recorded at 15-minute intervals, including DC power, AC power, daily yield, and total yield.
- **Weather Sensor Data:** Also recorded at 15-minute intervals, comprising ambient temperature, module temperature, and irradiation.

## Methodology
### Data Preprocessing
1. **Data Compilation:** Merging generation and weather sensor datasets based on timestamps.
2. **Feature Engineering:** Calculating derived features such as daily yield accumulation.
3. **Normalization:** Scaling numerical features to ensure uniformity across data distributions.

### Model Development
1. **Exploratory Data Analysis:** Visualizing feature distributions and correlations using scatter plots and heat maps.
2. **Feature Selection:** Employing Lasso Regression to identify significant predictors affecting AC power output.
3. **Model Selection:** Evaluating multiple regression algorithms:
   - **Linear Regression:** Baseline model for initial performance assessment.
   - **Random Forest:** Leveraging ensemble learning for capturing complex interactions.
   - **XGBoost:** Optimizing predictive accuracy through gradient boosting with regularization.
   - **Artificial Neural Networks (ANNs):** Utilizing deep learning for non-linear feature representation.

### Model Evaluation
1. **Performance Metrics:** Using Mean Squared Error (MSE) and R2 score to quantify model accuracy.
2. **Cross-Validation:** Employing k-fold cross-validation to mitigate overfitting and assess generalization capability.
3. **Hyperparameter Tuning:** Optimizing parameters such as learning rate and tree depth for XGBoost and ANN models.

## Results
### Model Performance Comparison
- **Linear Regression:** MSE = 23702.03, R2 = 0.8348
- **Random Forest:** MSE = 1567.58, R2 = 0.9891
- **XGBoost:** MSE = 97.26, R2 = 0.9992
- **ANN (Adam Optimizer):** MSE = 3.59, R2 = 0.99997

### Insights
- **Feature Importance:** DC power and irradiation exhibit strong positive correlations with AC power, highlighting their pivotal role in predictive accuracy.
- **Model Superiority:** XGBoost and ANN with Adam optimizer significantly outperform traditional regression models, showcasing their ability to handle complex, non-linear relationships inherent in solar power generation.

## Conclusion
This project underscores the efficacy of advanced machine learning techniques in enhancing solar power forecasting accuracy. By leveraging comprehensive data analysis, feature engineering, and sophisticated modeling, we achieve near-optimal predictions crucial for efficient solar energy management and planning.

## Future Work
1. **Ensemble Methods:** Exploring ensemble techniques like stacking to further enhance predictive performance.
2. **Real-time Integration:** Developing frameworks for real-time prediction using streaming data from sensors.
3. **Extended Features:** Incorporating additional environmental factors (e.g., wind speed) for comprehensive energy forecasting.

## References
1. Subramanian, E., et al. "Solar Power Prediction Using Machine Learning." arXiv preprint arXiv:2303.07875 (2022).
2. Chakraborty, D., et al. "Computational solar energy – Ensemble learning methods for prediction of solar power generation." Renewable Energy Focus 44 (2023): 277-294.
3. Phan, Q.-T., et al. "Short-term Solar Power Forecasting Using XGBoost with Numerical Weather Prediction." IEEE International Future Energy Electronics Conference (IFEEC) 2021.
4. Barrera, J. M. "Solar Energy Prediction Model Based on Artificial Neural Networks and Open Data." Sustainability 12.17 (2020): 6915.
5. McGovern, A., et al. "Solar Energy Prediction: An International Contest to Initiate Interdisciplinary Research on Compelling Meteorological Problems." Bulletin of the American Meteorological Society 96.8 (2015): 1388-1395.
