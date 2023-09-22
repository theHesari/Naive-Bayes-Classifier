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


