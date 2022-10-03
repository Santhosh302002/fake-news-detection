# fake-news-detection
In this work, we utilized the fake news dataset from Kaggle to classify untrustworthy news articles as fake news. We have a complete training dataset containing the following characteristics:

id: unique id for a news article
title: title of a news article
author: author of the news article
text: text of the article; could be incomplete
label: a label that marks the article as potentially unreliable denoted by 1 (unreliable or fake) or 0 (reliable).
It is a binary classification problem in which we must predict if a particular news story is reliable or not.



The statistics for the training and testing sets are as follows:

The text attribute has a higher word count with an average of 760 words and 75% having more than 1000 words.
The title attribute is a short statement with an average of 12 words, and 75% of them are around 15 words.
Our experiment would be with both text and title together.

We have imported NLTK, which is a famous platform for developing Python applications that interact with human language. Next, we import re for regex.
We import stopwords from nltk.corpus. When working with words, particularly when considering semantics, we sometimes need to eliminate common words that do not add any significant meaning to a statement, such as "but", "can", "we", etc.
PorterStemmer is used to perform stemming words with NLTK. Stemmers strip words of their morphological affixes, leaving the word stem solely.
We import WordNetLemmatizer() from NLTK library for lemmatization. Lemmatization is much more effective than stemming. It goes beyond word reduction and evaluates a language's whole lexicon to apply morphological analysis to words, with the goal of just removing inflectional ends and returning the base or dictionary form of a word, known as the lemma.
stopwords.words('english') allow us to look at the list of all the English stop words supported by NLTK.
remove_unused_c() function is used to remove the unused columns.
We impute null values with None using the null_process() function.
Inside the function clean_dataset(), we call remove_unused_c() and null_process() functions. This function is responsible for data cleaning.
To clean text from unused characters, we have created the clean_text() function.
For preprocessing, we will use only stop word removal. We created the nltk_preprocess() function for that purpose.


Explorative Data Analysis
In this section, we will perform:

Univariate Analysis: It is a statistical analysis of the text. We will use word cloud for that purpose. A word cloud is a visualization approach for text data where the most common term is presented in the most considerable font size.
Bivariate Analysis: Bigram and Trigram will be used here. According to Wikipedia: "an n-gram is a contiguous sequence of n items from a given sample of text or speech. According to the application, the items can be phonemes, syllables, letters, words, or base pairs. The n-grams are typically collected from a text or speech corpus".
