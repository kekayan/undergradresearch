# FYP: Stack Overflow Auto Tagging Using Transformers (BERT)


## Work Flow

###  Data Preparation 

*  Data can be downloaded from [Kaggle](https://www.kaggle.com/stackoverflow/stacksample)
* Data contains two zip files Questions & Tags
* Dropped questions which have upvotes lesser than five.
* Grouped Tags and merged with questions
* Analyze Tags & find out most frequent tags (top 5)
* filter the data according to it

### Preprocess

* Lower case both body and title
* Remove codes , Preformatted text, HTML
* Remove Special Characters , Punctuations
* Remove accented characters
* Expanded contractions
* Remove trialing Space
* [DATA for BERT](https://drive.google.com/file/d/1tDyUnssfZw8Ptsh80CqbsaUIgdgMB1Mk/view?usp=sharing)
* TF_IDF: Lemmatize
* TF_IDF: Stop Words Removal
* [DATA for TF IDF ](https://drive.google.com/file/d/1-0Gd9kUVKmmajMU98vx8gFX_yfEZA8C8/view?usp=sharing)

### TF IDF Baseline

* TfidfVectorize BODY & TITLE
* MultiLabelBinarize [Y](https://drive.google.com/file/d/1-J1_7Ic91zwNN7WNAfOzwKGqM5Bw0o8r/view?usp=sharing)
* Iterative starify train test split
* Binary Relavance Transformation
* Naive Bayes Classifier
* macro F1 & AUC to evaluate

### BERT for SOTA

* BERT Embeddings for [Body](https://drive.google.com/file/d/1-A2UgqshVkTgjNI-4jLdFfkOUyk_pz3q/view?usp=sharing) & [Title](https://drive.google.com/file/d/1-BjJu0UbIaDxQ_WOAxrDky0MPw1chEZq/view?usp=sharing)
* MultiLabelBinarize [Y](https://drive.google.com/file/d/1-J1_7Ic91zwNN7WNAfOzwKGqM5Bw0o8r/view?usp=sharing)
* NN for classifier
* macro F1 & AUC to evaluate


