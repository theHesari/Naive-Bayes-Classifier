# Naive Bayes

- Naive Bayes is a simple probabilistic algorithm used for classification tasks.
- Naive Bayes assumes that features and classes are unrelated to each other when the class label is known, <br>allowing it to calculate the probability of a particular class for a given set of feature values by multiplying the probabilities of each feature occurring within that class. (suppervised problems)

## kinds of Naive Bayes classifiers
There are several different kinds of Naive Bayes classifiers,<br>each suited to different types of data and assumptions about the data. <br>The most common types of Naive Bayes classifiers include:<br>

### 1. Gaussian Naive Bayes (GaussianNB):

Suitable for continuous data where features are assumed to follow a Gaussian (normal) distribution.<br>
Often used for tasks like document classification, sentiment analysis, and numerical data classification.<br>

### 2. Multinomial Naive Bayes (MultinomialNB):

Designed for discrete data, particularly text data represented as word counts or term frequency.<br>
Widely used in natural language processing for tasks like text classification, spam detection, and topic modeling.<br>

### 3. Bernoulli Naive Bayes (BernoulliNB):

Appropriate for binary or Boolean features, where each feature is either present (1) or absent (0).<br>
Commonly used in text classification, especially when dealing with binary text data (e.g., presence or absence of certain words in a document).<br>

### 4. Complement Naive Bayes (ComplementNB):

A variation of Multinomial Naive Bayes that is especially useful for imbalanced datasets.<br>
Tends to work well when the majority class overwhelms the minority class in terms of frequency.<br>
### 5. Categorical Naive Bayes (CategoricalNB):

Designed for categorical data where features have discrete, unordered values.<br>
Suitable for tasks involving categorical data, such as customer feedback analysis with categorical ratings.<br>


## Classification Report for Iris Dataset
### Dataset Overview
<br>
The Iris dataset is a well-known dataset in machine learning and consists of measurements of various characteristics of three different species of iris flowers: Setosa, Versicolor, and Virginica. For each species, four features are recorded: sepal length, sepal width, petal length, and petal width. The dataset is typically used for supervised classification tasks.
<br>

### Data Preprocessing
In this analysis, we applied preprocessing steps to convert continuous data into discrete or categorical data using transformers. Specifically, we used the KBinsDiscretizer transformer to discretize the continuous features into bins. The choice of transformer was made to make the data more compatible with certain Naive Bayes classifiers.
<br>

### Model Performance
We trained and evaluated five different Naive Bayes classifiers on the Iris dataset after preprocessing the data. Each of these classifiers is designed for specific types of data:

### 1. Gaussian Naive Bayes (GaussianNB)
**Best Data Type Supported:** GaussianNB is well-suited for continuous data, as it assumes that features follow a Gaussian (normal) distribution. <br>
**Performance Explanation:** GaussianNB performed well because it naturally handles continuous data with its Gaussian assumption. 
<br>

### 2. Multinomial Naive Bayes (MultinomialNB)
**Best Data Type Supported:** MultinomialNB is designed for discrete, count-based data, typically used in text classification with word counts or term frequency.<br>
**Performance Explanation:** MultinomialNB was not the ideal choice for the Iris dataset, as its features are not inherently discrete. Binarizing or discretizing the data may have resulted in information loss and suboptimal performance.<br> 

### 3. Bernoulli Naive Bayes (BernoulliNB)
**Best Data Type Supported:** BernoulliNB is suitable for binary or Boolean features, where each feature is either present (1) or absent (0).<br>
**Performance Explanation:** BernoulliNB was not the appropriate choice for the Iris dataset, as its features are not binary. Binarizing the data could lead to significant information loss.<br>

### 4. Complement Naive Bayes (ComplementNB)
**Best Data Type Supported:** ComplementNB is a variation of MultinomialNB and is particularly useful for imbalanced datasets.<br>
**Performance Explanation:** ComplementNB may not have been the best choice for the Iris dataset as it was not designed for continuous or discretized features. Its performance could be suboptimal due to data type mismatch.<br>

### 5. Categorical Naive Bayes (CategoricalNB)
**Best Data Type Supported:** CategoricalNB is designed for categorical data with discrete, unordered values.<br>
**Performance Explanation:** CategoricalNB may not have been the ideal choice for the Iris dataset as its features are originally continuous. Transforming them into categorical bins may have resulted in a loss of information and affected its performance.<br>

### Overall Conclusion
In summary, Gaussian Naive Bayes performed the best on the Iris dataset because it naturally handles continuous data, aligning with the dataset's original features. The other Naive Bayes classifiers, which are designed for discrete or binary data, were not the best choices for this dataset, especially after the transformation of continuous features into discrete bins. The choice of the appropriate classifier should align with the nature of the data, and for the Iris dataset, classifiers designed for continuous data would typically be more suitable.

| Classifier          | Accuracy |
|---------------------|----------|
| Gaussian Naive Bayes| 1.0     |
| Multinomial Naive Bayes | 0.76  |
| Bernoulli Naive Bayes   | 0.86  |
| Complement Naive Bayes  | 0.7  |
| Categorical Naive Bayes | 0.96  |
