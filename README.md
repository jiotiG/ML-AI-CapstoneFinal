<span style="color: green; ">

# ML-AI-CapstoneFinal
Final capstone project deliverables for ML AI Program at Berkeley Engineering

**Overview**: For my research question I have chosen to find out given a dataset if there is a pattern for DDoS (Distributed Denial of Service) Attack on the application or a given IP address.  
The type of machine learning algorithm used for this module would be supervised learning, where algorithms explore data to find patterns with a defined output variable.
</br>
The classification goal is to identify a model to best predict if the client will subscribe a term deposit.
Utilizing modeling and performing a comparison using Logistic Regression, K-Nearest Neighbors, Decision Tree and SVM models to understand which model is the best suited to provide the most accurate data such that the banks could successfully subscribe more customers with a fewer number of calls.


### Data Understanding
After the data exploration, data preparation to cleanse or delete the data was performed so that the model could be performant.
A very few number of duplicate or null rows existed in the data which were deleted.

### Data Preparation
The data was very mostly clean, some columns were renamed for consistency.
Utilizing the basic histogram the data representation was performed, and it was evidently clear that in large part the data is not normalized, and would need scaling for the models to perform well.


### Modeling
For Modeling purposes, data was encoded for the categorical columns and the numerical columns were scaled with StandardScalar.
The train split was 2/3 of the entire dataset and test split was 1/3 of the dataset.

Starting with a simple Logistic Regression, the outcome was already better than expected 88.85% with all the features. However, it was important to fine tune the hyperparmeters and find out if the other models can perform better.

Then the other models were built and compared.
1. KNN
2. Decision Tree
3. SVM

The basic models had lower accuracy scores, and high precision scores, Logistic Regression and SVM continued to provide good AUC however more fine-tuning was required to find better accuracy scores.


### Evaluation

In order to find the best hyperparmeters GridsearchCV was utilized and the outcomes were exemplary and mostly all models came out performing really well.  
One issue I ran into was Gridsearch hyperparameter tuning for the SVM model was not able to finish even after running 8-9 hours.

After hyperparameter tuning the Decision Tree model came with an accuracy of 100% and KNN with 99% accuracy, which largely points to the fact that these models maybe over-fitting and may need some re-evaluation.

### Neural Network Model
After the evaluation of classifier models, a simple Neural Network model was trained and evaluated with the MSE score.
The MSE score for the Sequential model came around 0.012 which seems low and signifies the model can predict really well with low score.

### Next steps and Recommendations:

The next steps are to evaluate the models by deploying and monitoring the actual usage of it. 
This would be required, so that the CRISP-DM framework could be utilized and the iterations over the model could be performed to find a best fine-tuned Machine Learning Model for this problem.