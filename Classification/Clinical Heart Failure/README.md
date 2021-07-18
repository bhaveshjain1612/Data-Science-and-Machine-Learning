# Cardio Vascular Disease Detection
## Index
1. [Problem](#problem)
2. [Solution](#solution)
    - [Importing libraries and data](#importing-libraries-and-data)
    - [Creating Modellng class](#creating-modellng-class)
    - [Exploratory Data Analysis](#exploratory-data-analysis)
    - [Data Split](#data-split)
    - [Model Selection](#model-selection)
3. [Result](#result)
4. [Credits](#credits)
5. [About Me](#about-me)

## Problem
The problem is to prdict the _Death Event_ due to Cardio Vascular Disease as **1** (present) or **0** (absent) on the basis of a variety of medical parameters<br>
The  solution steps are given below.

## Solution

### Importing libraries and data
The first step was to import the libraries. The libraies used are:<br>
* Pandas
* Numpy
* Scikit Learn
* Matplotlib
* Seaborn
* Time 
* Xg boost<br>

11 distinct machine learning models were imported from the _Scikit Learn_ library and initalised to variables.<br>
A function _Modelling_ was created to fit and evaluate the models given to it as an input.<br>
Then the csv data was read into a dataframe using Pandas<br>
An empty column was droppend and index reassigned to _id_ column.<br>

### Creating Modellng class
A class called _Modellng_ is created to ease the procedure of fitting and selection of classsification models<br>
The inputs while initialsing are:<br>
- Training Feature Set 
- Training Target Set 
- Testing Feature Set 
- Testing Target Set 
- Array of variables (assigned to models)

The instances of the class are:<br>
- **fit()**<br>
    Model Fits the various models and records accuracies and run times<br>
    This command must be run before any other instance is called. 
- **results()**<br>
    The dataframe containing accuracy and runtimes is returned<br>
    The dataframe is sorted, firstly by accuracy (descending) then runtime(ascending)
- **best_model(type)**<br>
    Returns ther best model<br>
    Attribute, 'type', which returns Name and Model with 'name' and 'model' as respective inputs.
- **best_model_accuracy()**<br>
    Returns the acuracy of the best model
- **best_model_runtime()**<br>
    Returns the acuracy of the best model
- **best_model_predict(X_test)**<br>
    Returns the prediction based on input X_test, as predicted by best model.
-**best_model_clmatrix()**<br>
    Returns Classification Matrix after fitting with the best model
      

### Exploratory Data Analysis
The columns were checked for null values.<br>
This was followed by creation and plotting of corrrelation matrix using heatmap by Seaborn<br>
Histogram and Box plot was plotted on the coluumns where the variable distribution is continuous.<br>
COuntplots were created for boolean type features<br>

### Data Split
The feature group, _X_ includes 12 feature rows and target, _Y_ has just the DEATH_EVENT column.<br>
The _X_ and _Y_ are split into test and train segments with a test data ize being 30% of the entire data<br>

### Model Selection
The models used here are:<br>
* Imported Multi Layer Perceptron	
* Bagging	
* Gradient Boosting	
* Ada Boost	
* XG Boost	
* Logistic Regression	
* Random Forest	
* k Nearest Neighbours	
* Support Vector Machine	
Initialise _Modelling_as _classification_<br>
They are passed through the function _classification.fit()_.<br>
The _classification.results()_ gives us a dataframe containg the model accuracies and run times.<br>
The best model is selected based on runtie and model accuracy.<br>

## Result
The final result is that we were able to classify cancer diagnosis in the test set with an accuracy of 85.556%.<br>
The model we used for this is **K Neighbors Classifier** <br>
It has a run time of 0.013 seconds.<br>

## Credits
Dataset Credits : https://www.kaggle.com/andrewmvd/heart-failure-clinical-data

## About Me
Hi, I am Bhavesh Jain.<br>
I am an Engineering student with a passion for Data Science and Machine Learning.<br>
Website - https://bhaveshjain1612.github.io/ <br>
Complete ML repository - https://github.com/bhaveshjain1612/Data-Science-and-Machine-Learning <br>
Kaggle Id - https://www.kaggle.com/bhaveshjain1612 <br>
