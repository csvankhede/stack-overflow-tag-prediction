# stack-overflow-tag-prediction
This repository contains a case study of stack overflow tag prediction. Where diferent machine learning models and techniqes are used.
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
