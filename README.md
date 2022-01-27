# Covid Based Tweet Analysis from scratch using Bert
BERT stands for Bidirectional Encoder Representations from Transformers. It's intended to use both left and right context conditioning to pre-train deep bidirectional representations from unlabeled text. As a result, with just one extra output layer, the pre-trained BERT model may be fine-tuned to generate state-of-the-art models for a wide range of NLP applications.

In other words, the BERT scans the entire sequence of words at once, unlike directional models that read the text input sequentially (left-to-right). As a result, it is classified as bidirectional. This feature enables the model to learn the context of a word from its surroundings (to the left and right of the word).

For the task of finding how covid has affected the mental health of people around the world, Tweets were extracted using tools like TWINT and TWEEPY.
TWINT is an advanced Twitter scraping tool written in Python that allows for scraping Tweets from Twitter profiles without using Twitter's API. Whereas, TWEEPY is an open source Python package that gives you a very convenient way to access the Twitter API with Python. Tweepy includes a set of classes and methods that represent Twitter's models and API endpoints, and it transparently handles various implementation details, such as: Data encoding and decoding.

The extracted datasets were stored in respective CSV files. The raw dataset had a lot of noise like hashtags, retweets, account handles (@s). Which were then cleaned and removed. Both the datasets after respective cleaning were then merged into one csv file.

After cleaning and merging, the next task was to determine the sentiment of the tweets. The library TEXTBLOB was used for that task, to find the POLARITY and SUBJECTIVITY of the tweets.

Polarity is a float value which lies in the range of [-1,1] where 1 means positive statement and -1 means a negative statement. Subjective sentences generally refer to personal opinion, emotion or judgment whereas objective refers to factual information. Subjectivity is also a float which lies in the range of [0,1]. Subjectivity quantifies the amount of personal opinion and factual information contained in the text. The higher subjectivity means that the text contains personal opinion rather than factual information. TextBlob has one more parameter — intensity. TextBlob calculates subjectivity by looking at the ‘intensity’. Intensity determines if a word modifies the next word. For English, adverbs are used as modifiers (‘very good’)

This is what the updated dataset looks like:
![](images/Bert-Model/textblob-csv.jpg)


