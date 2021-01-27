# Data Science Survey : Project Overview
 The main focus of the project is to compare Data Analyst and Data Scientist role, like :
   * How many percentage of the respondent is a Data Analyst or Data Scientist?
   * Does data analyst have to know how to code?
   * What programming language do data analyst vs data scientist use more? and what language they recommended?
   * What is the average age of data analyst vs data scientist?
   * What IDEs they usually used on a regular basis?
   * What data visualization libraries or tools they use on a regular basis?
   * Does data analyst have to know machine learning? If yes, which machine learning algorithm they use the most?
   * Which machine learning frameworks do they used on a regular basis?
   * What is the most important activities in their role at work?
   * How much do they make?(Comparison and distribution of the salary)
   * What are their favorite media sources that report on data science topics?
   * Where do they usually deploy their data analysis or machine learning applications?
   * Which platform to they use to completed data science courses?
   * Do you have to have a higher education?
   * Gender differencies in Data Analyst and Data Scientist Role
   * Salary based on Gender and Education
   * What cloud computing platforms do they use on a regular basis?
   * What big data products (relational databases, data warehouses, data lakes, or similar) do they use on a regular basis?
   * What business intelligence tools do they use on a regular basis? and used most often?
   
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
* The salary column is in a range value and in inconsistent format so I change it into the average of the range value
* Sort the x ticks based on the number of years(which have a range value and inconsistent format)

## Data Transformation
* The detailed questions were on the first row of the dataset, so what I did was :
    1. I seperate the questions detail from the dataset and combine it into a list with the columns name
    2. Remove the first row from the dataset
* The main focus for this project is the role of Data Analyst and Data Scientist, so what I did was:
    1. I make a new dataset with a filter where the role is only Data Analyst or Data Scientist
    2. I set the index with a new set of ordered index (because after filtering it, the number of index will be messy and not ordered)
* After I've done a couple of analysis, I found out that what you have to do is almost the same (there is a difference when transforming data for single and multiple choice questions), so I make some function that used a lot in this analysis :
    1. Function to combining answer optinon and the number of respondent for single option
    2. Function to combining answer optinon and the number of respondent for multiple option
    3. Function to sort dictionary based on their keys (this is to sort the bar label based on what you desired)
    4. Re-arrange list of values in dictionary based on the desired arrangement (I sorted the data based on Data Analyst so I have to re-arrange the order for Data 
       Scientist so I use this function to match it up)
    5. Side by side bar chart using matplotlib (I use this to compare between data analyst and data scientist)


## EDA
I looked at the distributions of the data and the value counts for the various categorical variables. Below are a few highlights from the pivot tables. 

![alt text](https://github.com/leoniemwindari/data-science-survey/blob/main/index1.png)
![alt text](https://github.com/leoniemwindari/data-science-survey/blob/main/education%20based%20on%20role.png)
![alt text](https://github.com/leoniemwindari/data-science-survey/blob/main/platform%20courses%20usesd%20to%20learn.png)
![alt text](https://github.com/leoniemwindari/data-science-survey/blob/main/programming%20language.png)
![alt text](https://github.com/leoniemwindari/data-science-survey/blob/main/ml%20algorithm%20used.png)


## Contact
Leonie M. Windari - @leoniemw_ds - leoniemwindari98@gmail.com
Website - 





