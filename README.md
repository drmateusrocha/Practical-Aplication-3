### Practical Application 3: Comparing Classifiers

**Mateus Rocha**

#### Executive summary
This is a practical exercise to complete the requirements for the Certificate in AI/ML at UC Berkeley. The goals is to compare the performance of different model classifiers (K Nearest Neighbor, Logistic Regression, Decision Trees and Support Vector Machines. The data set used is a dataset from the UCI Machine learning repository. The data is from a institution to determine if the client is likely to subscribe to a term deposit

#### Rationale
The understanding of the best model to predict the churn of the marketing campaign can help the optimization of the marketing workflow of the company. This can help targeting the right client that is more likely to accept the subscription a turn deposit

#### Research Question
Which model from K Nearest Neighbor, Logistic Regression, Decision Tree, or Support Vector Machine is the most accurate in the test data set, using their default parameters?

After optimization of the two best models in their default parameters, which one have better performance?

What are the most important features in the determination if the client has subscribed to a term deposit?

#### Data Sources
The data source can be found in this GitHub depository or at https://archive.ics.uci.edu/ml/datasets/bank+marketing

#### Methodology
I am using the Jupyter Notebooks with scikit-learn libraries. The method was to first check the data for missing values. We use the one-hot encoder to treat the data. Then we used only the following bank information:
	
	# bank client data:
	 - 1 - age (numeric)
	 - 2 - job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
	 - 3 - marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
	 - 4 - education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
	 - 5 - default: has credit in default? (categorical: 'no','yes','unknown')
	 - 6 - housing: has housing loan? (categorical: 'no','yes','unknown')
	 - 7 - loan: has personal loan? (categorical: 'no','yes','unknown')
After this I tested the default method of common classifiers; I selected the two best; and I optimize their parameters


#### Results
The results show that by default the logistic regression and the SVM model has the highest accuracy in the test data (0.8865); Both of them have the lowest accuracy in the training data, but still a high accuracy (0.8876). However, the train time for the logistic regression is only 0.3145 while the SVM is 13.37. Thus, by default, the logistic regression is the best model.

According to the logistic regression the highest coefficient to determine the model are: if the job is student and if the default_unknown.

Nevertheless, when the models are optimize, the results are completely different.
The Decision Tree when optimized (max_depth=3, min_samples_leaf=20, random_state=42) shows a highest train and test accuracy (0.8880 and 0.8872) , respectively.

Also the feature importance shows that the most important features to determine if the client will subscribe are
	> age = 0.60
	> job_student = 0.20
	> default_no = 0.19
	> education_basic.9y = 0.01

The decision tree model can be found in the link

#### Outline of project

- [Link to notebook 1]()
- [Link to notebook 2]()
- [Link to notebook 3]()


##### Contact and Further Information
mrocha@dental.ufl.edu