# Portuguese Banking Institution
![Barroso son gets job with Bank of Portugal ‘without competition ...](https://www.euractiv.com/wp-content/uploads/sites/2/2014/08/banco_de_portugal.jpeg)
## Objectives
- To perform neccessary exploratory data analysis to know some interesting fact about portuguese banking institition's marketing campaign. 
- How well did the campaign perform to sell the new product,"term deposits"?
- Create a model using the decision tree classifier and create a decision tree out of it.
- Create a function that predicts whether customer subscribes the term deposit using the user input. 
##  About the dataset
 The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed.
1.  age (numeric)
2.  job : type of job (categorical:admin.','bluecollar','entrepreneur','housemaid','management','retired','selfemployed','services','student','technician','unemployed','unknown')
3.  marital : marital status (categorical:'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
4.  education (categorical:"high.school','illiterate','professional.course','university.degree','unknown')
5.  default: has credit in default? (categorical: 'no','yes','unknown')
6.  balance: average yearly balance, in euros (numeric)
7.  housing: has housing loan? (categorical: 'no','yes','unknown')
8.  loan: has personal loan? (categorical: 'no','yes','unknown')
9.  contact: contact communication type (categorical:'cellular','telephone')
10.  day: last contact day of the month (numeric 1 -31)
11.  month: last contact month of year (categorical: 'jan', 'feb','mar', …, 'nov', 'dec')
12.  duration: last contact duration, in seconds (numeric).  
    Important note: this attribute highly affects the output target (e.g., ifduration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known.Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic  
    predictive model.
13.  campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
14.  pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
15.  previous: number of contacts performed before this campaign and for this client (numeric)
16.  poutcome: outcome of the previous marketing campaign(categorical: 'failure','nonexistent','success')
17.  target: has the client subscribed a term deposit? (binary:"yes","no")


#  Insights
-  Overall, out of more than 45000 existing customers the company has received around 12% customer subscribing the product the new product. Remaining 88.3% feels not to buy them. It is not a very good figure to present out of a huge existing client base. There must be neccessary steps taken to improve the figure.

- People who have subscribed the term deposits tend to be higher in late thirties. Although there is no much difference but one can easily tell that this effect could be the preference they have on investments like equity market or mutual funds. Usually, in reality they do not prefer deposits due to less returns.

- Probably, the next campaign also must be done through only cellular to reduce the time consumed in telephone and other source. Company can also bring in digital ads as it is becoming famous nowaday, that can cover exisiting as well as the new customers too.

- The customers who spend more duration on call has accepted our new product. This is the same in the case for the rest of the contact types too. Trying to engage the clients for long talk might improve the acquisition rate.

- Most of people who was successful in last marketing campaign have been successful in the current marketing campaign of term deposits. This shows that previous new product could have worked good for them but still the maketing campaign is not effective. The effective part is just minimal but the ineffective part is high for both previous as well as current marketing campaign.
- The new marketing campaign was not very successful to bring the previous failures. This shows that the marketing campaign no such improvement to acquire a lot of customers. If this trend continues, at one point of time we can loose the current succesful for our upcoming new products too.
- As per the job status we can find that clients with jobs that are blue-collar, enterpreneur and services have given more duration for the current marketing campaign. Probably we must start focusing on other job types too. We have a great potential on self-employed and management roles, so that we can target them more on our upcoming products too.


##  Modelling
Using this dataset, decision tree classifier model was performed. Initially before performing the modelling, null values were dropped. Another dataframe was made that only contains the categorical columns, so that label encoder can be applied. The dataframe was joined with the one that had all the numerical values. The data was finally splitted to create the testing and training data. From  sklearn model selection the decision tree classifier was performed and then it was fited to the training data. Predictions of both training and testing data was carried out. Minimum samples of 10000 was taken to fit in the decision tree regressor. From sklearn the tree was imported, and plotted the decision tree classifer. Finally a function was created for any user who wish to predict whether the client will subscribe the term deposits.
## Evaluation performed
- Confusion matrix
- Precision score
- ROC curve
- AOC curve

![Countdown begins on choice for new governor of Bank of Portugal ...](https://www.portugalresident.com/wp-content/uploads/2020/02/banco-de-portugal-1.jpg)

