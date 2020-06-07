# Spam-Filter
This is a project in which we have worked upon the data from [UCI collections](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwi-x-_bge_pAhWaXSsKHfRMACkQFjACegQIAxAB&url=https%3A%2F%2Farchive.ics.uci.edu%2Fml%2Fdatasets%2FSMS%2BSpam%2BCollection&usg=AOvVaw3scsW50LOCjz32-tGbXe00)
This project is based upon *Natural Language Processing* and I have used the ```nltk``` library for some preprocessing and basic feature engineering.
### Steps involved are:
- Carry out some preprocessing on data as:
  - Remove all punctuarions from data , for which I used ```string.punctutation``` list.
  - Remove all common words, otherwise called as **stopwords** using ```nltk.corpus.stopwords``` library.
- Create a bag of words which is a matrix representing *every word in corpus* v/s *count of word in a line*
- Fir the *bag of words* to TfidfTransformer from ```scikit_learn``` library
  - Here TF is the Term Frequncy (Self Explanatory)
  - IDF is the Inverse Document Frequency, that means, more frequent words are given lower weightage upon value
- Create a Tfidf model that would identify the label for a particular message.
___
## Pipeline
**This process could be performed using pipeline feature of scikit learn as has been shown later in the notebook**
The pipeline simply contains all the steps we performed in form of tuples and it performs them for us
___
**Note:** I have made the model upon naive_bayes classifier, but any suitable classifier could be used.
