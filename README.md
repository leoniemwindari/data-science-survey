# Data Science Survey : Project Overview
 The main focus of the project is to compare Data Analyst and Data Scientist role, like :
   * How many percentage of the respondent is a Data Analyst or Data Scientist?
   * Does data analyst have to know how to code?
   * What programming language do data analyst vs data scientist use more? and what language they recommended?
   * What is the average age of data analyst vs data scientist?
   * What IDEs they usually used on a regular basis?
   * What data visualization libraries or tools they use on a regular basis?

## Code and Resources Used 
**Python Version:** 3.7  
**Packages:** pandas, matplotlib

## Dataset
* Source : Kaggle - https://www.kaggle.com/c/kaggle-survey-2020/overview
* Methodology : The dataset is from a survey that Kaggle did by sending invitation to the entire Kaggle commmunity. It was also promoted on the Kaggle website and Twitter. The survey was from 7-30 October 2020. 
* Note : The questions consist of single and multiple choice questions. For the single choice questions, the answer were recorded in an individual columns. While for the multiple choice questions, the responses were split into multiple columns (with one column per answer)

## Data Cleaning
* The detailed questions were on the first row of the dataset, so what I did was :
1. I seperate the questions detail from the dataset and combine it into a list with the columns name
2. Remove the first row from the dataset
* Note : There are a lot of missing value but it's probably because of the multiple option that's been split into multiple columns and since the number of null is not greater than the other option, I simply did nothing to it. But I remove it when I did the analysis

## Data Transformation
* The detailed questions were on the first row of the dataset, so what I did was :
1. I seperate the questions detail from the dataset and combine it into a list with the columns name
2. Remove the first row from the dataset
* The main focus for this project is the role of Data Analyst and Data Scientist, so what I did was:
1. I make a new dataset with a filter where the role is only Data Analyst or Data Scientist
2. I set the index with a new set of ordered index (because after filtering it, the number of index will be messy and not ordered)
* After I've done a couple of analysis, I found out that what you have to do is almost the same (there is a difference when transforming data for single and multiple choice questions), so I make some function that used a lot in this analysis :
a. Function to combining answer optinon and the number of respondent for single option
b. Function to combining answer optinon and the number of respondent for multiple option
c. Function to sort dictionary based on their keys (this is to sort the bar label based on what you desired)
d. Re-arrange list of values in dictionary based on the desired arrangement (I sorted the data based on Data Analyst so I have to re-arrange the order for Data Scientist so I use this function to match it up)
e. Side by side bar chart using matplotlib (I use this to compare between data analyst and data scientist)

## EDA
(enter the graph here) (still hasn't edited yet)
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from the pivot tables. 

![alt text](https://github.com/PlayingNumbers/ds_salary_proj/blob/master/salary_by_job_title.PNG "Salary by Position")
![alt text](https://github.com/PlayingNumbers/ds_salary_proj/blob/master/positions_by_state.png "Job Opportunities by State")
![alt text](https://github.com/PlayingNumbers/ds_salary_proj/blob/master/correlation_visual.png "Correlations")


## Contact
Leonie M. Windari - @leoniemw_ds - leoniemwindari98@gmail.com





