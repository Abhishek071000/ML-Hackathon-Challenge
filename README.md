# ML-Hackathon-Challenge
Predicting whether client subscribed a term deposit
Table of Contents:
Data Set
Result
Data Set
The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed.

Input variables:

Bank client data:
age (numeric)
job : type of job (categorical: 'admin','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
education (categorical: 'high school', 'professional course','university degree','unknown')
default: has credit in default? (categorical : 'no','yes','unknown')
housing: has housing loan? (categorical: 'no','yes','unknown')
loan: has personal loan? (categorical: 'no','yes','unknown')
Related with the last contact of the current campaign:
contact: contact communication type (categorical: 'cellular','telephone')
month: last contact month of year (categorical: 'jan','feb','mar',.. , 'nov','dec')
day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.
Other attributes:
campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
previous: number of contacts performed before this campaign and for this client (numeric)
poutcome: outcome of the previous marketing campaign (categorical: 'failure', 'nonexistent', 'success')
Target variable:
y - has the client subscribed a term deposit? (binary: 'yes','no')

Results
       Model	              Accuracy	     Precision    	Recall	    F1 Score    	Mean    	  Std Deviation
Logistic Regression       	0.796576	     0.830189	     0.726672	    0.774989	    0.788186	     0.017302
K-Nearest Neighbors	        0.742834	     0.782783      0.645747	    0.707692	    0.742275	     0.013596
2	SVM (RBF)	                0.797771	     0.804857	     0.766309	    0.785110	    0.798941	     0.009331
3	Naive Bayes (Gaussian)	  0.692277	     0.728601	     0.576383	    0.643615	    0.691072	     0.020041
4	Decision Tree	            0.765924	     0.770165	     0.733278	     0.751269	    0.769922	    0.018911
