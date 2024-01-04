Language: 
Python

Structure:
The code is structured to read the text files into dataframe in their original form, creating two columns, one with the raw text and one with the category of the text. The category column functions as the target for this process. Once the raw text is read into the dataframe, the text goes through a series of text processing methods, the first step is a series of regular expressions that replace either useless text or header text that gives information about the newsgroup message, this text is all replaced with blank space. Next I used the Natural Language Processing Toolkit to remove common stopping words (the, a, and, etc..) and stem the words (replace a word like "running" with "run"). Both of these are meant to reduce the dimensionality of the text. 

After processing the raw text, it is is vectorized using a term frequency inverse document frequency (TFIDF) bag of words method. This method helps to place more value on words that more frequently occur in the category of the newsgroups opposed to the entire series of texts. Finally, a Naive Bayes Classifier is applied to the training set, and then tested on the testing set. This process is done twice for binary classification - comparing just two categories and five times for triclass categories - three classes. The results of the classifier are listed below each implementation, the overall accuracy as well as confusion matrix are shown. 

How to run:
There are two source codes included, one is the py file and the other is python notebook file. I did this work in the notebook file and then downed the py version of it, I recommend using the notebook file.

To run the code, you need to point the base directory to where the file holding the articles is located. Once the variable base_dir is set, the program will run. 

Warning: 
Because of the amount of text files, the cleaning process, and the training on such a large volume of data, the program will take a long time to run. On my machine it takes roughly ten minutes to run through. 
