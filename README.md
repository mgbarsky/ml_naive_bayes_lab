# Text Classification with Naive Bayes

The goal of this lab is to build a model using Naive Bayes to classify movie reviews into positive or negative, 
and then test the classifier on new movie reviews.

The dataset is from the following publication: ''Thumbs up? Sentiment Classification using Machine Learning
Techniques''. Bo Pang, Lillian Lee, and Shivakumar Vaithyanathan.
Proceedings of EMNLP, pp. 79--86, 2002.
Similar datasets can be found on [this site](https://www.cs.cornell.edu/people/pabo/movie-review-data/).

Each review is stored in a separate text file. All the files are grouped into 2 subfolders: *pos* and *neg*.
The dataset can be downloaded from here: [movies_reviews](https://drive.google.com/file/d/1rAJqDC8p6b5RWwoUT-0HwsxWk-b3j8cR/view?usp=sharing).

- First of all, create a new Jupyther notebook, and implement a module that reads files and stores their content in 2 string arrays of file names.
- Next, you would need to convert the words in each document into a vector of word occurrences. 
You can use the code with stop words from the clustering demo or you can use the `sklearn` module `feature_extraction.text`, 
where you are interested in the `CountVectorizer` (for this one you would need to remove stop words) or in the `TfidfTransformer`. 
The latter assigns a score to each word based on its frequencies across all the documents, 
and thus the words that occur across all the documents (the stop words) get score zero, so there is no need to remove stop words. You can find a nice explanation and an example about tf/idf score [here](https://medium.com/analytics-vidhya/tf-idf-term-frequency-technique-easiest-explanation-for-text-classification-in-nlp-with-code-8ca3912e58c3). Whatever vectorization technique you chose, you would need to explain it in your own words in a separate markdown cell in your notebook. 
- Once you have a vector for each review, you can add the labels *pos* or *neg*, depending on the directory (as we did in cat/dog classification lab), and then dividse the dataset into training and testing.
- Now use the train dataset to build a Naive Bayes model. You can use the `sklearn` module `naive_bayes` from [here](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.naive_bayes) to accomplish this task. Carefully select the correct classifier for the data at hand by reading about different classification options.
- Test the accuracy on the train and on the test data. Try to reach the accuracy of at least 0.80.

Finally, find 5 new movie reviews on the internet which include a numeric or star rating (known to be positive or negative), and try to classify them into positive/negative using your classifier. Report and discuss the results in a separate markdown cell.

For starters, you can look at a demo of text classification [here](https://heartbeat.fritz.ai/understanding-naive-bayes-its-applications-in-text-classification-part-1-ec9caea4baae).

