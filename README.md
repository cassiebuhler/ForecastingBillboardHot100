# Using Audio Features To Predict The Top Songs in Billboard Hot 100

***Note: This is an old project from Spring 2021 when I took DSCI 521 (Data Analysis and Interpretation).***

### Project Description
Given audio features from the songs on the Billboard Hot 100 chart for 2010-2020, I use shallow neural networks to predict which songs will be in the top 10. Then, I investigate which features yield the best model by implementing ExtraTreesClassifier, LASSO, and SVM. The neural networks with the best acccuracy are given from features selected by SVM and ExtraTreesClassifier. 

Songs are collected using a [Billboard API](https://github.com/guoguo12/billboard-charts) and audio features are collected using a [Spotify API](https://tekore.readthedocs.io/en/stable/). 

I have provided the data, however, if you'd like to use the 01-dataCollection script, you need to get access tokens from Spotify API. To do so, follow 
<a href="https://developer.spotify.com/documentation/web-api/tutorials/getting-started" target="_blank" rel="noopener noreferrer">these instructions.</a> 

---

### Contents: 
#### Code
- **01-dataCollection.ipynb:** Collects the data from the Billboard package and Spotify API
- **02-dataExploration.ipynb:** Visualizes and explores data 
- **03-dataAnalysis.ipynb:** Generates neural networks and feature selection with data

#### Data
- **Data/BillboardData2.csv:** Dataset given from 01-dataCollection.ipynb.
  - There are 4 entries with a blank genre column, so they are dropped in the analysis phase. 
  - Overall there are 16 audio features for nearly 1100 songs. 

#### Other
- **Figures:** Folder containing the figures used in the presentation
- **FinalPresentaiton.pdf:** The slide deck used in the presentation recording 

---

### How to Use:
The code is divided into 3 files. Each of the 3 python files are separate form one another so you do not need to run them in a particular order. Since the data is already provided in the data folder, you do not need to run dataCollection.ipynb to run the other 2 files. 

To look at the data visualization, you can run dataExploration.ipynb. 

To look at the neural networks and feature analysis, dataAnalysis.ipynb contains all the code for this. 

---

### Challenges: 

1. Data availability. I wanted to get additional features regarding the demographics of the artists, but this was not available on Spotify API nor could I find a database where I could get this data from. In addition, I also wanted to obtain sales or streams for each song, but again, was not able to get this. The features I used for the project are a bit limited, which I feel hindered the model predictive ability. 

2. Spotify API could only scrape multiple songs at once if they were in the same playlist or in the same album. I overcame this by creating 11 playlists on my personal Spotify account where I manually added all 1100 songs to the playlists. 


--- 

### Contact 

Author: Cassie Buhler

Email: cb3452@drexel.edu
