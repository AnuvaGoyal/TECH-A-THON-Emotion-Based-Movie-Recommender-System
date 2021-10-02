# TECH-A-THON-Emotion-Based-Movie-Recommender-System
The purpose of the movie recommendation system is to search for content that would be interesting to an individual as per his/her current mood. It makes use of supervised machine learning algorithms to build a deep learning model that creates a customized list of movies that are relevant to an individual. This can be achieved through predictive modeling and heuristics with the data available.

## TABLE OF CONTENTS
|S.No.| Content |
|:--:|:--------------------:|
| 1. | Overview |
| 2. | Motivaton and Goal |
| 3. | About the Dataset |
| 4. | Installation|
| 5. | Tech/Framework Used |
| 6. | Component 1 Description|
| 7. | Component 2 Description|
| 8. | Project Workflow |
| 9. | Scope/ Improvement |

## OVERVIEW
The user will be given two options, either to enter his/her mood preference or to simply give a speech input and let the system decide the mood of the user. Thereafter, the system will then recommend the movies.
The project consists of two components:
Component 1: Speech Emotion Recognition System
Component 2: Movie Recommendation System

## MOTIVATION AND GOAL
The existing movie recommender systems (Netflix, Amazon Prime, 123movies, FMovies, etc.) work on browsing history of an individual, ratings of the movie, genres, popularity and trends. This project model will complement such systems by providing a new filter.

## ABOUT THE DATASET
We have used the RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song) dataset that contains 7356 files. It is one of the most common datasets used for this exercise because of its quality of speakers, recording and it has 24 actors of different genders. Here's the filename identifiers as per the official RAVDESS website:

>	Modality (01 = full-AV, 02 = video-only, 03 = audio-only).

>	Vocal channel (01 = speech, 02 = song).

>	Emotion (01 = neutral, 02 = calm, 03 = happy, 04 = sad, 05 = angry, 06 = fearful, 07 = disgust, 08 = surprised).

>	Emotional intensity (01 = normal, 02 = strong). NOTE: There is no strong intensity for the 'neutral' emotion.

>	Statement (01 = "Kids are talking by the door", 02 = "Dogs are sitting by the door").

>	Repetition (01 = 1st repetition, 02 = 2nd repetition).

>	Actor (01 to 24. Odd numbered actors are male, even numbered actors are female).

Here's an example of an audio filename. 02-01-06-01-02-01-12.mp4

## INSTALLATION

## TECH/FRAMEWORK USED


## COMPONENT 1
#### SPEECH EMOTION RECOGNITION
Speech Emotion Recognition (SER) is the task of recognizing the emotional aspects of speech irrespective of the semantic contents.

This component takes an audio input and recognises the emotion of the speaker. The steps involved are as follows:
##### 1. EXPLORATORY DATA ANALYSIS (EDA) OF THE DATASET
>The key features of the audio data are namely, MFCC (Mel Frequency Cepstral Coefficients), Mel Spectrogram and Chroma.
    
##### 2. DATA AUGMENTATION
>Data augmentation is the process by which we create new synthetic data samples by adding small perturbations on our initial training set.
>To generate syntactic data for audio, we can apply noise injection, shifting time, changing pitch and speed.
    
##### 3. FEATURE EXTRACTION
>The acoustic charac-teristics of the speech signal features such as pitch, energy, zero crossing rates, Mel Frequency Cepstral Coeﬃcients and Discrete Wavelet Transform        are extracted to analyze the signal .
     
##### 4. Data Preprocessing
>This involves splitting the dataset into training ans test set, encoding the categorical variables using OneHotEncoder and scaling the values using StandardScaler.
     
##### 4. MODEL BUILDING
>The model is trained using 1D CNN with three convolutional layers and one output layer and obtained an accuracy score oftest set

## COMPONENT 2
#### MOVIE RECOMMENDER SYSTEM
This component takes the emotion of the user predicted by the SER Model as input and recommends the latest movies accordingly.

##### Web Scraping
This process is done through Web Scraing the IMBb(Internet Movie Database) website. The dataframe given as output contains the names of the movies, their ratings and the corresponding links to visit the website for further information, classified according to the emotion.

## PROJECT WORKFLOW
<p align = "center"><img src = "https://user-images.githubusercontent.com/86526643/135710333-343d5b07-2446-41dc-a840-f310d7cbe74c.png"></p>

![workflow](https://user-images.githubusercontent.com/86526643/135710333-343d5b07-2446-41dc-a840-f310d7cbe74c.png)


## SCOPE/IMPROVEMENT
>The SER model can be improved to a better accuracy through training on a larger dataset.

>More emotions can be added to the Speech Emotion Recognizer Dataset.

>More features can be incorporated in the model through refining the dataset with more labels.

>Further the Movie Recommender System can be integrated with filters such as recommending the movies on the basis on emotion, gender and age rather than just emotion.

