# DataRobot
This notebook continues the incredibly clever work from the Data Science team a BuzzFeed.

## Background 
BuzzFeed released a dataset and jupyter notebook recently that analyzed public flight data to identify potential spy planes.  This built on previous BuzzFeed stories on the same topic, which identified and verified spy planes. <br><br> Features from the 97 previously verified surveillance-planes were used as positive training examples in train.csv, as well as 500 randomly selected planes from a sample of 20,000.

BuzzFeed conducted some very clever feature engineering (described below), and used random forests to train on the 597 plane training set using a train/validation split (due to time constraints no cross-validation was done), and then ran predictions on the remaining 19,799 aircraft in their sample. 

BuzzFeed identified 69 likely surveillance planes from their RandomForest prediction, and 19,091 normal aircraft flights.  

[Github](https://buzzfeednews.github.io/2017-08-spy-plane-finder)<br>
[Original Article](https://www.buzzfeed.com/peteraldhous/spies-in-the-skies?utm_term=.phVp8l3DE#.ri7okwGBp)

# Objective
BuzzFeed's data gathering and feature engineering were extremeley clever, and highlight a critical aspect of data science: developing new features from your dataset that enhance predictions. Feature engineering is both art and science, and the team at BuzzFeed did an incredible job deconstructing available flight data to create meaningful featres. In their article, they indicate a few areas of further study that they would like to do but were not able to.  In particular, 

 * Use cross-validation on the training data set to get more generalizable predictions.  BuzzFeed fit their model on the entire training data set to set model parameters, and then ran predictions based on that fit.  While the bagging internal to Random Forests is a robust procedure against overfitting, we will use cross-validation.
 * Evaluate multiple models.  Random Forests is powerful tree-based algorithm that performs well in many settins, but DataRobot will evaluate dozens of models to see which performs best.
 
**This is exactly where leveraging the power of automated machine learning with DataRobot becomes incredibly useful: Allowing Data Scientists to focus on feature engineering, interpretation and evaluation, and letting DataRobot's powerful automation evaluate dozens of models and preprocessing steps, all designed by some of the top Data Scientists in the world**
 
In this notebook we will address the two items BuzzFeed wasn't able to get to, and in the process answer the following questions: 

* *Can we build a more robust model using DataRobot that better predicts surveillance planes?*
* *Can we identify new planes that may have been missed?* 
* *Can we identify new important features in the model, and do our important features line-up with BuzzFeed's important features?*

Chandler.mccann@datarobot.com
