# Clustering User Comments on News Articles
![](/images/wordclouds.png?raw=true "Example Images")
## Introduction

The news industry has been in decline for the last two decades. What was once a thriving industry is now a shrinking and competitive field. The chart below is from a [Pew Research Center study](https://www.pewresearch.org/fact-tank/2020/04/20/u-s-newsroom-employment-has-dropped-by-a-quarter-since-2008/), showing the decrease in newsroom employment over the last twenty years. As customer retention becomes more difficult, these companies to learn as much as they can about their customers, and what drives engagement for their particular market segment. 

<img src=https://www.pewresearch.org/wp-content/uploads/2020/04/ft_2020.04.20_newsroomemployment_01.png>

## Data

I used comments on New York Times articles from April 2017. The dataset had information on the comments, commenters and the article about which they were posting. Some of the variables included: time the comment was written; commenter's location; number of upvotes the comment received; subject of the article the comment was written about; and the body of the comment.

## Methodology

During exploratory data analysis I focused on the comment bodies, looking at the most common words overall and by topic. I created several features including a `writingTime` feature representing the number of minutes the commenter worked on their comment, and several features to reflect the presence of the most common words.


By the time I had finished creating features and encoding my categorical variables, the dataset had close to 100 features. I tried several dimensionality reduction techniques, comparing the results of UMAP, FAMD and PCA. The PCA components did not score as well as the others, so I did not run those through my clustering models. 

## Results

I ran KMeans, DBSCAN and GMM on the UMAP and FAMD components, and compared the results. KMeans was the most successful at clustering the comments into consistent groups. The clusterings were useful as they allowed us to gain insight into the average features for each group of comments.


The original dataset can be found <a href='https://www.kaggle.com/aashita/nyt-comments?select=CommentsApril2017.csv'>here</a>.
