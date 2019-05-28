## Classifying-Genres-to-Songs-Based-on-Lyrics

Classification in music is a field that is increasingly being researched. Music apps like Spotify and Apple Music classify songs by genre, artists and mood amongst other things, but they do it by using the audio of songs and comparing frequencies and different attributes in each genre. The task chosen for this project was to be able to classify a song based on just the lyrics of the song. This is a much harder classification as its hard to draw the difference between words of a particular genre. 

For the text retrieval, Bag-of-Words, TF-IDF and Word2Vec were used as models. These were tested with different classifiers to analyze how accurate the classification was.

...dataset

## Features
* Classify songs from their lyrics
* Four different type of classifiers for BOW and TFIDF: Multinomial Naive Bayes, Decision trees, Random Forest and Gradient boost
* Word2vec : XGBoost and Linear SVM


## Framework
Built with <a href="https://jupyter.org" target="_blank">Jupyter Notebook</a>.</h4>


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

## Files

The data set was taken from kaggle which consists of 380000+ song which was split into a train and test set and can be found in the repository.
In order to run the project only the jupyter notebook is needed.



