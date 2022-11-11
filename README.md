# Email classification based on Bayesian analysis
Group Members: Yuhuan Ma, XXX and XXX
### Introduction
If you have an email account, we are sure that you have seen emails being categorised into different buckets and automatically being marked important, spam, promotions, etc. It's wonderful to see machines being so smart and doing the work for us. In other words, spam email, or junk email, refers to unsolicited messages sent in bulk, which has a reputation of being ubiquitous, repetitive and unavoidable. 
### Data Collection
We will collect datasets from open source 
Eg. 
https://github.com/shijing888/BayesSpam
https://archive.ics.uci.edu/ml/machine-learning-databases/00228/. 
And we try to collect more datasets from Internet.
### Method
Like Naive Bayes, other classifier algorithms like Support Vector Machine, or Neural Network also get the job done! We choose Naive Bayes as learning algorithm used  learning algorithm. Naive Bayes is a probabilistic algorithm based on the Bayes Theorem used for email spam filtering in data analytics. In this situation, the formula can be written as:
![image](https://github.com/halona2333/Bayes/blob/main/Images/bayes1.svghttps://github.com/halona2333/Bayes/blob/main/Images/bayes1.png)
For instance, the probability of the word “FREE” appears in an email is 20%, the probability of an email being a spam is 25%, and the probability of a junk email has the word “FREE” is 45%. Then, when an email contains the word “FREE” was received by a user than the system will calculate the probability of this email is a spam according to the Bayes’ theorem is 56%.
### Performance
First, we use unused parts of the dataset as our test set. Then, we use some of the e-mails in our account as a test set.
