# Content-Based-Movie-Recommender-System

API : 9252174438851d4a8acccdee16cfe66d
Dataset : https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv
**Application can be found at:** https://github.com/siddmodi/movie-recommendation-system

Content Based Recommender System recommends movies similar to the movie with their tags and cluster them together using cosine similarity between them

Check out the live demo: ### herokuapp link ###

## How to get the API key?

Create an account in https://www.themoviedb.org/, click on the `API` link from the left hand sidebar in your account settings and fill all the details to apply for API key. If you are asked for the website URL, just give "NA" if you don't have one. You will see the API key in your `API` sidebar once your request is approved.

## How to run the project?

1. Clone or download this repository to your local machine.
2. Install all the libraries mentioned in the [requirements.txt](https://github.com/siddmodi/         movie-recommendation-system) file with the command `pip install -r requirements.txt`
3. Get your API key from https://www.themoviedb.org/. (Refer the above section on how to get the API key)
3. Replace YOUR_API_KEY in line no. 10 of 'app.py' file and hit save.
4. Run working_notebook.ipynb file and dump similarity.pkl file in directory.
5. Open your terminal/command prompt from your project directory and run the file `app.py` by executing the command 'streamlit run app.py'.
6. Hurray! That's it.


## Similarity Score : 

   How does it decide which item is most similar to the item user likes? Here we use the similarity scores.
   
   It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.
   
## How Cosine Similarity works?
  Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.
  
  ![image](https://user-images.githubusercontent.com/36665975/70401457-a7530680-1a55-11ea-9158-97d4e8515ca4.png)

  
More about Cosine Similarity : [Understanding the Math behind Cosine Similarity](https://www.machinelearningplus.com/nlp/cosine-similarity/)

===================**Explaination**===================

Streamlit app to recommend simillar top 5 movies based on movie we search of the collection of 5000 movies data. we created content based recommendation system

similarity between movies are calculated based on their similarity score 
We fatch posters of movies using API 
We clean data and extract some features from it 
Based on cosine similarity we recommend movies with higher ones  
This whole process works in 5 stages 
	Data-preprocessing
   model making
   create streamlit app
   deployment
Here we use Bag of words for vectorization 
