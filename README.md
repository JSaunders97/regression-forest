# Regression Forest

## Introduction

Implementation of a random forest regression. Compared with a single decision tree, random forests help to reduce the tendency of indivdual decision trees to overfit to the training data. This is achieved through ensemble learning, where by many decision trees are trained on bootstrap samples with the random subspace method and the prediction is computed as the average prediction of the forest. To this end, each tree makes *'different'* mistakes which are averaged out when it comes to make a prediction. 

## Toy problem

The implementation is tested on a simple toy problem. The toy problem used is the simple surface, ![equation](https://latex.codecogs.com/gif.latex?z%20%3D%20x%5E2%20&plus;%20y%5E2%20%5Ctext%7B%20where%20%7D0%20%3C%20x%20%3C%20%5Cfrac%7B%5Csqrt%7B2%7D%7D%7B2%7D%20%5Ctext%7B%20and%20%7D%200%20%3C%20y%20%3C%20%5Cfrac%7B%5Csqrt%7B2%7D%7D%7B2%7D%20%5Ctext%7B%20such%20that%2C%20%7D%200%20%3C%20z%20%3C%201.)

1000 values were sampled from the surface, 800 were used for training and 200 used for evaluation.

![surface](https://github.com/JSaunders97/regression-forest/blob/master/Toy_Problem_Example.png)

## Training 

The single decision tree was trained on the whole training set with a maximum depth of 10. The random forest consisted of 10 trees trained on bootstrap samples of 500 from the training set with a random subset size of 2 (all features) and maximum depth of 10.

## Results

Method | Explained Variance | R^2 | Mean Squared Percentage Error (%) | Mean Squared Error
--- | --- | --- | --- | --- |
Single Decision Tree  | 0.9914 | 0.9913 | 2.1709 | 0.000345 |
Random Regression Forest | **0.9962** | **0.9947** | **1.7989** | **0.000207** |
