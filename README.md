# Political German Word Embeddings

German word embeddings computed from a corpus of parliamentary transcripts (2017-2019). 

## Methodology 

A detailed description can be found [on Medium](https://medium.com/@martina.schories/using-word-embeddings-as-a-method-for-journalistic-research-ae82ffea7a62). This is a corpus centered approach, the models are trained to analyse language change of plenery sittings.

## Algorithm

Implementation of word2vec skip-gram with [gensim](https://radimrehurek.com/gensim/models/word2vec.html)

## Parameters

* `size = 300`: Dimensionality of the word vectors
* `window = 5`: Maximum distance between the current and predicted word within a sentence
* `sg = 1`: Training algorithm: 1 for skip-gram; otherwise CBOW
* `hs = 0`: If 1, hierarchical softmax will be used for model training. If 0, and negative is non-zero, negative sampling will be used
* `negative = 5`: If > 0, negative sampling will be used, the int for negative specifies how many “noise words” should be drawn (usually between 5-20)
* `iter = 5`: Number of iterations (epochs) over the corpus
* `min_count = 2`:Ignores all words with total frequency lower than this
* `workers = 4`: Use these many worker threads to train the model

## Corpus and Preprocessing

The German parliament Bundestag [publishes](https://www.bundestag.de/services/opendata) the documents for all 19 legislative periods as machine-readable XML files. The lemmatizing was implemented with the software [TreeTagger](https://www.cis.uni-muenchen.de/~schmid/tools/TreeTagger/) written by Helmut Schmid from the Ludwig Maximilian University of Munich. Further preprocessing steps were sentence segmentation and the removal of hidden control characters.

Some words, such as "migrants" were not recognized by the lemmatizer. In cases like this, we converted the words back and made "migrants" into "migrant" so that it would fit with the other data. 

## Models

I provide 30 models of transcripts of the current electoral term. Why more than one? Because word embeddings are unstable, read more about it [on Medium](https://medium.com/@martina.schories/using-word-embeddings-as-a-method-for-journalistic-research-ae82ffea7a62). The models are saved as a KeyedVectors instance, so you can start right away with various syntactic/semantic NLP word tasks.

* [wp-19-iter-1.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-1.w2v.zip)
* [wp-19-iter-2.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-2.w2v.zip)
* [wp-19-iter-3.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-3.w2v.zip)
* [wp-19-iter-4.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-4.w2v.zip)
* [wp-19-iter-5.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-5.w2v.zip)
* [wp-19-iter-6.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-6.w2v.zip)
* [wp-19-iter-7.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-7.w2v.zip)
* [wp-19-iter-8.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-8.w2v.zip)
* [wp-19-iter-9.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-9.w2v.zip)
* [wp-19-iter-10.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-10.w2v.zip)
* [wp-19-iter-11.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-11.w2v.zip)
* [wp-19-iter-12.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-12.w2v.zip)
* [wp-19-iter-13.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-13.w2v.zip)
* [wp-19-iter-14.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-14.w2v.zip)
* [wp-19-iter-15.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-15.w2v.zip)
* [wp-19-iter-16.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-16.w2v.zip)
* [wp-19-iter-17.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-17.w2v.zip)
* [wp-19-iter-18.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-18.w2v.zip)
* [wp-19-iter-19.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-19.w2v.zip)
* [wp-19-iter-20.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-20.w2v.zip)
* [wp-19-iter-21.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-21.w2v.zip)
* [wp-19-iter-22.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-22.w2v.zip)
* [wp-19-iter-23.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-23.w2v.zip)
* [wp-19-iter-24.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-24.w2v.zip)
* [wp-19-iter-25.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-25.w2v.zip)
* [wp-19-iter-26.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-26.w2v.zip)
* [wp-19-iter-27.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-27.w2v.zip)
* [wp-19-iter-28.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-28.w2v.zip)
* [wp-19-iter-29.w2v.zip](https://gfx.sueddeutsche.de/data/politicalGermanWordEmbeddings/wp-19-iter-29.w2v.zip)

## Published stories (in German)
* How the German Bundestag was messing up climate change: https://projekte.sueddeutsche.de/artikel/politik/wie-der-bundestag-ueber-klimapolitik-spricht-e704090/

* The rushed parliament: The so-called refugee crisis was a turning point, Germany has changed. This data research shows: The discourse on refugees and migration has shifted to the right  -  also by the AfD https://projekte.sueddeutsche.de/artikel/politik/bundestag-das-gehetzte-parlament-e953507/

* "In the engine room of language": A text about the methodology with the ambition is to explain the topic of machine learning without taking refuge in a "it's a black box" https://projekte.sueddeutsche.de/artikel/politik/so-haben-wir-den-bundestag-ausgerechnet-e893391/
