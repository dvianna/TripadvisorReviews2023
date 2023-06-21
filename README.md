# Kaggle - Tripadvisor Reviews 2023

In progress....


# The Tripadvisor Reviews 2023 Dataset

The data can be downloaded from (file New_Delhi_reviews.csv):
https://www.kaggle.com/datasets/arnabchaki/tripadvisor-reviews-2023

The dataset is composed of reviews and ratings. Ratings can assumes values from 1 to 5, with 5 being the most positive rating.


# Topic Modeling

The first experiment, file topicmodeling.ipynb, uses topic modeling to cluster semantically similar reviews, Then, we go ahead and analyze some topics according with the reviews' ratings.

For example, for topic 211, we have most positive words:

![Worldcloud - Topic 211](https://github.com/dvianna/TripadvisorReviews2023/blob/main/img/words211.png)

By plotting the ratings we can see that all reviews were positive, with ratings been either 5 or 4.

![Ratings - Topic 211](https://github.com/dvianna/TripadvisorReviews2023/blob/main/img/plot211.png)


Looking at topic 198, we see mostly negative words (cockroaches):

![Worldcloud - Topic 198](https://github.com/dvianna/TripadvisorReviews2023/blob/main/img/words198.png)

By plotting the ratings, we can see that even though some clients mention seeing cockroaches, they still consider the experience positive, while others give very low ratings.

![Ratings - Topic 198](https://github.com/dvianna/TripadvisorReviews2023/blob/main/img/plot198.png)


# Sentiment Analysis

The second experiment, file sentimentanalysis.ipynb, uses the language model bloomz-560m to rate reviews as positive, neutral, or negatives (sentiment analysis).

[{'generated_text': 'Given the sentence delimited by triple backticks ```{go there . dont miss the chance. the food and service was great. just a bit expensive. ,my bill , alone was 100 $ ( no alcohol included)}``` Would you rate the previous review as positive, neutral or negative? positive'}]


# Classification

The third experiment, file classifier.ipynb, combines sentence-transformer and SVM to perform multi-class classification.

The original dataset was split (stratified) in 80%/20% for train and test. 

The confusion matrix resulted after running SVM on the 20% test set:

![Confusion Matrix - Imbalanced Dataset](https://github.com/dvianna/TripadvisorReviews2023/blob/main/img/confmatrix_imbalanced.png)

Using SMOTE, an over sampling technique, to improve the performance of the minority classes:

![Confusion Matrix - SMOTE](https://github.com/dvianna/TripadvisorReviews2023/blob/main/img/confmatrix_smote.png)
