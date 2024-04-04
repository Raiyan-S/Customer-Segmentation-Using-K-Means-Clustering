# Customer-Segmentation-Using-K-Means-Clustering
# Overview
Our project focuses on customer segmentation using K-Means clustering, a powerful technique for grouping customers based on similarities in their attributes or behavior.
By dividing customers into distinct segments, businesses can tailor their marketing strategies more effectively, leading to improved customer satisfaction and retention.

## Introduction
Customer segmentation is a pivotal strategy in marketing that involves dividing a broad
customer base into distinct groups with similar characteristics, behaviors, or needs. This
process allows businesses to better understand their customers, tailor their marketing efforts,
and deliver more personalized products or services.

Segmentation criteria can vary widely, including demographic factors like age, gender, income,
or geographic location, as well as psychographic traits such as lifestyle, values, interests, and
behavior patterns. By identifying these segments, companies can create targeted marketing
campaigns, develop products that meet specific needs, and improve customer satisfaction and
loyalty.

In this project, we are going to apply Machine Learning concepts to Customer Segmentation
problems, and see how it could be beneficial for business stakeholders.

## The Problem Statement
The task at hand involves devising a strategy for customer segmentation to optimize
marketing tactics using a dataset summarizing the behaviors of approximately 9000 active
credit card holders over the past half-year. This dataset encompasses 18 behavioral indicators at
an individual customer level, portraying their spending patterns and account activities.

## Objectives
1. Explore ML Algorithms for Customer Segmentation: Let's check out different ML
   tools that can help us group customers better. Think of it like finding the right tool for
   the job.
   
2. Fit Machine Learning into Business Strategies: We'll see how ML can be part of our
   bigger business plan. It's not just about technology; it's about making our business goals
   a reality.
   
3. Apply data wrangling methods: Machine Learning can be tricky. We'll look at
   common problems like poorly structured data and confusing results and figure out how
   to resolve them.
   
4. See the Impact on Marketing: Lastly, we'll measure how using ML for customer
   segmentation affects our marketing efforts. It's not just about numbers; it's about
   making customers happy and boosting businesses.

## Background
In this section, we are going to discuss important concepts that are going to be used in our project.

### Machine Learning
Machine learning is a subset of artificial intelligence (AI) that focuses on the development of
algorithms and statistical models that enable computer systems to improve their performance
on a specific task through experience and without explicit programming. The goal of machine
learning is to develop models that can generalize patterns from data and make predictions or
decisions without being explicitly programmed for the given task.

There are three main types of machine learning:
1. Supervised Learning
2. Unsupervised Learning
3. Reinforcement Learning
   
We are going to give a brief about each of them.

#### Supervised Learning
Supervised learning, a fundamental machine learning approach, operates on labeled datasets.
These datasets serve as guides, and training algorithms to accurately classify data or predict
outcomes. By utilizing labeled inputs and outputs, the model gauges its accuracy and
progressively learns over iterations. It involves two primary types of problems: classification
and regression.

* Classification: Algorithms sort test data into specific categories, such as separating
apples from oranges or filtering spam emails from your inbox. Common algorithms
include linear classifiers, support vector machines, decision trees, and random forests.

* Regression: This method explores relationships between dependent and independent
variables, predicting numerical values. For instance, it forecasts sales revenue based on
various data points. Popular regression algorithms encompass linear, logistic, and
polynomial regression models.

#### Unsupervised Learning
Unsupervised learning relies on machine learning algorithms to analyze and cluster
unlabeled datasets. These algorithms autonomously uncover underlying patterns within the
data, operating without human intervention during the learning but, it need human validation
for output variables. There are two forms of unsupervised learning, clustering and association.

* Association: An unsupervised learning technique seeks relationships between
variables within a dataset using various rules. Often applied in the market basket
analysis and recommendation engines, it facilitates suggestions like "Customers
Who Bought This Item Also Bought," aiding in personalized recommendations.

* Clustering: An Unsupervised data exploration technique employed in data mining to
group unlabeled data based on their similarities or differences. Each cluster is
represented by a single point, called the centroid, which is the mean of all data
points in a cluster. There are multiple clustering methods, let’s discuss one of
the simplest ones, that is K-means clustering.

#### K-means
Operates iteratively, it aims to partition a dataset into 'k' predefined and non-
overlapping subgroups. Each data point is assigned to a single subgroup, contributing to the
formation of distinct and separate clusters. The steps of the K-means clustering method are as
follows:

1. Start by randomly initializing the cluster centroid.
   
2. Determine cluster membership of each input.
   
3. Re-compute cluster centroids.
   
4. Repeat step 2 until the stopping criteria are met (i.e. centroids do not
change across iterations).

It is important to determine the ideal number of clusters to use, for that, we are going to use a
method called the elbow method. Moreover, we need to evaluate the accuracy of K-means
clustering on our dataset. We are going to use the Silhouette score for that.

#### The Elbow Method
The method is a minor method that is applied alongside K-means clustering
to find the ideal value for ‘K’ which makes our model perform better. Let’s
break it down into 4 steps:

1. Run the clustering algorithm for different values for ‘k’(i.e. from 1 to 10
    clusters).
   
2. For each ‘k’, calculate the total within-cluster sum of squares (WSS).
```math
WSS = \sum_{i=1}^K \sum_{x \in k_{i}}  distance(x,Centroid_{i})
```

3. Plot WSS with respect to K.
   
4. The Location of a bend (elbow) in the plot is generally considered as an
    indicator of the appropriate number of clusters.


## FIGURE 1 : AN EXAMPLE OF THE ELBOW METHOD
![](https://github.com/Raiyan-S/Customer-Segmentation-Using-K-Means-Clustering/blob/main/Elbow%20method.png)

#### The Silhouette Score
The Silhouette Score is a metric for evaluating how well each data point fits
its assigned cluster compared to other clusters. Let’s break down how the
silhouette score is calculated:

1. Calculating the average distance (𝑎𝑖) to other data points within the same
    cluster for each data point.
  
2. Computing the average distance (𝑏𝑖) to all other clusters that the data
    point doesn't belong to. The Silhouette score is determined through the formula:
```math
S𝑖𝑙ℎ𝑜𝑢𝑒𝑡𝑡𝑒 𝑆𝑐𝑜𝑟𝑒 = \frac{(b_{i}-a)}{max(a_{i},b_{i})}
```

Obtaining an overall Silhouette score involves averaging the Silhouette
scores calculated for each data point, providing a measure of the effectiveness of
the clustering outcomes. The score ranges from -1 to +1. Positive scores signify
that data points are appropriately assigned to their clusters, indicating effective
clustering outcomes. A score of zero implies the presence of overlapping
clusters or data points equidistant from multiple clusters. Negative scores
indicate the misassignment of data points to inappropriate clusters, reflecting
suboptimal clustering outcomes.

## Supervised Learning vs. Unsupervised Learning
![](https://github.com/Raiyan-S/Customer-Segmentation-Using-K-Means-Clustering/blob/main/Supervised%20and%20Unsupervised.png)

## Customer segmentation in Artificial Intelligence
Customer segmentation is the process of dividing a customer base into groups of
individuals that are similar in certain ways relevant to marketing, such as age, gender, interests,
and spending habits. It enables companies to target specific groups with tailored promotions,
products, or services that are most likely to resonate with them. The following paragraph
illustrates an example of how customer segmentation works.

## FIGURE 2 : SEGMENTIZING CUSTOMERS IN A TARGET MARKET BASED ON CERTAIN FEATURES
![](https://github.com/Raiyan-S/Customer-Segmentation-Using-K-Means-Clustering/blob/main/Segmentizing%20customers.png)

After looking at this figure, we can realize that the customer segmentation problem is basically
a clustering problem. Hence, we can conclude that there is a relationship between it and
Machine Learning brings us to use Machine Learning algorithms to segmentize the
customers appropriately.

### Domain problem
The domain we chose to segmentize is a bank, which raises a question, how are we going to use
AI with that? Well, we have a dataset that represents that bank, it contains information regarding
users and their credit cards’ info. We are going to use this dataset and apply machine learning
algorithms on it to segmentize it. However, this dataset is huge! When we have too much information
that some of them are irrelevant to our problem, a well-known problem in the field of data
called “The Curse of Dimensionality”.

## FIGURE 3: CLASSIFIER PERFORMANCE BASED ON THE NUMBER OF FEATURES
![](https://github.com/Raiyan-S/Customer-Segmentation-Using-K-Means-Clustering/blob/main/Curse%20of%20Dimensionality.png)

### The Curse of Dimensionality
In the context of data analysis and machine learning, dimensions refer to the features or
attributes of data. The Curse of Dimensionality encompasses a range of difficulties and
intricacies that emerge when examining and structuring data within spaces characterized by a
high number of dimensions.

So how do we resolve such a problem? By using the Principal Component
Analysis method (PCA).

#### PCA
The Principal Component Analysis method (PCA) is a method that helps you avoid the
curse of dimensionality without losing valuable features. What it does is simply:
* Decorrelation of features.
* Reduction of dimensionality.

## FIGURE 4: APPLYING PCA ON A 3D DATA
![](https://github.com/Raiyan-S/Customer-Segmentation-Using-K-Means-Clustering/blob/main/PCA.png)
