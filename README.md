# Movie-Recommendation-System

Recommendation systems have become prevalent in recent years as they deal with the information overload problem by suggesting to users the most relevant products from massive data.
Some people like genre-specific movies be it a thriller, romance, or sci-fi, while others focus on lead actors and directors. When we take all that into account, it’s astoundingly difficult to generalize a movie and say that everyone would like it. The main goal of the recommendation system is to forecast the rating that a specific user gives to an item. It helps the user to find the best solution from the available list of items. Many companies use recommendation systems so that they can serve their user and raise their profit like Netflix, such YouTube, Amazon, others Still now it is a good topic of research because finding what the user wants from the available resource is a big challenge, as our choice keeps on changing with time. Nowadays what we purchase online is a recommendation. 

# Dataset

MovieLens 20M Dataset:- https://grouplens.org/datasets/movielens/20m/
 
--> by grouplens.org
 
--> 20 million ratings 

--> 465,000 tag applications applied to 27,000 movies by 138,000 users.


# Methodology
## Content-Based Filtering 

This filtering recommends items to the user based on his past experience. For example, if a user likes only action movies, then the system predicts him only action movies similar to it that he has highly rated. If a user likes only politics-related content so the system suggests websites, blogs, or news similar to that content.

## TF-IDF Vectorizer
TF-IDF is commonly used in text mining and information retrieval tasks, such as document classification, sentiment analysis, and search engines. It is a useful tool for identifying important words in a document and for comparing the similarity between documents.
TF-IDF stands for term frequency-inverse document frequency. It is a popular technique used in natural language processing (NLP) to represent the importance of words in a document.
In TF-IDF, each word in a document is assigned a score that reflects its importance. The score is calculated by multiplying the term frequency (TF) and inverse document frequency (IDF) of the word.

Term frequency (TF) measures the frequency of a word in a document. It is calculated as the number of times a word appears in a document divided by the total number of words in the document.

Inverse document frequency (IDF) measures how important a word is across all documents in a corpus. It is calculated as the logarithm of the total number of documents in the corpus divided by the number of documents that contain the word.
The TF-IDF score is calculated as the product of the term frequency and inverse document frequency. Words that are common in a document but rare in the corpus are assigned high scores, indicating that they are important for that document. Words that are common in both the document and the corpus are assigned lower scores, indicating that they are less important for that document. 

We apply this Using in-built library – “from sklearn.feature_extraction.text import TfidfVectorizer”	

# Collaborative Filtering

Collaborative Filtering is one of the most well-known techniques for recommending items. This technique suggests relevant items to the user based on the neighbour’s choice. It first finds out the similarity between the user and his neighbour and then predicts the items.

# Hybrid filtering

Third filtering technique is hybrid filtering it basically combines both collaborative filtering, content-based filtering to overcome the challenges of each method like collaborative filtering may lack information about domain dependencies while content-based filtering lacks information about the preferences of the people and user behaviour data and the content data are used to come up with recommendations.

Hybrid = (content + collaborative) / 2

## Dimensionality reduction using truncated SVD

This transformer performs linear dimensionality reduction by means of truncated singular value decomposition (SVD). Contrary to PCA, this estimator does not centre the data before computing the singular value decomposition. This means it can work with sparse matrices efficiently.

## Similarity measures

In this project we used Cosine similarity as the measure of similarity which gives a score between two movies defining the similarity. It measures the angle between these two vectors.
Mathematically, cosine of two non-zero vectors can be calculated using dot products of these two vectors:
 
For two given vectors u and v ( here, movies ) , the cosine similarity, cos of angle theta will be computed as the combination of dot product divide by magnitude of the vectors:

![image](https://github.com/sanidhya-chaudhary/Movie-Recommendation-System/assets/109888164/e38b4e7d-cf48-4500-8f1f-be50d92b552a)

# Results and discussion

We will get recommendations on basis of user requirements. Three input from user will be taken, First “Movie_Name”, Second “Recommendation_Method”, Third one is “No. of Movies to be recommended

![image](https://github.com/sanidhya-chaudhary/Movie-Recommendation-System/assets/109888164/0e413ffc-5a7d-42f4-9657-16e4641711eb)


![image](https://github.com/sanidhya-chaudhary/Movie-Recommendation-System/assets/109888164/c3a7f58c-ce2e-416f-a232-1ffc13710795)

![image](https://github.com/sanidhya-chaudhary/Movie-Recommendation-System/assets/109888164/9610b9d7-885b-4321-be67-5c321a28cca8)


# Conclusion

Movie recommendation systems are an essential part of the entertainment industry including  The above-mentioned types of recommendation systems, algorithms, and evaluation metrics can help to create a better system that provides relevant recommendations to the users. However, it's important to note that there are still challenges associated with these systems, including the cold-start problem and the diversity problem. Therefore, there is a need for further research and development in this field.
Challenges and Future work

(i)	Cold Start - A comparison is always made on the characteristics of the user was and the features of the movie and the rating given to the movie. However, in some instances, there are no user characteristics that can be used for a recommendation if the user is new, and nothing is known about them.

(ii)	Diversity - The new excellent movies may end up not being watched because of the lack of being rated by the users. Some of the excellent movies also may not be rated, leaving the recommendation system blank about whether the movies are great for a specific class of watchers or not.

There are various advances in the use of blockchain technology, and some of these applications may affect the efficacy of algorithms in movie recommender systems. Blockchain technology enhances user privacy through user data encryption; yet collaborative filtering depends on the availability of user information so that it can match the features and characteristics before making recommendations.








