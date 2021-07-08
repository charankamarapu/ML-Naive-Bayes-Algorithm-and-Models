# ML-Naive-Bayes-Algorithm-and-Models

## INTRODUCTION
- Naive Bayes methods are a set of supervised learning algorithms based on applying Bayes’ theorem with the “naive” assumption of conditional independence between every pair of features given the value of the class variable.
- Generally we have features for a particular class , they may be co-related and have something in common but in the context of this  algorithm we assume that all features are completely independent of each other.
- Let us look at the formula of Bayes' theorem with single feature

![Screenshot (159)](https://user-images.githubusercontent.com/72094895/124888810-13ac3800-dff4-11eb-90b2-e2aa3cdc4693.png)
- In this example we are classifying spam and ham mails , B here mean that the mail which contain the word 'Buy'.
- P(S|B) is the probablity of the mail that it is spam , by already knowing that the mail contains the word 'Buy', this is nothing but classification.
- P(B|S) is the probability of the mail that it conatins the word 'Buy' . by already knowing that it is a spam mail, this can be know by the data we have.
- P(S) is the probability of the mail to be spam, this can be know by the data we have.
- P(B|H) is the probability of the mail that it conatins the word 'Buy' . by already knowing that it is a ham mail, this can be know by the data we have.
- P(H) is the probability of the mail to be ham, this can be know by the data we have.
- As the RHS part of the formula can be solved by the data present with us we can the classify the LHS part.
- Let us now look at the formula of Bayes' theorem with more that one feature

![Screenshot (160)](https://user-images.githubusercontent.com/72094895/124890822-0c862980-dff6-11eb-8f90-0d12ad88a19e.png)
- In this example we added an another feature that is a word 'Cheap'
- P(S|(B∩C)) is the probability of the mail that it is spam ,by already knowing that mail conatains both 'Buy' and 'Cheap' words
- P(C|H) is the probability of the mail that it conatins the word 'Cheap' . by already knowing that it is a ham mail, this can be know by the data we have.
- P(C|S) is the probability of the mail that it conatins the word 'Cheap' . by already knowing that it is a spam mail, this can be know by the data we have.
- We have to notice here that we considered the features to be independent which is the main idea of navie bayes that is the reason in the RHS we have used a property of probability i.e if A,B are independent then P(A∩B)=P(A)xP(B) so,here in RHS instead of P((B∩C)|S) is wriiten as P(B|S)xP(C|S) similary with P((B∩C)|H)
- As the RHS part of the formula can be solved by the data present with us we can the classify the LHS part.
- We will have many features and we go on cascade them in the same manner.

When we provide the all the features  of a particular object the algorithm uses the formula considering those features only and give the probability of the classes to which the object belongs to.\
For better understanding give a look at the video - https://www.youtube.com/watch?v=Q8l0Vip5YUw

## When should we use Naive Bayes..?
- Naive Bayes is used for classification problems.
- It is used when the training is less.
- It gives good result if the features are really appeared to be independent.
- Naive Bayes is an eager learning classifier and it is sure fast. Thus, it could be used for making predictions in real time.
- aive Bayes classifiers mostly used in text classification (due to better result in multi class problems and independence rule) have higher success rate as compared to other algorithms. As a result, it is widely used in Spam filtering (identify spam e-mail) and Sentiment Analysis (in social media analysis, to identify positive and negative customer sentiments)

## PROS
- It is easy and fast to predict class of test data set. It also perform well in multi class prediction.
- When assumption of independence holds, a Naive Bayes classifier performs better compare to other models like logistic regression and you need less training data.
- It perform well in case of categorical input variables compared to numerical variable(s). For numerical variable, normal distribution is assumed (bell curve, which is a strong assumption).

## CONS
- If categorical variable has a category (in test data set), which was not observed in training data set, then model will assign a 0 (zero) probability and will be unable to make a prediction. This is often known as “Zero Frequency”. To solve this, we can use the smoothing technique. One of the simplest smoothing techniques is called Laplace estimation.
- Another limitation of Naive Bayes is the assumption of independent predictors. In real life, it is almost impossible that we get a set of predictors which are completely independent.

## Tips to improve the model
- If continuous features do not have normal distribution, we should use transformation or different methods to convert it in normal distribution.
- Remove correlated features, as the highly correlated features are voted twice in the model and it can lead to over inflating importance.
- If test data set has zero frequency issue, apply smoothing techniques “Laplace Correction” to predict the class of test data set.

## Types of Naive Bayes models
- Gaussian: It is used in classification and it assumes that features follow a normal distribution.\
  https://www.youtube.com/watch?v=H3EjCKtlVog \
  https://iq.opengenus.org/gaussian-naive-bayes/
- Multinomial: It is used for discrete counts. For example, let’s say,  we have a text classification problem. Here we can consider Bernoulli trials which is one step further and instead of “word occurring in the document”, we have “count how often word occurs in the document”, you can think of it as “number of times outcome number x_i is observed over the n trials”.\
  https://www.mygreatlearning.com/blog/multinomial-naive-bayes-explained/
- Bernoulli: The binomial model is useful if your feature vectors are binary (i.e. zeros and ones). One application would be text classification with ‘bag of words’ model where the 1s & 0s are “word occurs in the document” and “word does not occur in the document” respectively.\

for more info regarding types visit https://scikit-learn.org/stable/modules/naive_bayes.html


