# Kaggle - Tripadvisor Reviews 2023

In progress....


# The Tripadvisor Reviews 2023 Dataset

The data can be downloaded from (file New_Delhi_reviews.csv):
https://www.kaggle.com/datasets/arnabchaki/tripadvisor-reviews-2023

The dataset is composed of reviews and ratings. Ratings can assumes values from 1 to 5, with 5 being the most positive rating.


# Topic Modeling and Sentiment Analysis

The first experiment, file topicmodeling.ipynb, uses topic modeling to cluster semantically similar reviews, Then, we go ahead and analyze some topics according with the reviews' ratings.

For example, for topic 211, we have most positive words:

![Worldcloud - Topic 211](https://github.com/dvianna/TripadvisorReviews2023/blob/main/omg/words211.png?raw=true)

By plotting the ratings we can see that all reviews were positive, with ratings been either 5 or 4.

![Ratings - Topic 211](https://github.com/dvianna/TripadvisorReviews2023/blob/main/omg/plot211.png?raw=true)


Looking at topic 198, we see mostly negative words (cockroaches):

![Worldcloud - Topic 198](https://github.com/dvianna/TripadvisorReviews2023/blob/main/omg/words198.png?raw=true)

By plotting the ratings, we can see that even though some clients mention seeing cockroaches, they still consider the experience positive, while others give very low ratings.

![Ratings - Topic 198](https://github.com/dvianna/TripadvisorReviews2023/blob/main/omg/plot198.png?raw=true)
