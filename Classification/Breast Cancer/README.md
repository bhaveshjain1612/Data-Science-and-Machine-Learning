# Breast Cancer Diagnosis
## Problem
The problem is to classify to the a given cancer as **Benign** or **Malignant** on the basis of a variety of medical parameters
## Solution
### Importing libraries and data
The first step was to import the libraies. The libraies used are Pandas, Numpy, Scikit Learn, Matplotlib, Seaborn, Time and Xg boost.<br>
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
<ul>
<li>Imported Multi Layer Perceptron	</li>
<li>Bagging	</li>
<li>Gradient Boosting	</li>
<li>Ada Boost	</li>
<li>XG Boost	</li>
<li>Logistic Regression	</li>
<li>Random Forest	</li>
<li>k Nearest Neighbours	</li>
<li>Support Vector Machine	</li>
<li>Stacked (RFR & SVM)</li>
</ul>
They are passed through the function _Modelling_ and tthat gives us a dataframe containg the model accuracies and run times.<br>
The best model is selected based on runtie and model accuracy.<br>
## Result
The final result is that we were able to classify cancer diagnosis in the test set with an accuracy of 98.2%.<br>
The model we used for this is **AdaBoostClassifier** <br>
It has a run time of 0.078 seconds.<br>
## Credits
Dataset Credits : https://www.kaggle.com/uciml/breast-cancer-wisconsin-data
