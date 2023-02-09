# startup-success
This project explores the effects that various attributes have on whether or not a startup is successful. The dataset used was obtained from the following source:

KC, M. (2020, September 16). Startup Success Prediction. Kaggle. Retrieved February 7, 2023, from https://www.kaggle.com/datasets/manishkc06/startup-success-prediction 

Beyond the ingenuity of an initial idea or the hours spent on getting a startup off the ground, there are many external and environmental factors that undoubtedly sway the future of each startup. The aforementioned dataset includes attributes such as location, type of industry, and rounds of funding that will be used to create supervised learning models. These models will then be used to form binary classification predictions as to the success of a startup based on the given attributes. This type of classification would be useful in determining factors like location in building a startup, as well as in informing investors of what makes a startup more likely to be successful than others. 

The dataset was chosen because it provides many attributes that may be known during the early stages of a startup, as well as including some later-stage indicators of success. More information on the dataset is explored in the EDA notebook. 


Review, discussion, and conclusions drawn from the model:

Cleaning of the dataset followed by exploration of the dataset, including visualization and analysis of some of the key features, was performed in the EDA notebook. This was followed by training logistic regression and decision tree models, with the goals of both maximizing predictive power as well as obtaining interpretable results. 

The models were judged on their accuracy, F1 score, and ROC AUC. All models used k-fold cross validation to obtain more accurate measures of lower variance. Details of the results are discussed in more depth within the notebooks, but the best model was found to be a random forest classifier with hyperparameters determined via a grid search. The scoring metrics are as follows:
	Test accuracy: 0.792
	Test F1 score: 0.854
	Test ROC AUC: 0.823
	
As far as key attributes, fitted coefficients are listed in the logistic notebooks. Some interesting observations include years just post 2000 being excellent predictors for success, whereas years just prior to 2000 tend to be associated with failure. Additionally, Massachusetts tends to coincide with startup success, whereas Texas does especially poorly in this regard. The entire list of attribute coefficients are available in the relevant notebooks. 

One surprising takeaway was that the optimized hyperparameters obtained from the grid search did not significantly alter the performance of the random forest model; the native model performed rather similarly. As tweaking the hyperparameters often leads to better performance, it is possible that the lack of improvement was due in part to the optimal variables being near the native ones by chance. Additionally, the decision tree format would be an excellent means of conveying information about these startups. Unfortunately, due to the poor interpretability of random forests, this was not possible. A more interpretable implementation of a decision tree trained on this dataset may be a useful future step. 

