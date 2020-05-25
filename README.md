# Starbucks Capstone Challenge:

> ### Overview :

Customer satisfaction drives business success and data analytics provide useful insight into what customers think about their product or services. The Starbucks Udacity Data Scientist Nanodegree Capstone data set is a simulation of customer behavior on the Starbucks rewards mobile application. Starbucks sends out an offer to users that may be an advertisement, discount, or buy one get one free (BOGO). An important characteristic regarding this dataset is that not all users receive the same offer.

This data set consists of three files. The first file describes the characteristics of each offer, including its duration and the amount a customer needs to spend to complete it. The second file contains customer demographic data including their age, gender, income, and when they created an account on the Starbucks rewards mobile application. The third file describes customer purchases and when they received, viewed, and completed an offer. An offer is only successful when a customer both views an offer and meets or exceeds its difficulty within the offer's duration

> ### Problem Statement / Metrics

The problem that I chose to solve are to:

 1- What are the main drivers of an effective offer on the Starbucks app?
 
 2- Build a model to predict that whether a user would take up an offer?

Using the data provided, I answer the above two questions using 3 classification supervised machine learning models.I use the model to uncover the feature importances to identify the drivers of offer effectiveness, while exploring if the model itself could be used to predict if a user would take up an offer.I also explore the characteristics of users who do or do not take up an offer.

I will assess the accuracy and F1-score of a naive model that assumes all offers were successful ,My first assessing whether an all-in-one model could be used in place of 3 different models, with the offer types functioning as a categorical variable. Secondly, I also build a regression model to see if we could predict the amount a user would spend, given that the offer is effectively influencing them. I will refine the parameters of the model that has the highest accuracy and F1-score.

> ### Libraries :
	
* pandas
	
* numpy
	
* matplotlib

* re
	
* nltk
	
* sklearn

> ### Data :

* portfolio.json: containing offer ids and meta data about each offer.

* profile.json: demographic data for each customer 

* transcript.json: records for transactions, offers received, offers viewed, and offers completed

> ### Files :

* Starbucks_Capstone_notebook.ipynb : contains all the code with its output.
  
> ### Results Summary :

**Question 1 findings:**

The feature importance given by all three models were that the tenure of a member is the biggest predictor of the effectiveness of an offer. Further study would be able to indicate what average tenure days would result in an effective BOGO offer.

For all three models, the top three variables were the same-membership tenure, income and age. However, income and age switched orders depending on offer type.

For BOGO and discount offers, the distribution of feature importances were relatively equal. However, for informational offers, the distribution is slightly more balanced, with income the second most important variable.

**Question 2 findings:**

My decision to use three separate models to predict the effectiveness of each offer type ended up with good accuracy for the BOGO and discount models (82.83% for BOGO and 87.35% for discount), while slightly less accurate performance for informational offers (75.3%). However, I would regard 75% as acceptable in a business setting, as for informational offers, there is no cost involved to inform users of a product.

Meanwhile, for BOGO and discount models, I am quite happy with the 80% and above accuracy, as in a business setting that would be acceptable to show offers to people, even if the model misclassifies a few, the overall revenue increase might justify the few mistakes.

> ### Acknowledgement:

* Udacity for great course materials

* Starbuck for the dataset


#### For more information visit my Starbucks Capstone Challenge [post](https://medium.com/@samplecsn16/sentiment-analysis-of-twitter-data-in-python-2f41ba2b3ea5).  
