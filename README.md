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
1. [Abstract](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19/blob/main/README.md#1-abstract) 
2. [Motivation](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#2-motivation)
3. [Problem Statement](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#3-problem-statement)
4. [Introduction](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#4-introduction)
5. [Requirements](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#5-requirements)
6. [Dataset Creation](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#6-dataset-creation)
7. [Generic Methodology](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#7-generic-methodology)
8. [Results](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#8-results)
9. [Summary and Conclusion](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#9-summary-and-conclusion)
10. [Limitations](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#10-limitations-challenges-faced-during-the-project)
11. [Future Scope](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#11-future-scope)
12. [Credits](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#12-credits)
13. [License](https://github.com/Piyush2912/Multi-modal-Emotion-Analysis-on-COVID-19#13-license)

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

## Dataset : https://github.com/Piyush2912/Twitter_dataset

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

### I. Analysis from bar plots:
  - The emotion of population from different states of India is analyzed, and Maharashtra can be clearly seen at the top of every emotion score followed by NCT of Delhi and Karnataka. 
  - These states were worst hit by the pandemic which led to a sudden and massive rise in corona virus cases. 
  - These could be the reason for higher fear, anger ,disgust and sadness score in these states. 
  - While at the same time they have also seen immense growth in the number of recovered patients that rises the level of trust and joy among the people. 
  - This same trend is followed in other states like Tamil Nadu, West Bengal, Andhra Pradesh too.
  - The Indian State-wise 8 Emotion (Anger, Anticipation, Disgust, Fear, Joy, Sadness, Surprise, and Trust) bar plots are as follows:

<p float="left">
  <img src="https://user-images.githubusercontent.com/47279598/125636352-eb814232-e6c9-45bf-a8c1-d61291a0d9aa.png" alt="India state-wise anger score" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125636359-6bacf62d-3889-4658-b981-93b459092f07.png" alt="India state-wise anticipation score" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125636361-6c253af8-e03b-482d-8667-b6369818265d.png" alt="India state-wise disgust score" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125636363-9e3ce057-7f3e-49d6-9267-5e4ae9f5059a.png" alt="India state-wise fear score" width="220"/>
</p>
<p float="left">
  <img src="https://user-images.githubusercontent.com/47279598/125636367-81b9be0c-d9e9-474a-87c1-b5b8d1f9f254.png" alt="India state-wise joy score" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125636370-7c64ea89-2ef8-480d-862b-7f5e8a376809.png" alt="India state-wise sadness score" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125636372-7318a350-178a-4da9-8e8d-acd45cbb6070.png" alt="India state-wise surprise score" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125636375-eb818bb0-c45f-46d6-a26c-274cfef9aed9.png" alt="India state-wise trust score" width="220"/>
</p>




### II. Analysis from doughnut plots:
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
  - The 6 Multimodal Emotion doughbut plots are as follows:

<p float="left">
  <img src="https://user-images.githubusercontent.com/47279598/125636867-8726f955-c0a7-4472-88ba-42b12b0976d1.png" alt="Education" width="300"/>
  <img src="https://user-images.githubusercontent.com/47279598/125636874-1c57f43a-5728-439c-b88d-68ba2a083aa0.png" alt="Health" width="300"/>
  <img src="https://user-images.githubusercontent.com/47279598/125636878-5c26a884-ba00-4a13-8614-d32310e9b78f.png" alt="Lockdown" width="300"/>
</p>
<p float="left">
  <img src="https://user-images.githubusercontent.com/47279598/125636882-75f22753-9992-479f-b15b-851c58c1751f.png" alt="Market" width="300"/>
  <img src="https://user-images.githubusercontent.com/47279598/125636883-4f020060-d8cf-475c-8e0f-cca38e193aa5.png" alt="Nature" width="300"/>
  <img src="https://user-images.githubusercontent.com/47279598/125636887-332996d7-f6dd-4ec4-b5af-13fe8b72b9de.png" alt="Politics" width="300"/>
</p>


### III. Analysis from Bubble charts:
  - Figure 7 depicts mode-wise emotion distribution during the lockdown period.
  - COVID-19 has clearly, not just taken away jobs and the economy but has also affected people’s mental health adversely.
  - Living away from family trapped in foreign lands, losing loved ones, and not attending their funerals, wearing masks every time you step out is not easy to adapt to.
  - The new normal is definitely not normal for people.
  - The Emotion intensity bubble plots pertaining to 6 modes are as follows:

<p float="left">
  <img src="https://user-images.githubusercontent.com/47279598/125637051-3f22939c-eeb7-47ae-be21-c4e2f8ebad69.png" alt="ANGER" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125637054-24f8bae6-7f6c-4ba3-91cc-10d9cd7dbff1.png" alt="ANTICIPATION" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125637055-e3f9e7a6-288d-4c83-95a6-c2fe5bf7a478.png" alt="DISGUST" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125637057-d08bc144-94d6-4b91-8bb0-d59217523020.png" alt="FEAR" width="220"/>
</p>

<p float="left">
  <img src="https://user-images.githubusercontent.com/47279598/125637060-cba06a90-0a04-4fe9-8214-748615f6cf8e.png" alt="JOY" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125637063-9ca10681-eba3-433b-9a1b-5695672fafec.png" alt="SADNESS" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125637065-f3f01de3-cc85-4ef4-846e-85d741fdb35f.png" alt="SURPRISE" width="220"/>
  <img src="https://user-images.githubusercontent.com/47279598/125637067-f046f0e1-ed8d-4eb5-a4f8-93acf20fb7c6.png" alt="TRUST" width="220"/>
</p>

## 9. Summary and Conclusion

- In this project, we present an emotion care scheme web-based platform to recognize the emotional state of Indian citizens throughout the ongoing COVID-19 crisis. 
- Taking India as a case study, we inferred from this textual analysis that ‘joy’ has been lesser towards everything (~9-15%) but nature (~17%) due to the apparent fact of lessened pollution. 
- The education system entailed more trust (~29%) due to teachers' fraternity's consistent efforts. 
- The health sector witnessed sadness (~16%) and fear (~18%) as the dominant emotions among the masses as human lives were at stake. 
- With the help of this research, health organizations and higher authorities will be able to have a better insight into the emotional health of people and will also be able to interpret the way people react to various day-to-day decisions.
- Additionally, the state-wise and emotion-wise depiction is also provided. 
- An interactive internet application has also been developed for the same.


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
   <p text-align= "justify"> Team Mate : Rohan Arora      : https://www.linkedin.com/in/rohanarora18/ </p> 
   <p text-align= "justify"> Team Mate : Shreya Dhingra   : https://www.linkedin.com/in/shreya-dhingra-927b19190 </p> 
  </p>
</div>

## 13. License: 
- Apache License 2.0
