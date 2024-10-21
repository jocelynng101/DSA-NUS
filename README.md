# Introduction
Goal: Develop a word embedding model in Python and train it to find the most similar medical words to a given target word using scholarly articles about COVID-19, SARS-CoV-2, and related corona viruses (CORD-19, 2020)

# Background & Methodology
Word Embeddings are short, dense vectors that represent words. In this project the Skip-Gram architecture with negative sampling (SGNS) method is used to compute the embeddings. This is one of the methods the package word2vec uses to determine embeddings. Word2vec is a neural network-based technique used to generate vector representations of words in a continuous vector space. The resulting word vectors capture semantic meanings, allowing for mathematical operations like finding similarities and relationships between words. 
How does the math work? The method learns a fixed (static) embedding for each word in the vocabulary based on the words surrounding that word). The word embedding itself is the weight the classifier that comes up with how likely a word is to occur around another word.

# Implementation
There are 4 main steps to implementing this method:
1) Treat the target word and a neighboring context word as positive examples
3) Randomly sample other words in the lexicon to get negative samples
4) Use logistic regression to train a classifier to distinguish between those two cases
5) Used the learned weights as the embedding

# Discussion
...

# Resources
https://developer.ibm.com/tutorials/awb-stemming-text-porter-stemmer-algorithm-python/ 

Jurafsky and Martin. 2009. Speech and Language Processing (2nd Edition). Pearson.
COVID-19 Open Research Dataset (CORD-19). 2020. Version 2024-10-20. Retrieved from COVID-19 Open Research Dataset (CORD-19). Accessed 2024-10-20. doi:10.5281/zenodo.3715505
