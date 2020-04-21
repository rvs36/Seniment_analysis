The goal of this project was to predict the sentiment of a sentence (positive, negative or neutral) based on the sentences recorded for reviews of the restaurnats in the city.

# Dataset description 
Each line contains 5 tab-separated fields: the polarity of the opinion, the aspect category on which the opinion is expressed, a specific target term, the character offsets of the term (start:end), and the sentence in which that opinion is expressed.  
There are two files - the one for training and another one for testing (dev file)

# Approaces  
## Aproach 1 - Training Neural Network 

The sentiment terms were extracted from the given sentence and then a neural network with a custom architecture was trained on these sentiment terms and hence the sentiment label.  
This neural network was then used to predict the sentiment for the dev dataset

## Approach 2 - Using BERT to get the sentiment of the sentence.
Bidirectional Encoder Representations from Transformers [BERT](https://ai.googleblog.com/2018/11/open-sourcing-bert-state-of-art-pre.html) is a technique for NLP pre-training developed by Google.  
The sentences were given as an input to the BERT model and then a SVM model was used to predict the sentiment for the dev dataset.  

# Results

- Training a neural network with cutom architecture from random wheights gave us an accuracy of **approx. 75%**  
- Leveraging BERT+SVC to predict the sentiment gave a result of **approx. 84%** 
