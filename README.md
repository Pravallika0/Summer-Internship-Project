# Summer-Internship-Project
# Machine Learning in Prediction of Intrinsic Aqueous Solubility of Drug-like Compounds

This repository contains the implementation of machine learning algorithms to predict the intrinsic aqueous solubility of drug-like compounds, based on the research by Mario Lovric, Kristina Pavlovic, Petar Žuvela, Adrian Spataru, Bono Lucˇic, Roman Kern, and Ming Wah Wong. The focus is on reproducing the results of the original paper and understanding the methodologies used.

## Abstract

The project aims to use machine learning algorithms to predict the intrinsic aqueous solubility of 829 drug-like compounds based on their chemical structures. The study compares four different machine learning algorithms and finds that the LASSO and random forests (RF) performed the best. A consensus model combining the two best learners showed the highest predictive ability and generalization. The results of this study can be useful in drug discovery and development by helping researchers prioritize compounds with better solubility early in the process.

## Introduction

Predicting the intrinsic aqueous solubility of drug-like compounds is crucial in the early stages of drug discovery and development. Poor solubility can lead to low bioavailability and other pharmacokinetic issues. This study uses a dataset of intrinsic aqueous solubility values for drug-like compounds to train and test machine learning models.

## Data Collection and Preprocessing

Data was collected from various sources with pH measurements between 22.5 and 25 degrees Celsius and used inert gases in measurements. The dataset was preprocessed by calculating and considering fingerprints (FPs) and molecular descriptors (DPs). The preprocessing steps included:

1. Removing features with missing values
2. Removing correlated features (Pearson correlation > 0.85)
3. Converting categorical features to binary features
4. Removing low variance binary features

## Machine Learning Methods

The following machine learning methods were evaluated:

1. Partial Least Squares (PLS)
2. Random Forest (RF)
3. Light Gradient Boosting Machine (LGBM)
4. Least Absolute Shrinkage and Selection Operator (LASSO)

The models were trained and tested on a dataset of 829 compounds. Performance was evaluated using metrics such as root mean squared error (RMSE) and coefficient of determination (R^2).

## Feature Selection and Hyperparameter Optimization

Feature selection was done using permutation importance, and hyperparameter optimization was performed using Bayesian optimization. These steps helped improve the performance of the machine learning algorithms.

## Model Training and Evaluation

Models were trained on an 80% training set and validated on a 20% validation set. A ranking schema was used to evaluate the performance of the machine learning models, considering test performance, complexity, and generalization.

## Results and Conclusion

- LASSO showed the best predictive ability on an external test set.
- RF achieved a good balance between complexity and predictive ability with a smaller number of features.
- A consensus model combining LASSO and RF outperformed all other models with an RMSE of 0.67 log points and an R^2 of 0.81.

The study concludes that LASSO and RF are effective for predicting the intrinsic aqueous solubility of drug-like compounds, with the consensus model providing the best results.

## Performance Metrics

The performance of the models was assessed using the following metrics:

- RMSE
- R^2
- Generalization ability

### LASSO Results
- Train RMSE: 0.6625
- Validation RMSE: 0.9580
- Test RMSE: 0.6964

### RF Results
- Train RMSE: 0.4726
- Validation RMSE: 0.9390
- Test RMSE: 0.7212

## Conclusion

The project successfully reproduced the results of the original paper and provided insights into the predictive ability of different machine learning algorithms for solubility prediction. LASSO showed the best predictive ability, while RF provided a good balance between complexity and predictive ability.

## Acknowledgments

This work was done as part of an internship project. Special thanks to the authors of the original paper for their research and methodologies.

## Contact

For any queries, please reach out via LinkedIn: [[Pravallika Oggu]](https://www.linkedin.com/in/pravallika-oggu-303360225/)

---

This README provides a comprehensive overview of the project and its findings. For detailed code and implementation, please refer to the Jupyter notebooks provided in the repository.
