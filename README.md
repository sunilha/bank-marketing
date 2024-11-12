# Bank-Marketing
### Project Overview
This dataset comes from the UCI Machine Learning repository [link](https://archive.ics.uci.edu/ml/datasets/bank+marketing). The data is from a Portuguese 
banking institution and is a collection of the results of 17 phone marketing campaigns between May 2008 and November 2010. During these
phone campaigns, an attractive long-term deposit application, with good interest rates, was offered.

### Data Understanding
This dataset contains of demographics of individuals who are enrolled with the bank, 
their social/financial details and campaign information.

``` 
Demographics : age, job, marital status, education etc.
Financial : Has housing/personal loans, Employment etc.
Campaign : Number of time customer was contacted, outcome of previous campaigns etc.
```

### Business Objective
This dataset resulted in 8% success rate. Objective here is to identify the attributes of bank customers who are likely to subscribe for long term deposit.
This will be help banks to get better in customer engagement, reach out to customers who are likely to subscribe thus increase campaign success rate. 


### Findings Summary
Analysis was made can be classified into 2 halves. One inclusive all the features and modelling with default settings and 
another with limited features modelled with optimized settings

1) All feature inclusive \
    Duration i.e. last phone conversation with customer, is the most influential feature. Modelled the data with Logistic Regression, k-nearest neighbors(KNN), Decision Tree and Support Vector Machine(SVN) models.

 - Models were used with default settings
 - Train and Test accuracy for Logistic Regression and SVM are comparable, however SVM takes more time for training
 - There is decent difference between Train and Test accuracy for KNN and Decision Tree, both have comparable training time

2) Limited features included \
    Along with duration, Social and Economic context features are removed ``` "duration","emp.var.rate","cons.price.idx","cons.conf.idx","euribor3m", "nr.employed" ```.
 - pdays i.e. number of days that passed by after the customer was last contacted from a previous campaign,  is the most influential feature, followed by Customer's age, martial status, education.
 - Models were optimized - hyperparameter tuning and gridsearch
 - All models had marginal drop in both train and test accuracy
 - Train and Test accuracy are comparable for all the models
 - Model training got better for all but SVM, SVM training time took a longer in this case

Customer with good finance, previously enrolled in campaign (repeat customer) are expected to enroll for this long term deposit campaign. 
With help of this analysis bank can come up with better customer engagement programs, focus their resources towards 
limited number of customers which will likely result in higher success rate. 
Using similar analysis bank can come with tailored products for its customers.

Jupyter Notebook having code for all these analysis information can be found [here](Solution.ipynb). 