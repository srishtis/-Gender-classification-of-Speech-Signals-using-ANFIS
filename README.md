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
1. Database 1- NOIZEUS (University Of Texas, Dallas): Word extracted- ‘the’
2. Database 2- American English Database (International Telecommunication Union): Word extracted- ‘the’
3. Database 3- Modified TIMIT Database (Prof. Dan Ellis, Electrical Engineering, Columbia University): Words extracted- ‘cottage’, ‘cheese’, ‘chives’, ‘delicious’

and finally...
4. Database (for the final submission): Modified TIMIT database (derived from TIDIGITS): Words uttered: ‘oh’, ‘zero’, ‘two’, ‘three’, ‘four’, ‘five’, ‘six’, ‘seven’, ‘eight’, ‘nine’

While we used the words from these datasets, we also got some of our friends, peers and acquaintances to enunciate the same words. This data creation and collection exercise not only helped us increase the volume of data to work with but also introduced us to the actual process of industry-grade problem solving and even theoretical research. 

### Methodology
The methodology can be summarized succinctly in the following steps:
1. Data Preprocessing and Cleaning
2. Feature Extraction: Pitch, Zero Crossing Rate, Short-time energy, Energy Entropy, Formants
3. Building and reiterating various models: ANFIS (both with 1 feature i.e. pitch and multiple features), ANN and SVMs

A diagramatic representation of the process is as follows:
![Process Summary]
(/process_summary.jpg)

### Results
METHOD USED | EFFICIENCY OBTAINED
------------ | -------------
ANN (Multi-Feature) | 90.00 %
SVM (Multi-Feature) | 90.00 %
ANFIS (using only Pitch as a feature) | 95.00 %
ANFIS (Multi-Feature) | 100.00 %

Following were the __takeaways from the result__:
_1. The pitch of the female speakers is significantly higher than the male speakers._

_2. The normalized zero crossing rate values are also higher for the female speakers than the male speakers._

_3. The normalized short-time energy values are slightly higher for the female speakers than the male speakers._

_4. The normalized energy entropy values are also in general slightly higher for the female speakers than the male speakers._

_5. The first formant frequencies are higher for the female speakers when compared to male speakers._

_6. The Neural Network and Support Vector Machine classifiers have an efficiency of 90.00% in the multi-feature format._

_7. The ANFIS network using only Pitch as a feature has an efficiency of 95.00%, showing improvement over the standard methods._

_8. The multi-feature ANFIS gives an efficiency of 100.00% for the given dataset, hence rectifying the error arising from the exceptional case when using only Pitch as a discriminating factor._
