# Breast Cancer Diagnosis
## Index
1. [Problem](#problem)
2. [Importing libraries and data](#importing-libraries-and-data)
3. [Exploratory Data Analysis](#exploratory-data-analysis)
4. [Data Split](#data-split)
5. [Model Selection](#model-selection)
6. [Result](#result)
7. [Credits](#credits)
8. [About Me](#about-me)

## Problem
The problem is to classify to the a given cancer as **Benign** or **Malignant** on the basis of a variety of medical parameters<br>
The  solution steps are given below.
## Solution
### Importing libraries and data
The first step was to import the libraies. The libraies used are:<br>
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
### Exploratory Data Analysis
The columns were checked for null values.<br>
This was followed by creation and plotting of corrrelation matrix using heatmap by Seaborn<br>
Next up, the olumns with a aboslute correlation of 0.95 with any other column was dropped from the DataFrame.<br>
Histogram and Box plot was plotted on the remaining columns<br>
The columns where the Malignant and Benign coyldnt be diffrentiated were dropped.<br>
### Data Split
The feature group, _X_ includes 20 feature rows and target, _Y_ has just the diagnosis column after encoding it to binary values<br>
The _X_ and _Y_ are split into test and train segments with a test data ize being 20% of the entire data<br>
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
* Stacked (RFR & SVM)<br>

They are passed through the function _Modelling_ and tthat gives us a dataframe containg the model accuracies and run times.<br>
The best model is selected based on runtie and model accuracy.<br>
## Result
The final result is that we were able to classify cancer diagnosis in the test set with an accuracy of 98.2%.<br>
The model we used for this is **AdaBoostClassifier** <br>
It has a run time of 0.078 seconds.<br>
## Credits
Dataset Credits : https://www.kaggle.com/uciml/breast-cancer-wisconsin-data
## About Me
Hi, I am Bhavesh Jain.<br>
I am an Engineering student with a passion for Data Science and Machine Learning.<br>
Website - https://bhaveshjain1612.github.io/ <br>
Project repository - https://github.com/bhaveshjain1612/Data-Science-and-Machine-Learning <br>
Kaggle Id - https://www.kaggle.com/me <br>
