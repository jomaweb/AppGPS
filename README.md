# AppGPS
Preliminary Apps Analysis Using NLP to characterize the preliminary needs of app-users and to predict the acceptance (polarity) of app-reviews posted in Google Play Store.


## Content
- [Project Description](#project-description)
- [Questions](#hypotheses-questions)
- [Dataset](#dataset)
- [Model](#model)
- [Conclusion](#conclusion)
- [Resources](#links)
- [Credits](#credits)


## Project Description
This project aims to analyze **What people like and dislike about the Apps in the Google Play Store?** In this regard this project deals with the analysis of reviews from the Google Play Store that belong to the category communication. The techniques applied are:
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

* To what extent the analysis of user reviews is accurate to identify requirements, opinions and their acceptance of the apps?

## Goals
1. Train a model to predict user acceptance of the apps
2. Visualize common words, Requirements and opinions to characterize the needs of apps-users

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
In this repository you can find the file of the final presentation, the data files (.csv), and the *jupyter notebooks* related to *web scraping* and *model training*. For the *jupyter notebook* with the *data cleaning* and *data visualizations*, please fell free to contact me via LinkedIn.  
[Repository](https://github.com/jomaweb/Data_Excercises_IH/tree/main/AppGPS_Word_Analysis)<br>
[LinkedIn](https://www.linkedin.com/in/jose-ma/)

## Credits 
This project was submitted to graduate from the Bootcamp in *Data Analysis and Machine Learning* at IronHack Berlin, 2021* 
