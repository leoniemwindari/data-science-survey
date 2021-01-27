# Data Science Survey : Project Overview
Data science related job is hot in the industry now. A lot of industry realizing the importance of data for their business.It is expected that the job related with data science will continue to increase each year.If you are interested in data science, whether you're a student or thinking of switching your career. You must've had this kind of questions popping in your head. Trust me, I've been there as this is also the questions I ask myself when I started my Data Science Journey.
   
## Questions :
 **General** :
    * How many percentage is the data analyst and scientist from the respondent?
    * Am I too old to be a Data Analyst or Data Scientist?
    * Gender differencies based on Role
    * Do you have to have higher education?
    
  **Technical** :
    * On which platforms should I begin on data science courses?
    * Do I have to know how to code?
    * What programming language should I learn?
    * Do Data Analyst have to know machine learning?
    * What machine learning algorithm used a lot?
    * What Machine Learning framework usually used?
    * Which of the following integrated development environments (IDEs) do they use on a regular basis?
    * What data visualization libraries or tools do they use on a regular basis?
    * Activities that make up an important part of their role at work (Data Analyst vs Data Scientist)
    * What are their favorite media sources that report on data science topics?
    * Where do you publicly share or deploy your data analysis or machine learning applications?
    * What  big data products (relational databases, data warehouses, data lakes, or similar) do they use on a regular basis?
    * What business intelligence tools do you use on a regular basis?

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





