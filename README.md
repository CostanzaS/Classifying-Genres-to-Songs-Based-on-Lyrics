## Classifying-Genres-to-Songs-Based-on-Lyrics

Classification in music is a field that is increasingly being researched. Music apps like Spotify and Apple Music classify songs by genre, artists and mood amongst other things, but they do it by using the audio of songs and comparing frequencies and different attributes in each genre. The task chosen for this project was to be able to classify a song based on just the lyrics of the song. This is a much harder classification as its hard to draw the difference between words of a particular genre. 

For the text retrieval, Bag-of-Words, TF-IDF and Word2Vec were used as models. These were tested with different classifiers to analyze how accurate the classification was.


## Features
* Classify songs from their lyrics
* Four different type of classifiers for BOW and TFIDF: Multinomial Naive Bayes, Decision trees, Random Forest and Gradient boost
* Word2vec : XGBoost and Linear SVM


## Framework
Our framework was <a href="https://jupyter.org" target="_blank">Jupyter Notebook</a>.</h4>


## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install:
* numpy
* pandas
* seaborn
* matplotlib.pyplot
* re
* sklearn
* nltk
* gensim

```bash
pip install numpy
pip install pandas
pip install seaborn
pip install matplotlib.pyplot
pip install re
pip install sklearn
pip install nltk
pip install gensim
```

## Dataset

The data set was taken from [Kaggle](https://www.kaggle.com/gyani95/380000-lyrics-from-metrolyrics) which consists of 380000+ song which was split into a train and test set.
In order to run the project only the jupyter notebook is needed.

**Content**
The dataset initially consisted of 6 columns:

* ID
* Song
* Artist
* Year
* Genre
* Lyrics

However, Index, Artist and Year were dropped as they were not relevant to our classification.

![dataset](https://github.com/CostanzaS/Classifying-Genres-to-Songs-Based-on-Lyrics/blob/master/pictures/Schermata%202019-05-28%20alle%201.47.08%20AM.png)

Genres with less occurence such as "Electronic", ”Folk”, ”Indie”, ”Not Available”, ”Other”and ”R&B” were dropped as they were not significant. However, after running some tests, we also decided to drop ”Rock” as it is so dominant in thedataset.

## Accuracy (full dataset)

| Classifier          | BOW      | TFIDF |
|-------------------:|:--------:|:------|
| Decision trees     | 76.5%    | 76.2% |
| Multinomial NB     | 58.7%    | 56.5% |
| Random Forest      | 76.8%    | 76.8% | 
| Gradient Boosting  | 61.0%    | 61.5% |

## Accuracy (full dataset)

| Classifier       | Word2Vec |
|----------------:|:--------:|
| XGBoost         | 60.3%    | 
| Linear SVM      | 59.4%    | 

## General Findings

![TFIDF with RF](https://github.com/CostanzaS/Classifying-Genres-to-Songs-Based-on-Lyrics/blob/master/RandomForestTfidf_full.png)
![BOW with RF](https://github.com/CostanzaS/Classifying-Genres-to-Songs-Based-on-Lyrics/blob/master/BOW_RF.png)

## Conclusion

Firstly, we realized that adding Rock to our dataset was making it biased. Therefore, we removed it to get higher accuracies.
Secondly, from the confusion matrices we could see that although it was still trying to classify most songs for Pop, as this was now the highest occurring genre, it also did quite well with others. Genres such as Hip-Hop and Country were classified correctly many times as well. This is due to the similar style in Hip-Hop and the repeated chorus style in Country. 
It can also be seen that in a way the model does not work that bad as it accurately classifies some of the less represented genres well too. This is already better than humans who also have a hard time classifying these songs based on just the lyrics.
Therefore, all models performed quite well depending on the classifiers used and the best classifier to use is the Random Forest Classifier.

## Credits
* Costanza Siani
* Sarah Waseem
