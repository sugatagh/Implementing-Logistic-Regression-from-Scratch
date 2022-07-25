# Implementing Logistic Regression from Scratch

## Kaggle Notebook

[Implementing Logistic Regression from Scratch](https://www.kaggle.com/code/sugataghosh/implementing-logistic-regression-from-scratch)

## Classification

In [statistics](https://en.wikipedia.org/wiki/Statistics) and [machine learning](https://en.wikipedia.org/wiki/Machine_learning), [classification](https://en.wikipedia.org/wiki/Statistical_classification) refers to a type of [supervised learning](https://en.wikipedia.org/wiki/Supervised_learning). For this task, training data with known class labels are given and is used to develop a [classification rule](https://en.wikipedia.org/wiki/Classification_rule) for assigning new unlabeled data to one of the classes. A special case of the task is [binary classification](https://en.wikipedia.org/wiki/Binary_classification), which involves only two classes. Some examples:

- Classifying an email as `spam` or `non-spam`
- Classifying a tumor as `benign` or `malignant`

The algorithms that sort unlabeled data into labeled classes are called *classifiers*. Loosely speaking, the [sorting hat](https://en.wikipedia.org/wiki/Magical_objects_in_Harry_Potter#Sorting_Hat) from [Hogwarts](https://en.wikipedia.org/wiki/Hogwarts) can be thought of as a classifier that sorts incoming students into four distinct houses. In real life, some common classifiers are [logistic regression](https://en.wikipedia.org/wiki/Logistic_regression), [k-nearest neighbors](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm), [decision tree](https://en.wikipedia.org/wiki/Decision_tree_learning), [random forest](https://en.wikipedia.org/wiki/Random_forest), [support vector machine](https://en.wikipedia.org/wiki/Support-vector_machine), [naive Bayes](https://en.wikipedia.org/wiki/Naive_Bayes_classifier), [linear discriminant analysis](https://en.wikipedia.org/wiki/Linear_discriminant_analysis), [stochastic gradient descent](https://en.wikipedia.org/wiki/Stochastic_gradient_descent), [XGBoost](https://en.wikipedia.org/wiki/XGBoost), [AdaBoost](https://en.wikipedia.org/wiki/AdaBoost) and [neural networks](https://en.wikipedia.org/wiki/Artificial_neural_network).

## The Purpose of the Notebook

Many advanced libraries, such as [scikit-learn](https://en.wikipedia.org/wiki/Scikit-learn), make it possible for us to train various models on labeled [training data](https://en.wikipedia.org/wiki/Training,_validation,_and_test_data_sets#Training_data_set), and predict on unlabeled [test data](https://en.wikipedia.org/wiki/Training,_validation,_and_test_data_sets#Test_data_set), with a few lines of codes. While it is very convenient for day-to-day practice, it does not give insight into the details of what really happens underneath, when we run those codes. In the present notebook, we implement a logistic regression model manually from scratch, without using any advanced library, to understand how it works in the context of binary classification. The basic idea is to segment the computations into pieces, and write functions to compute each piece in a sequential manner, so that we can build a function on the basis of the previously defined functions. Wherever applicable, we have complemented a function which is constructed using for loops, with a much faster vectorized implementation of the same.