
# Enhance

## About

Enhance aims to resolve the subject of mental issues among individuals by offering a secure, anonymous environment. Any person can freely discuss his/her problem with other individuals suffering from the same issue with qualified counsellors who can provide solutions to their problems. 

The platform discusses the topic of identification of internet harassment and related question matching. The principle purpose of this platform is to increase positive mental development among individuals as well as to show ways of identifying harassment and question similarities.

## Technology Stack

1. Web Application developed using React.js
2. Mobile Application developed using Flutter
3. Backend developed using Node.js/Express
4. ML Backend developed using Flask
5. User authentication using Passport.js
6. Data stored in cloud via MongoDB Atlas

## ML Algorithms

### Abuse Detection Algorithm

This section discusses the dataset used for online abuse detection, data preprocessing and the algorithm used for the classification of the sentence into different classes.

We made use of a [Twitter sentences dataset](https://github.com/t-davidson/hate-speech-and-offensivelanguage/tree/master/data/) that consists of 24,802 labelled tweets, in which each tweet was voted by a certain number of individuals and classified into three categories: "Hate speech", "Offensive Language" and "Neither". After preprocessing the data and removing undesirable words, punctuations, numbers, and emoticons various classification algorithms were executed on the data. 

Logistic regression was selected as the primary classification algorithm to conduct the analysis. To improve the model, a Grid search combined with K-fold cross-validation was performed. The dataset was then trained and tested on a 90-10 train-test split. Before fitting it into the logistic regression model, data preprocessing steps were carried out.

The best performing model had an overall precision of 0.87, recall of 0.83, and F1 score of 0.83. _The accuracy of the model was around 82%._ 

### Semantic Similarity Algorithm

This section discusses the dataset used for semantic similarity, data preprocessing and the algorithm used for the comparison of sentences.

We used a BERT model and data from the [Stanford Natural Language Inference](https://github.com/MohamadMerchant/SNLI/) corpus to predict semantic similarity with transformers. The BERT model takes two sentences as input and provides a similarity score between them and categorizes them into various classes. For training the model, 100,000 sample sentences were used. As for training and validation purposes, 10,000 sentences were used. The sentences are classified into three separate groups in the dataset: Contradiction, Entailment, and Neutral and are assigned similarity scores based on one of these categories.

In our model, we first loaded and preprocessed the data that generated a data generator. In this data generator, we performed tokenization and the procedure of Masked LM. We then built the model and carried out training and tested it against the validation data. One of the most crucial steps of the model, fine-tuning, was executed with a low learning rate. This step helped improve the pre-trained features of the new data. After fine-tuning, we once again retrained the model and then evaluated the model on the test data. _The model accuracy is around 79%_.

## Developers

-  Adnan Hakim [github.com/adnanhakim](https://github.com/adnanhakim)
   -  UI Designing, React.js Web Application and Node.js Backend
 
-  Arsh Shaikh [github.com/arshshaikh06](https://github.com/arshshaikh06)
   -  UI Designing and Flutter Mobile Application
 
-  Hussain Sadriwala [github.com/hussainf46](https://github.com/hussainf46)
   -  Abuse Detection Module, Semantic Similarity Module and Flask Backend
