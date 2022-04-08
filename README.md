
# Lexical vs Vector Semantics
This repository contains the code that investigates the similarities between Lexical and Vector Semantics. This was done as a part of Assignment 03 for COMP8730 Course.

## Overview
The code for training Word2Vec and TF-iDF models on the Brown Corpus and Reuters Corpus can be found in the ``/code/word2vec`` and  ``code/tfidf`` directories. 
These models are then saved in the ``models`` directory, which are then used to create testing dictionaries for every single model saved at ``data/similarities``. 
These dictionaries are then compared with the golden truth (SimLex-999) words using the nDCG metric.

## [Setup](https://colab.research.google.com/drive/1xUQ30UxCi74e3_B1t1njEWau8O49-nho?usp=sharing)
To run our code, you need to have ```python >= 3.8``` installed. You can then use ```pip ``` to install all the required dependencies that are listed in ```requirements.txt```. 
Step 1: Clone this github repository and set it as your working directory by the following command:
```bash
!git clone https://github.com/Mrulay/COMP8730_Assign03.git
!cd /content/COMP8730_Assign03
```
Step 2: Install all the dependencies from the ```requirements.txt```
```bash
pip install -r requirements.txt
```
A tutorial notebook is available [here](https://colab.research.google.com/drive/1xUQ30UxCi74e3_B1t1njEWau8O49-nho?usp=sharing) that displays the execution of all these steps and performs testing of the code as well. 

## Results
![alt text](https://github.com/Mrulay/COMP8730_Assign03/blob/master/Picture1.png?raw=true)


Upon testing all the Word2Vec models, the best nDCG score was obtained with $window size=10$ and $vector size=10$ on Brown Corpus. While on Reuters Corpus, the most optimal parameters were $window size=10$ and $vector size=100$
The Word2Vec models trained on both The Brown Corpus and The Reuters Corpus perform better on this task. TF-iDF values only represent the weight of words based on their frequency, they do not represent the actual relation with other words. On the other hand, Word2Vec models actually look at the words surrounding them. 
