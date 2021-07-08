# ML-Naive-Bayes-Algorithm-and-Models

## INTRODUCTION
- Naive Bayes methods are a set of supervised learning algorithms based on applying Bayes’ theorem with the “naive” assumption of conditional independence between every pair of features given the value of the class variable.
- Generally we have features for a particular class , they may be co-related and have something in common but in the context of this  algorithm we assume that all features are completely independent of each other.
- Let us look at the formula of Bayes' theorem with single feature

![Screenshot (159)](https://user-images.githubusercontent.com/72094895/124888810-13ac3800-dff4-11eb-90b2-e2aa3cdc4693.png)
- In the example we are classifying spam and ham mails , B here mean that the mail which contain the word 'Buy'.
- P(S/B) is the probablity of the mail that it is spam , by already knowing that the mail contains the word 'Buy', this is nothing but classification.
- P(B/S) is the probability of the mail that it conatins the word 'Buy' . by already knowing that it is a spam mail, this can be know by the data we have.
- P(S) is the probability of the mail to be spam, this can be know by the data we have.
- P(B/H) is the probability of the mail that it conatins the word 'Buy' . by already knowing that it is a ham mail, this can be know by the data we have.
- P(H) is the probability of the mail to be ham, this can be know by the data we have.
- As the RHS part of the formula can be solved by the data present with us we can the classify the LHS part.
- Let us now look at the formula of Bayes' theorem with more that one feature
