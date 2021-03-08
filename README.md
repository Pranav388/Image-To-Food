# Image-To-Food

The project consists of mainly two models. The first model is an object recognition model used for identifying the food item from the input image. The second model is a popularity based recommendation model which will recommend the top five recipes for the identified food item.

Model1 is based on  ResNet50.
Model2 is based on Recommendation System.

Data set for Food image classification is https://www.kaggle.com/kmader/food41 
For Recipe Recommendation https://www.kaggle.com/shuyangli94/food-com-recipes-and-user-interactions?select=interactions_train.csv

Formula used for Recommendation System:-

For the Popularity based recommendation system we have used the IMDb formula. This formula provides a true 'Bayesian estimate', which takes into account the number of votes each title has received, minimum votes required to be on the list, and the mean vote for all titles:
weighted rating (WR) = (v ÷ (v+m)) × R + (m ÷ (v+m)) × C
Where:
R = average for the movie (mean) = (rating)
v = number of votes for the movie = (votes)
m = minimum votes required to be listed in the Top Rated list (currently 25,000)
C = the mean vote across the whole report

Main Function: 

Loading the saved model into the main function.
It has GUI where we have three buttons:
a) Select Image
b) Get Recipes
c) Exit
After Selecting desired image, the main function will call model 1(Image Classification) and will tell what food is there in the selected image.
If you click on the Get Recipes button, then you’ll be redirected to the top 5 recipes section (Model 2).
The user can choose their favorite recipe out of that recommended top 5 recipes.
Exit button will destroy the window.

