# Gender Classification of Speech Signals using ANFIS

This was my final semester project during my undergrad studies in B.Tech (Electronics and Communication engg.), class of 2015 at Manipal Institute of Technology.

## Historical context of the pursuit of the project
This project was my first experience with data engineering, wrangling and ultimately artificial neural networks. In my final semester (starting January, 2015), we were supposed to either get industrial experience as an internship or complete a thesis or project under the guidance of the faculty members. I paired up with another batchmate of mine, Neha Rawat to bring the project to fruition.

### Inspiration behind the project
We took inspiration from the IEEE paper: [Automated pitch-based gender recognition using an adaptive neuro-fuzzy inference system] (https://ieeexplore.ieee.org/document/6526879)
While the given paper identified the gender of the speaker using the pitch of the voice sample, we extracted 4 other features:

1. Formants
2. Short-Time Energy
3. Energy Entropy
4. Zero Crossing Rate

As stated in out project report, the motivation of the project was as follows:
_The motivation for this project is to use a multi-feature classification system involving the frequency as well as the energy based features. 
The use of a multi-feature based system is expected to give a more accurate classification as even if there is an aberration in the case of pitch or formants, it can be nullified by the values of the energy-based features. This would then provide a balanced and flexible estimate for comparison between the speakers._

## Aim of the project
As mentioned in our project report, Neha and I defined the following objective for oyr final semester project:

_Our primary objective is to design an efficient neuro-fuzzy based classifier for gender-based speaker classification using frequency as well as energy based features.
Our secondary objective is to analyze the features extracted and first observe the rough distinction apparent through just the values. Also, we will analyze the methodologies and tools used for feature extraction and the changes observed on modifying them if required._

## Brief on Datasets, Methodology and Results

### Data Gathering
We used the following datasets to start building our model:

While we used the words from these datasets, we also got some of our friends, peers and acquaintances to enunciate the same words. This data creation and collection exercise not only helped us increase the volume of data to work with but also introduced us to the actual process of industry-grade problem solving and even theoretical research. 

### Methodology
The methodology can be summarized succinctly in the following steps:
1. Data Preprocessing and Cleaning
2. Feature Extraction: Pitch, Zero Crossing Rate, Short-time energy, Energy Entropy, Formants
3. Building and reiterating various models: ANFIS (both with 1 feature i.e. pitch and multiple features), ANN and SVMs

A diagramatic representation of the process is as follows:

