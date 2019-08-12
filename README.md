# Sentiment analysis of IMDb movie reviews: a study on features selection & classification algorithms


## **Phuong T.M. Chu, Lan Nguyen and Tu Nguyen**

![](https://i.imgur.com/NjCp49S.png)

## INTRODUCTION:

**IMDb (Internet Movie Database)** is an online database of information related to films, television programs, home videos, video games, and streaming content online – including cast, production crew and personal biographies, plot summaries, trivia, fan and critical reviews, and ratings. An additional fan feature, message boards, was abandoned in February 2017. Originally a fan-operated website, the database is owned and operated by IMDb.com, Inc., a subsidiary of Amazon.
By late 1990, the lists included almost 10,000 movies and television series correlated with actors and actresses appearing therein. On October 17, 1990, Needham developed and posted a collection of Unix shell scripts which could be used to search the four lists, and thus the database that would become the IMDb was born.At the time, it was known as the `rec.arts.movies movie database`.
Internet Movie Database users are invited to participate in the site's ever-growing wealth of information by rating movies on a rating scale.
The labeled dataset consists of 50,000 IMDB movie reviews. No individual movie has more than 30 reviews. The 25,000 reviews labeled training set does not include any of the same movies as the 25,000 review test set. 

### *There are three columns in the movie review dataset:*
* Id
*	Review 
*	Sentiment

### *There are two classes in the movie review dataset:*
*	1 : >= 7 rating
*	0: <5 rating

### *This project explores the applicability of machine learning based classification techniques:*
1.	Logistic Regression
2.	Decision Tree
3.	Random Forest 
4.	Gaussian Naïve Bayes & Multinomial Naïve Bayes
5.	K-Nearest Neighbor
6.	SMV – Support Vector Machine

We are going to determine that feature selection improves the performance of sentiment based classification, but it depends on the method adopted and the number of feature selected. The experimental results presented in this project show that Logistic Regression performs better than other techniques for sentiment based classification.

### Models Performance Summary


| Models | Additional conditions |Accuracy (before features selection) | Accuracy (after features selection)|
| --- | --- | --- | --- |
| * **Logistic Regression** |---  | **0.884** |**0.8881481481481481**|
| Logistic Regression |`chi2, k=45000`  | --- | 0.7644444444444445 |
| Decision Tree |---  | 0.7094814814814815 | **0.7197037037037037** |
| Random Forest | default | 0.7585185185185185 | --- |
| Random Forest | `n_estimators = 200` | 0.8428148148148148 | **0.8573333333333333** |
| KNN | `k=71` | 0.8065185185185185 | **0.8139259259259259** |
| SVM | `C=1` | 0.8814814814814815 | **0.8837037037037037** |
| SVM | `C=3` | 0.8765925925925926 | --- |
| Multinomial Gaussian Naive Bayes | --- | 0.8622222222222222 | 0.8622222222222222 |
| Gaussian Naive Bayes | --- | 0.6687407407407407 | **0.6688888888888889** |

## C

* Sentiment classification methods above identify texts from the review dataset according to the users opinions toward movies, which are both negative and positive. The extracted data is further enhanced using feature classification techniques and these methopologies facilitate the keywords from the users reviews. After training and testing the dataset, **Logistic Regression** has the **best result** compared to the other methods.
* We successfully **improve the accuracy** of our baseline models by **adding more stop words**.

