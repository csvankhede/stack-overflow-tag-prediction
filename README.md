# stack overflow tag prediction
![SO_Tag_Prediction2](https://user-images.githubusercontent.com/25454660/62774821-999b6d80-bac3-11e9-8876-5fbd6dc0151b.jpg)
This repository contains a case study of stack overflow tag prediction. Where diferent machine learning models and techniqes are used.
### Data Overview
Refer: https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/data 
* All of the data is in 2 files: Train and Test.
* Train.csv contains 4 columns: Id,Title,Body,Tags.
* Test.csv contains the same columns but without the Tags, which you are to predict.
* Size of Train.csv - 6.75GB
* Size of Test.csv - 2GB

Number of rows in Train.csv = 6034195

The questions are randomized and contains a mix of verbose text sites as well as sites related to math and programming. The number of questions from each site may vary, and no filtering has been performed on the questions (such as closed questions).

#### Data Field Explaination
Dataset contains 6,034,195 rows. The columns in the table are:
* Id - Unique identifier for each question
* Title - The question's title
* Body - The body of the question
* Tags - The tags associated with the question in a space-seperated format (all lowercase, should not contain tabs '\t' or ampersands '&')

### Problem Statemtent

Suggest the tags based on the content that was there in the question posted on Stackoverflow. 

#### Source: https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/

### Type of Machine Learning Problem
It is a multi-label classification problem 

### Preprocessing
* Sample 1M data points
* Separate out code-snippets from Body
* Remove Spcial characters from Question title and description (not in code)
* Remove stop words (Except 'C')
* Remove HTML Tags
* Convert all the characters into small letters
* Use SnowballStemmer to stem the words

### Loss of each Machine Learning models
<table>
  <th><td>Model</td><td>	precision micro</td><td>	recall micro</td><td>	f1 score micro	</td><td>precision macro	</td><td>recall macro	</td><td>f1 score macro</th>
<tr><td>0</td><td>	Logistic regression(OvR) 4 grams</td><td>	0.773217	</td><td>0.577346	</td><td>0.661078	</td><td>0.345109	</td><td>0.192955	</td><td>0.234645</td><tr>
<tr><td>1</td><td>	Logistic regression hyperpara tuning</td><td>	0.773217</td><td>	0.577346	</td><td>0.661078	</td><td>0.345109	</td><td>0.192955	</td><td>0.234645</td><tr>
<tr><td>2</td><td>	Linear SVM(OvR)</td><td>	0.779737</td><td>	0.511716	</td><td>0.617915	</td><td>0.200884</td><td>	0.168827	</td><td>0.160631</td><tr>
</table>

#### Here logistic regression 4 grams gives better result.
