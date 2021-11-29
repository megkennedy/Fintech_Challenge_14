# Fintech_Challenge_14
UW Fintech Bootcamp Challenge 14

In this challenge I am a financial advisor who is attempting to improve the existing trading signals system with machinge learning.



## Contributors

As always a shout out to my professer, TAs, and classmates for all their help during this process


## Libraries and dependencies needed

import pandas as pd

import numpy as np

from pathlib import Path

import hvplot.pandas

import matplotlib.pyplot as plt

from sklearn import svm

from sklearn.preprocessing import StandardScaler

from pandas.tseries.offsets import DateOffset

from sklearn.metrics import classification_report

from sklearn.ensemble import AdaBoostClassifier


## Tuning the Baseline Trading Algorithm

In this challenge we were given a baseline algorithm with SMA_short=4, SMA_long=100, and DateOffset=3. This baseline was considered model 1. I then changed a variable to see if I could improve the algorithm, which were the subsequent models.


### Model 1

Model one has a DateOffset of 3 months

SMA short =4

![Model 1 plot](https://user-images.githubusercontent.com/88640228/143805802-299fe8cf-ea09-4b6d-8536-4a7c7a1688e1.png)


### Model 2

Model two has a DateOffset of 6 months

SMA short=4

![Model 2 plot](https://user-images.githubusercontent.com/88640228/143805836-4d44d80c-6410-4be9-bb19-29a075937803.png)


### Model 3

Model three has a DateOffset of 3 months

SMA short=20

![Model 3 plot](https://user-images.githubusercontent.com/88640228/143805849-62ea537d-6ecb-42b7-8c55-7968ad265dbf.png)

### Model 4

Model four has a DateOffset of 4 months

SMA short =4

![Model 4 plot](https://user-images.githubusercontent.com/88640228/143805871-bbd4a386-8421-4469-b1ce-eb4455369b1b.png)


### Model Manipulation Analysis
When adjusting the SMA short and the SMA long (not pictured) it made the model's predictions less accurate. Therefore, further adjustments were made to the DateOffset to see if that would increase the accuracy of the predictions. While six month offset showed fair accuracy when comparing the actual returns line to the strategy returns, when the DateOffset was reset to 8 (not pictured) the resulting graph was less accurate. The final model chosen was a DateOffset of four months which once again shows the two lines running close together. 


## Evaluating a New Machine Learning Classifier

The final task in this challenge was to use a different classifier and compare it to the original model. I chose to use AdaBoost.

### AdaBoost Plot

![Ada_plot](https://user-images.githubusercontent.com/88640228/143808925-dcb9a774-73d4-452e-950d-30d4d8257890.png)

### Evaluation

As seen in the above plot the AdaBoost Classifier was not better than the original model. When running the AdaBoost model the data parameters were left at the Model 4 settings and the accuracy for the AdaBoost Actual vs Strategy lines was way off. Perhaps adjusting the model parameters (e.g. SMA_short or DateOffset) before running it would provide a better outcome for this classifier.


