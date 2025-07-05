🌍 NLP with Disaster Tweets
This project aims to classify tweets as real disaster-related or not using various Natural Language Processing (NLP) techniques. It explores traditional and modern text representation methods—Bag of Words, Word Embeddings (Word2Vec & GloVe), and Transformer-based models (BERT)—with multiple classifiers.

📌 Problem Statement
The goal is to build a binary classifier that can predict whether a tweet is about a real disaster or not. The dataset was originally provided on Kaggle.

🛠️ Techniques Used
✨ Preprocessing
Lowercasing, punctuation & emoji removal

Acronym and contraction expansion

Stopword removal, lemmatization, stemming

POS tagging to retain meaningful words

🧠 Models Compared
Bag of Words + ML classifiers: Logistic Regression, SVM, Random Forest, XGBoost, etc.

GloVe embeddings: 100D vectors (glove-wiki-gigaword-100)

Word2Vec embeddings: Trained from scratch using Gensim on cleaned tweets

Transformers: Fine-tuned DistilBERT model using HuggingFace Trainer API

📊 Evaluation
Models were evaluated using F1-score with stratified k-fold cross-validation. Transformer models achieved the best performance, followed by Word2Vec.

Model Type	Best Classifier	F1-Score
Bag of Words	SVM (RBF kernel)	~0.74
Word2Vec (Custom)	SVM (RBF kernel)	~0.78
GloVe (Pretrained)	Logistic Regression	~0.76
Transformers (BERT)	Fine-tuned DistilBERT	~0.81

📁 Files
Disaster_Tweet_Classifier.ipynb: Full notebook with preprocessing, modeling, and evaluation

submission.csv: Final predictions on test data

🧾 Acknowledgements
Kaggle competition

HuggingFace Transformers

Gensim Word2Vec

