# Email classification based on Bayesian analysis
Group Members: Yuhuan Ma, Yifei He and Ziqing Tang

### 1. Introduction
If you have an email account, we are sure that you have seen emails being categorised into different buckets and automatically being marked important, spam, promotions, etc. It's wonderful to see machines being so smart and doing the work for us. In other words, spam email, or junk email, refers to unsolicited messages sent in bulk, which has a reputation of being ubiquitous, repetitive and unavoidable. In this project, we will understand briefly about the Naive Bayes Algorithm and try to label spam email by algorithm.

### 2. Data Collection
We will collect datasets from open source. And we try to collect more datasets from Internet. Some online resources for datasets
*  https://www.kaggle.com/datasets
*  https://archive.ics.uci.edu/ml/datasets.php
*  https://www.csie.ntu.edu.tw/˜cjlin/libsvmtools/datasets/
*  https://en.wikipedia.org/wiki/List_of_datasets_for_machine-learning_research

We find some datasets such as following:

English Spam Dataset
* [Spam Mail 📧 Classifier](https://www.kaggle.com/code/syamkakarla/spam-mail-classifier)
* [smsspamcollection](https://archive.ics.uci.edu/ml/machine-learning-databases/00228/)

Chinese Spam Dataset
 * [BayesSpam](https://github.com/shijing888/BayesSpam)


### 3. Method
Like Naive Bayes, other classifier algorithms like Support Vector Machine, or Neural Network also get the job done! We choose Naive Bayes as learning algorithm used  learning algorithm. Naive Bayes is a probabilistic algorithm based on the Bayes Theorem used for email spam filtering in data analytics. In this situation, the formula can be written as:

![image](https://github.com/halona2333/Bayes/blob/main/Images/bayes1.png)

For instance, the probability of the word “FREE” appears in an email is 20%, the probability of an email being a spam is 25%, and the probability of a junk email has the word “FREE” is 45%. Then, when an email contains the word “FREE” was received by a user than the system will calculate the probability of this email is a spam according to the Bayes’ theorem is 56%. At the same time, the cost of classifying a legitimate email into spam is far larger than classifying a junk email into legitimate. So the system might not ignore this email. However, as the amount of data becomes larger, the accuracy will also be improved. According to another study, only when the probability is as high as 99%, they will make the decision and filter this email.

However, this formula only indicates the probability of an email being a spam based on a single word appears in the email. Many other indicators, like the domain type of the sender (.edu or .org), or whether it has an attachment or not, should also be taken into consideration in real email spam filtering. We should be carefully to choose features for  email spam filtering.

We use build-in implementation in our project to compare performance, Some information of this built-in implementation can be find here ([naive_bayes]https://scikit-learn.org/stable/modules/naive_bayes.html).



### Performance
We choose three as indicators to measure your performance of the task, including accuracy, precision [(spam and label as spam)/(labeled as spam)] and recall rate [(spam and label as spam)/(all spam)].

Three built-in implementation performace as following in Dataset 1([Spam Mail 📧 Classifier](https://www.kaggle.com/code/syamkakarla/spam-mail-classifier)).
* BernoulliNB():
accuracy: 0.9101, precision: 0.8632, recall: 0.8200
* MultinomialNB():
accuracy: 0.9507, precision: 0.8807, recall: 0.9600
* ComplementNB():
accuracy: 0.9527, precision: 0.8815, recall: 0.9667
* Our methods:
accuracy 0.9353, precision: 0.8416, recall: 0.9567

