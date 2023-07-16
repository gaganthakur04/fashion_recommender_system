# Fashion_recommender_system
A fashion recommendation system is an application that recommends the most trending fashion based on the user’s search query. For example, if a user is looking for a Kurti, the recommendation system will recommend the most trending or highly rated Kurtis on their platform.

To build a fashion recommendation system, we need a dataset based on fashion products. We collected data about Kurtis from Myntra that we can use to create a fashion recommendation system using Python.

Data collection and preprocessing:
First of all we have to import the necessary python libraries.
![1](https://github.com/gaganthakur04/fashion_recommender_system/assets/64032653/f73aae1c-0cd6-4346-8dea-218650553a90)

![1 5](https://github.com/gaganthakur04/fashion_recommender_system/assets/64032653/3204cd43-f2f6-4ef2-8c4c-e31710c7b36e)

The data contains information about:

Brand name of the product
URL of the product
Image URL of the product
Ratings of the product on Myntra
Total number of ratings
Information about the product
Selling price and original price of the product
and discount on the product

Since image column has 467 null values therefore we can remove this column for our ease 
![2](https://github.com/gaganthakur04/fashion_recommender_system/assets/64032653/e5f2e323-e068-44e9-9e5b-fb65202bf8d4)

Now the large brand names appearing in the wordcloud show that they among the popular ones
![3](https://github.com/gaganthakur04/fashion_recommender_system/assets/64032653/8eb86263-0d76-48e7-946b-546f8cc9e164)

So, brands like Anubhutee, Malhaar, Now, Tissu, and Pistaa are popular for Kurtis on Myntra. Now let’s have a look at the highest-rated Kurtis on Myntra:

![4](https://github.com/gaganthakur04/fashion_recommender_system/assets/64032653/f253085b-dddc-4fcc-ae8a-499822f1e2d5)

So, brands like Indyes, Sangria, Malhaar, Fabindia, Paramount Chikan, Biba, and Saanjh are selling the highest-rated Kurtis on Myntra.

Finally recommending fashion products:

To recommend the trending fashion, we cannot use the content-based filtering strategy. The content-based filtering strategy is good to use when a user is looking at a fashion product, and your application wants to recommend something similar.

To recommend the trending fashion, we can find the weighted average of all the ratings and recommend the products based on the weighted average ratings. To count the weighted score of all the ratings of Kurtis, we need:

mean rating (mr): the mean rating of all the products
minimum ratings (m): minimum number of ratings
number of ratings (n): total number of ratings of the product
average ratings (a): average rating of the product
Now below is the formula to calculate the weighted score of the product ratings:

score = (n/(n+m) * a) + (m/(m+n) * mr)
Now let’s calculate the weighted score and recommend the most trending Kurtis on Myntra:

![5](https://github.com/gaganthakur04/fashion_recommender_system/assets/64032653/1e594683-33e1-45c9-ab21-bf7c2a5ec3cf)

Summary:
A fashion recommendation system is an application that recommends the most trending fashion based on the user’s search query. Myntra is one of the popular e-commerce platforms known for its fashion recommendations that's why we took it's data.
