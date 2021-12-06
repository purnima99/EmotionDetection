# UCS757-Emotion Detection in Audio Files (Speech & Songs)

Built deep learning model that detects 8 different kind of emotions - neutral, calm, happy, sad, angry, fearful, disgust and surprised in any user uploaded audio file.
Web Application developed using Django.

## Table of contents
* [Behind the Project](#Behind-the-Project)
* [Metrics](#metrics)
* [Methodology Flow Chart](#methodology-flow-chart)
* [I/O Screenshots](#inputoutput-screenshots)
* [Tools & Technologies Used](#technologies-and-tools)
* [Setup](#setup)
* [How to Use this Repo](#how-to-use-this-repo)
* [Status](#status)
* [Appendix](#appendix)

## Behind the Project

This project is a Django-REST API that uses a deep learning model interfacing using a simple front end. The model adopted in this work is an Emotion Classifier trained with audio files of the RAVDESS & TESS dataset links to which are in the Appendix.

This project presents a deep learning classifier able to predict the emotions of a human speaker encoded in an audio file. The classifier is trained using 2 different datasets, RAVDESS and TESS, and has an overall F1 score of 80% on 8 classes (neutral, calm, happy, sad, angry, fearful, disgust and surprised).

Feature set information -

For this task, the dataset is built using 5252 samples from:
* the Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS) dataset
* the Toronto emotional speech set (TESS) dataset

The samples include:
1440 speech files and 1012 Song files from RAVDESS. This dataset includes recordings of 24 professional actors (12 female, 12 male), vocalizing two lexically-matched statements in a neutral North American accent. Speech includes calm, happy, sad, angry, fearful, surprise, and disgust expressions, and song contains calm, happy, sad, angry, and fearful emotions. Each file was rated 10 times on emotional validity, intensity, and genuineness. Ratings were provided by 247 individuals who were characteristic of untrained adult research participants from North America. A further set of 72 participants provided test-retest data. High levels of emotional validity, interrater reliability, and test-retest intrarater reliability were reported.

2800 files from TESS. A set of 200 target words were spoken in the carrier phrase "Say the word _____' by two actresses (aged 26 and 64 years) and recordings were made of the set portraying each of seven emotions (anger, disgust, fear, happiness, pleasant surprise, sadness, and neutral). There are 2800 stimuli in total. Two actresses were recruited from the Toronto area. Both actresses speak English as their first language, are university educated, and have musical training. Audiometric testing indicated that both actresses have thresholds within the normal range.

The classes the model wants to predict are as follows: (0 = neutral, 1 = calm, 2 = happy, 3 = sad, 4 = angry, 5 = fearful, 6 = disgust, 7 = surprised). This dataset is skewed as there is not a calm class in TESS, hence there are less data for that particular class and this is evident when observing the classification report.

**Prediction Accuracy of 0.80** 

More information on datasets in the appendix.

## Metrics 

*Model summary*

![Link to model](https://github.com/purnima99/UCS757-EmotionDetection/media/model.png) 

*Loss and accuracy plots*

![Link to loss](https://github.com/purnima99/UCS757-EmotionDetection/media/loss.png) 

![Link to accuracy](https://github.com/purnima99/UCS757-EmotionDetection/media/accuracy.png)

*Classification report*

![Link to classification report](https://github.com/purnima99/UCS757-EmotionDetection/media/ClassificationReport.png)

*Confusion matrix*

![Link to classification report](https://github.com/purnima99/UCS757-EmotionDetection/media/ConfusionMatrix.png)

## Methodology Flow Chart

![Link to flow chart](./flow_chart.png)

## Input/Output Screenshots
![Alt Text](./i-o/01.png)

## Technologies and Tools
* Python 3.x 
* TensorFlow
* Keras
* OpenCV
* h5py

## Setup

* Use the command prompt to setup a virtual environment.
* Install all dependencies and requirements using the following command - 

`python -m pip install -r requirements.txt`

This will install all libraries required for the project.

## How to Use this Repo 

### Run via the Django App
* Clone the repo by running - 

    `git clone https://github.com/purnima99/UCS757-EmotionDetection.git`

* Run the manage.py file - 
    
    `python manage.py runserver`

## Status    
Project Status: Completed 
