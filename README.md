
# AppGPS
Preliminary Sentimental Analysis of Apps Reviews Using NLP. 

![app_wordcloud.png](https://github.com/jomaweb/AppGPS/blob/main/AppGPS_Data/app_wordcloud.png)

## Content
- [Project Description](#project-description)
- [Questions](#hypotheses-questions)
- [Dataset](#dataset)
- [Model](#model)
- [Conclusion](#conclusion)
- [Resources](#links)
- [Credits](#credits)


## Project Description
There is a link between the possibility of uninstalling an app and the fact that users do not receive the expected performance of an app or do not understand how it works. A sentimental analysis of app review can be used to determine users' opinions about apps' performance, improvements, and shortcomings, as well as their acceptance (like or dislike). This project presents an approximation to identify needs, requirements, and opinions of app user, as well as a characterization of the community supporting the apps. This project will download (data mine) app reviews from Google Play. However, in order to keep track of the same conversation, we will concentrate on the feedback from the 50 most popular communication apps as of March 3rd, 2021, sorted by Most Relevant and Newest. This project aims to analyze **What people like and dislike about the Apps in the Google Play Store?**

The techniques applied are:
1. Data mining 
  * web scraping & google-play-api
2. Lexical dispersion plots (LDPs)
  * Lexical dispersion is an technique to  identify “how are the use of words (lexemes) dispersed throughout the existence of a corpus.” They show the density of word usage throughout over the course of the wordcount of a speech event (for literary/linguistics scholars) or time."
3. Natural Language Processing using Python
  * Analysis of users acceptance (polarity)
  * Analysis of lexemes with wordclouds
  * training a prediction model (RandonForestClassifier) that identify if a bulk of reviews contain positive or negative acceptance of the app.

## Questions
* What people like and dislike about the Apps in the Google Play Store?

* How reliable is the sentimental analysis of user reviews in identifying criteria, opinions, and acceptance of apps?

## Goals
1. Predict the acceptance (polarity) of apps regarding the reviews posted in Google Play Store.
2. Characterize the preliminary needs, requirements and opinions of app-users regarding the prominent words in the apps reviews.
3. Train a model to predict user acceptance of the apps.

## Dataset
* The Data set was acquired with data mining from the website of Google Play Store from USA (*Beautifulsoup* & *google-play-api*)
* The sample contains 45.609 reviews posted between 2013-2021 and selected as the *Most Relevant* and the *Newest*.
* The Distribution of the reviews in the sample is:
  * score 1: 8.659 
  * score 2: 7.561
  * score 3: 14.222
  * score 4: 7.449
  * score 5: 7.718
 
This data was intentional downloaded in this unbalanced relation. The aim was to achieve a *feature engineering* to define a target that contains three main values for ranking the reviews according to the following proportion:

* Positive: 15.167 (reviews with score 4 & 5)
* Neutral: 14.222 (reviews with score 3)
* Negative: 16.220 (reviews with score 1 & 2)
 
## Model
The data set was transformed using *nltk.WordNetLemmatizer* and *TfidfVectorizer*. <br>
The model trained was a *RandonForestClassifier* an it was tested throughout a *cross-validation* with a score of 72.3% (0.723) of prediction.  

## Conclusion
* Data do not tell about cultural, technological and demographic conditions.
* NLP analysis of reviews do not provided what exactly people like and dislike about an apps.
* NLP analysis of reviews is a relevant approach to:
  * identify the tendency of user acceptance,
  * compare user acceptance in in relation to others apps,
  * characterize the preliminary needs of user, 
  * characterize the community of users related to a particular product, such as the apps in Google Play Store.



## Resources
In this repository you can find the file of the final presentation, the data files (.csv), and the *jupyter notebooks* related to *web scraping*, *data cleaning*, *EDA & visualization* and *model training*. 
[Repository](https://github.com/jomaweb/Data_Excercises_IH/tree/main/AppGPS_Word_Analysis)<br>
[LinkedIn](https://www.linkedin.com/in/jose-ma/)

## Credits 
This project was submitted to graduate from the Bootcamp in *Data Analysis and Machine Learning* at IronHack Berlin, 2021* 
