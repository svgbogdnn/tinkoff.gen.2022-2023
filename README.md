# tinkoff
### solution to  6ix selection task for [Tinkoff gen](https://fintech.tinkoff.ru/school/generation/)

Description of the ```Doc2VecLM``` model: </br>

My(our) major target is to showcase how synergy between Word2Vec, TF-IDF, and linear classifiers can yield an effective text generation pipeline, ensuring flexibility and accuracy for various NLP tasks.

The model is a hybrid of Word2Vec (Skipgram), TF-IDF and a linear classifier.

Description of ```Doc2VecLM``` model:
1) ```Word2VecWrapper``` returns embeddings for each word in the input sequence.
2) ```TFIDFWrapper``` returns tfidf score of each word in the input sequence.
3) ```Word2VecWrapper``` embeddings are multiplied by ```TFIDFWrapper``` scores and averaged, which represents the overall context of the sentence.
4) ```Classifier``` takes as input the context embedding and ```last_n``` embeddings of the last words and returns the probabilities of the next word.

Train the model:

```
bash train.sh
```

Generate text:
```
bash generate.sh
```
