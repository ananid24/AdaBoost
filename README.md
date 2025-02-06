# AdaBoost

The methodology for this project was inspired by two key papers: *"Cost-sensitive Boosting for Classification of Imbalanced Data"* by Yanmin Sun and Mohamed S. Kamel, and *"One-Benefit Learning: Cost-sensitive Learning with Restricted Cost Information"* by Bianca Zadrozny. Both works provide valuable theoretical and practical approaches for managing missing data and class imbalances.

The project's objective was to develop a model that predicts the binary target variable, **Y_target**, which necessitated the use of a classification framework. Prior to model development, it was essential to address the data imbalance issue. This was achieved using two complementary approaches:

1. **Data-Level Approach:**  
   - **Random Oversampling:** The minority class was first subdivided into sub-concepts using K-means clustering. Each sub-cluster was then oversampled so that its size matched that of the largest cluster. Finally, the oversampled minority data was combined with the majority class data to form a balanced training set.

2. **Algorithmic-Level Approach:**  
   - **Cost-Sensitive Learning:** A cost matrix was developed to incorporate misclassification costs, enabling the model to prioritize the extraction of rare, yet regular, patterns. This approach helped to minimize the overall cost of misclassification.

The implementation of these strategies was carried out using AdaBoost, which naturally integrates cost-sensitive learning with variance and bias reduction, thereby focusing on minimizing misclassifications.

The remainder of the code is self-explanatory. Please note that the dataframes `df_1` and `df_2` are reserved for further analysis and can be disregarded in this context.
