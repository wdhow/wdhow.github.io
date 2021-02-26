# Machine Learning Notes

## What is machine learning?
It is the science and art of programming computers so they can learn from data (without being explicitly programmed).

In a spam filter, the data the program learns from is called a training set. Each example of the data is called a training instance or sample.

Data mining is when you employ ML techniques to dig into large amounts of data is help discover patterns that were no immediately apparent.

### Applications of ML
* Convolutional neural networks - Analyzing images to classify them
* Natural language processing - automatically classify news articles, flagging offensive comments on a forum, summarizing news articles (text summarization)
* Anomaly detection - detecting credit card fraud
* Clustering - segmenting clients based on their purchases
* Recommender system - recommending a client a product that they might be interested in based on past pruchases
* Reinforcement learning - building a bot for a game

### Types of ML systems
* whether or not trained with human supervision (unsupervised / supervised, semi-supervised, reinforcement learning)
* can they learn incrementally or on the fly? (online vs batch learning)
* do they work by comparing new data points to known data points, or by deteching patterns in training data and building a predictive model (instance based vs model based learning)

## Supervised / unsupervised learning
### Supervised learning
The training set you feed the algorithm includes desired solutions called 'labels'.

In machine learning, an attribute is a data type (eg. milage) while a feature has several meanings but generally means an attribute plus its value.

Examples of supervised learning algorithms:
* k-Nearest neighbour
* linear regression
* logistic regression
* support vector machines
* decision trees and random forests
* neural networks

### Unsupervised learning
Training data is unlabeled - the system tries to learn without a teacher.

Clustering:
* K-Means
* DBSCAN
* Heirarchiacal cluster analysis

Anomaly detection:
* One class SVM
* Isolation forest

Visualization and dimensionality reduction:
* Principal component analysis
* Kernel PCA
* Locally linear embedding
* t-Distributed stochastic neighbour embedding

Association rule learning:
* Apriori
* Eclat

Feature extraction is when you collapse two correlating features into one (eg. milage and age for a car). This can improve speed of the algorithm and take up less disk and memory.

* Anomaly detection is where you train algorithm with normal samples during training.
* novelty detection is when you train to detect new instances that look different from all instances in the training set. this requires having a clean training set devoid of any instance you would like the algorithm to detect.
* association rule learning - to dig into large amounts of data and discover interesting relations between attributes.

### Semisupervised learning
Labelling data is expensive and time consuming. There will be lots of unlabelled instances compared to labeled. Some algorithms deal with data that's partially labeled - semisupervised learning.

### Reinforcement learning
The learning system is called an agent can observe the environment, select and perform actions and gets rewards in return (or penalties!). It must learn by itself what is the best strategy (called policy) to get the most reward over time.

### Batch learning
System is incapable of learning incrementally - it must be trained using all the available data. This will take a lot of time and resources (typically done offline). First the system is trained, then launched to production and runs without learning anymore. This is called offline learning. If you want it to learn new data, you need to train a new version of the system from scratch, stop the old one and replace it.

This can be automated, making it feasable, however retraining could potentially take hours, requiring daily updates. You might need a more reactive system. It is also very resource intensive and could cost a lot.

### Online learning
In online learning you train the system incrementally by feeding it data instances sequentially or in small groups called mini-batches. The system can learn on the fly. This is great for systems which receive data continuously and have limited resources. Once the learning system has learned about new instances, it can discard them, saving space. Can also be used to train on huge datasets too large to fit into memory.

Learning rate - how fast they adapt to changing data. If set high, it will adapt to new data faster, but forget old data quicker. If you set to learn slowly, it will have more interia - learn slower but be less sensitive to noise in the new data. This would need to be monitored.

### Instance based learning
System will classify based on measure of similarity. (Eg flag spam with similar word count to other spam). The system learns examples by heart and generalizes to new cases by using a similarity measure.

### Model based learning
Build a model of examples and use it to make predictions. eg. finding a correlation between GDP and quality of life index (linear model).

Sampling bias occurs when the sampling method is flawed

Overfitting data - when the model overgeneralizes!