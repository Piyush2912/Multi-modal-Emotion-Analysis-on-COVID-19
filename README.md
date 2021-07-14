# Multi-modal-Emotion-Analysis-on-COVID-19

## An Emotion Care Model using Multimodal Textual Analysis on COVID-19
A novel emotion care scheme has been proposed in this project to analyze multimodal textual data contained in real-time tweets related to COVID-19.

## Demonstration of Project:
<p align="center" >
  <img src="https://user-images.githubusercontent.com/47279598/125491350-d92c5a59-3002-4dee-8975-fecdf4db89fa.gif" />
</p>


### Link for Research Paper: https://www.sciencedirect.com/science/article/abs/pii/S0960077921000618
### Contributed in other researches: https://scholar.google.com/citations?user=73b_WZcAAAAJ&hl=en
### Link to the EmotionofIndia.com : http://emotionofindia.herokuapp.com/# 
### Link to Download Complete Dataset: https://github.com/Piyush2912/Twitter_dataset


## How to use?
1. Download the required files into a directory if your choice.
2. Open required codes in Jupyter Notebook.  
3. Install the dependencies as mentioned in code.
4. Execute the code block by block.
5. Get visualized results.
6. Done

## Table of Contents: 
1. Abstract
2. Motivation
3. Problem Statement
4. Introduction
5. Requirements
6. Dataset Creation
7. Generic Methodology
8. Results
9. Summary and Conclusion
10. Limitations
11. Future Scope
12. Credits
13. License

## 1. Abstract
- At the dawn of the year 2020, the world was hit by a significant pandemic COVID-19, that traumatized the entire planet.
- The infectious spread grew in leaps and bounds and forced the policymakers and governments to move towards lockdown.
- The lockdown further compelled people to stay under house arrest, which further resulted in an outbreak of emotions on social media platforms.
- Perceiving people's emotional state during these times becomes critically and strategically important for the government and the policymakers.
- In this regard, a novel emotion care scheme has been proposed in this project to analyze multimodal textual data contained in real-time tweets related to COVID-19.


## 2. Motivation
- In the rapid developing world, with increasing in technology so is increasing diseases such as Covid-19.
- To prevent the spread of disease, it is absolutely necessary to analyze and act correctly.
- There is a need for perceiving people's emotional state during these times becomes critically and strategically important for the government and the policymakers.

## 3. Problem Statement
- The goal is to identify the emotions of people living in different states of India during the phases of lockdown.
- There is availability of huge amount of data in Twitter which needs to be analyzed.
- There is an absolute need for classification into categories in order to analyze efficiently. 
- In order to categories, there is a need to develop an effective algorithm for investigation of data.


## 4. Introduction
- This project studies 8-scale emotions (Anger, Anticipation, Disgust, Fear, Joy, Sadness, Surprise, and Trust) over multiple categories such as nature, lockdown, health, education, market, and politics.
- This is the first of its kind linguistic analysis on multiple modes pertaining to the pandemic to the best of our understanding. 
- An interactive internet application has also been developed for the same.
<p align="center">
  <img src="https://user-images.githubusercontent.com/47279598/125605114-e928e43e-1557-493e-aaaa-6862fb22b316.png"/>
</p>
<p align=center> 
Figure 1: Web Application 
</p>

## 5. Requirements
All the experimental trials have been conducted on a laptop equipped by an Intel i7-8750H processor (4.1 GHz), 16 GB of RAM with 1050ti max-Q with 4 GB of VRAM. 
The Jupyter Notebook software equipped with Python 3.8 kernel was selected in this project for the development and implementation of the different experimental trails.

- Jupyter Notebook version 6.1 or above
- Python version 3.8 or above
- NRC Emotion Lexicons - http://saifmohammad.com/WebPages/NRC-Emotion-Lexicon.html
- Python Libraries Used:
  - numpy https://numpy.org/doc/
  - pandas https://pandas.pydata.org/docs/
  - string https://docs.python.org/3/library/string.html
  - matplotlib https://matplotlib.org/stable/users/index.html
  - re https://docs.python.org/3/library/re.html
  - nltk https://www.nltk.org/api/nltk.html
  - wordcloud https://pypi.org/project/wordcloud/
  - stopwords https://pypi.org/project/stop-words/
  - tweepy https://docs.tweepy.org/en/stable/index.html
  - seaborn https://seaborn.pydata.org/tutorial.html

## 6. Dataset Creation

### Retrieving data from Twitter using Twitter API called Tweepy library available in Python.
Go to Dataset section in this repository to understand how the magic is happening.

### Dataset Description

<p align="center">
  <img src="https://user-images.githubusercontent.com/47279598/125612318-d00e9b7f-c496-45dc-b8ab-0f69af94282c.png"/>
</p>
<p align=center> 
Figure 2: Dataset First 5 rows
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/47279598/125612224-a53f85eb-d8b4-41e6-ba79-b65a0ae3e6c9.png"/>
</p>
<p align=center> 
Figure 3: Dataset Last 5 rows
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/47279598/125613655-56216733-5631-4cd2-b56a-b1cafcf2b1f9.png" />
</p>
<p align=center> 
Figure 4: Word Cloud of tweeted words
</p>

- The data set consist of 8,14,887 total tweets from all around India.
- The following figure 2 shows the first 5 rows of the dataset.
- The following figure 3 shows the last 5 rows of the dataset.
- The figure 4 represents most used words in tweets from complete dataset.
- From the following figures the dataset description is described as:
  - "S.No." depicting the number of tweet in incresing order
  - "Tweet Posted Time (UTC)" depicting the time of posting of that particular tweet.
  - "tweets" depicting textual content of that tweet.
  - "Tweet Location" depicting the location from which the tweet has been posted.
 
## 7. Generic Methodology
<p align="center">
  <img src="https://user-images.githubusercontent.com/47279598/125615027-53b9d0d2-4ab6-40b5-82fb-c371044d2a4d.png" />
</p>
<p align=center> 
Figure 5: Data Pipeline
</p>

- The following figure 5 represents sequential steps performed in order to reach to end goal.
- Firstly, the twitter data is scraped from Twitter using Twitter streaming API.
- Secondly, the dataset is curated and made in a csv format for each state.
- Thirdly, the tweets from the data is cleaned using basic nlp operations like:
  - converting text into lowercase
  - removing user mentions
  - removing re-tweets
  - removing special characters except [a-zA-Z]
  - removing hyperlink starts with https
  - removing punctuations 
  - removing stopwords
- After that, POS(Part-of-speech) tagging, also called grammatical tagging the process of marking up a word in a text (corpus) is applied on the data. 
- After that, Multimodal vectors are created using tuples of aspect category which stores aspect terms.
- After that, An algorithm is developed using NRC emotion lexicon and data from each states to create a Multimodal emotion scoring system using word count frequency.
- Lastly, the results of India state-wise emotion plots are analyzed using different visualization techniques such as bar plots, doughnut plots and bubble charts.


## 8. Results

### - 1. Analysis from bar plots:
- The emotion of population from different states of India is analyzed, and Maharashtra can be clearly seen at the top of every emotion score followed by NCT of Delhi and Karnataka. 
- These states were worst hit by the pandemic which led to a sudden and massive rise in corona virus cases. 
- These could be the reason for higher fear, anger ,disgust and sadness score in these states. 
- While at the same time they have also seen immense growth in the number of recovered patients that rises the level of trust and joy among the people. 
- This same trend is followed in other states like Tamil Nadu, West Bengal, Andhra Pradesh too.

### - 2. Analysis from doughnut plots:
- The people have mostly been very patient during the lockdown period and have contributed their bit to stop the spread chain of COVID-19.
- They have shown trust in the governmental policies and decisions as well as on their fellow citizens.
- Even after all this, due to the rapid spread of the virus, people have been quite fearful about catching infection.
- The rising death toll can be another cause of distress and sadness.
- Most people have been fearful and unsure about the outcomes of lockdown.
- Unemployment, working from home, falling economy and losing close ones has taken a toll on people’s emotional health.
- Despite all the shortcomings, people have been trying to look at the bright side of things.
- They have widely trusted the capabilities of teachers and schools to cope up with the changing education system.
- Reduction in pollution levels has been another cause of contentment amongst people.
- There has been a lot of anticipation regarding the final outcomes of lockdown and its impact on the economy.
- People have been looking forward to the governmental policies towards the unlocking procedure.

### - 3. Analysis from Bubble charts:

- Figure 7 depicts mode-wise emotion distribution during the lockdown period.
- COVID-19 has clearly, not just taken away jobs and the economy but has also affected people’s mental health adversely.
- Living away from family trapped in foreign lands, losing loved ones, and not attending their funerals, wearing masks every time you step out is not easy to adapt to.
- The new normal is definitely not normal for people.

## 9. Summary and Conclusion

- In this project, we present an emotion care scheme web-based platform to recognize the emotional state of Indian citizens throughout the ongoing COVID-19 crisis. 
- With the help of this research, health organizations and higher authorities will be able to have a better insight into the emotional health of people and will also be able to interpret the way people react to various day-to-day decisions.     


## 10. Limitations/ Challenges faced during the project

- The collection of the labeled dataset was a problem because of the unavailability of the properly labeled dataset.
- The proposed scheme currently works only on Twitter data. 
- The model is fully functional but it cannot be used for other languages.
- The number of emotions considered in this project are 8-scale emotions (Anger, Anticipation, Disgust, Fear, Joy, Sadness, Surprise, and Trust) only.

## 11. Future Scope

- The proposed scheme is scalable if data from different social media platforms is incorporated.
- The model is fully functional but its horizon can be widened by including different languages.
- The number of emotions considered can be increased to have an even more fine-grained analysis.
- Usage of deep learning approaches might also fine-tune the current scheme.
- To investigate new features to improve the existing model.

## 12. Credits: 
Thanking my project mentors and teammates for caring and supporting me wholeheartedly. The role you played in my life is invaluable. I’m grateful for all of your help and continued support.
<div class="align-text">
  <p>   
   <p text-align= "justify"> Mentor    : Dr. Vedika Gupta : https://www.linkedin.com/in/drvedikagupta/  </p>  
   <p text-align= "justify"> Team Mate : Adarsh Kumar     : https://www.linkedin.com/in/adarsh-kumar-5b1a1719b/ </p> 
  </p>
</div>

## 13. License: 
- Apache License 2.0
