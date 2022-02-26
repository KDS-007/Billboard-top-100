# Predicting-Billboard-Hits-Using-Spotify-Data-DS3-200721
The Billboard Hot 100 Chart1 remains one of the definitive ways to measure the success of a popular song. We investigated using machine learning techniques to predict which songs will become Billboard Hot 100 Hits.

# Predicting Billboard Hits Using Spotify Data 
## Dataset used: songs_complete_data.csv

# Exploratory Data Analysis
The dataset included songs from the year 1980 - 2020

![image](https://user-images.githubusercontent.com/65284408/129548170-52f94d0b-5cca-45c8-992c-869bd82da73f.png)

Trends of different audio features changes over the decades
![image](https://user-images.githubusercontent.com/65284408/129549616-cdfb9438-46a2-4c4e-81b4-ef091ead08f8.png)
![image](https://user-images.githubusercontent.com/65284408/129549734-89c518b4-b76e-4959-8756-245559932789.png)
![image](https://user-images.githubusercontent.com/65284408/129549801-8604862c-bce7-45e0-86e2-7997b664cbe2.png)

The distribution of Acousticness w.r.t Danceability and Loudness
![image](https://user-images.githubusercontent.com/65284408/129549969-0f34d284-ab5d-4475-9cac-0590a08b67ee.png)
![image](https://user-images.githubusercontent.com/65284408/129550187-7606e001-0940-49ec-ae1d-77eb28d01ef1.png)

# Preprocessing
  1. Filtering songs with same title but different Artist and dropping duplicate row containing same independent features but different dependent feature
  2. Dropping columns which are not requires (unnamed: 0,URI,Lyrics,Title,Artist)
  3. Removal of outliers from release year col
  4. Label encoding for categorical features
  5. Transfor features to a normal distrbution
  6. SMOTE to balance the data
  7. Standard Scaler used to standardize the data


# Model Training

Model used: Decision Tree Classifier, Ada Boost Classifier

Problem: To predict if a song will be a billboard top100 hit



### Dataset
![data](https://user-images.githubusercontent.com/65284408/129482910-0baa3325-26c3-4b02-9e39-64f4c3f5bc36.PNG)
- Independent Features Selected
  1. Danceability	
  2. Energy	
  3. Loudness	
  4. Speechiness	
  5. Acousticness	
  6. Mode
  7. Insturmentalness
  8. Liveness	
  9. Valence	
  10. Tempo	
  11. Genre	

- Label
  1. Top100  

  
#
## Models
### Decision Tree Classifier
### accuracy:76%
![auc](https://user-images.githubusercontent.com/65284408/129483092-1962e2d6-d1ee-48af-b62f-6ab36935a48a.PNG)
![report](https://user-images.githubusercontent.com/65284408/129483099-c9633f70-4de5-47bf-915e-c2d2668a7aac.PNG)
#### confusion matrix
![cm](https://user-images.githubusercontent.com/65284408/129483104-7850046a-c4d2-48b5-8e8f-dd5b14602b93.PNG)
# 
### Ada Boost with base model Decision tree Classifier
### accuracy:87%
![auc](https://user-images.githubusercontent.com/65284408/129483049-59a73dd9-dddb-4644-97f2-d2cb7ae41973.PNG)
![report](https://user-images.githubusercontent.com/65284408/129483057-06bf9c1a-d42c-4dc1-88de-47989da81405.PNG)
#### confusion matrix
![cm](https://user-images.githubusercontent.com/65284408/129483068-14cb32ef-8a32-453f-b914-2a0ded01921a.PNG)
#
### LDA
### accuracy:65%
![auc](https://user-images.githubusercontent.com/65284408/129482989-73280453-a890-4dcf-83c8-0b1008e0189b.PNG)
![report](https://user-images.githubusercontent.com/65284408/129483006-7710ca02-267c-4e9f-bc9f-87642ed582ac.PNG)
#### confusion matrix
![cm](https://user-images.githubusercontent.com/65284408/129483019-a3f4db59-68c5-4fdc-86f5-7b7e55c4a39b.PNG)

# Deployment
## Deployed the model on heroku using flask framework

### Screenshots
![image](https://user-images.githubusercontent.com/65284408/129594547-4f3d5216-2c8f-4905-b448-5a6b8ee4b7a8.png)
![image](https://user-images.githubusercontent.com/65284408/129594847-6f98b68b-6c5b-49df-bf7b-9f8cb0ba5d58.png)
![image](https://user-images.githubusercontent.com/65284408/129594938-fe97cbdd-4a70-4912-9be1-11c387281a9e.png)
