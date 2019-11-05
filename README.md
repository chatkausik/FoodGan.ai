# FoodGan.ai
App to classify the Food, identifies ingredients, calories and recommend similar type food based on health conditions.

# Introduction
This project was completed by Kausik Chattapadhyay. This article details how to create a web and mobile app image classifier and is deep-learning-language agnostic. 

FoodGan.ai app will capture food images and perform the following tasks :
1. Identify the Food.
2. Identify Ingredients and total calories.
3. Recommend similar food based on user health conditions.

Our example uses the fastai library, but a model weights file from any deep learning library can be used to create a web and mobile app using our methods.

# Summary
The project covers:

1. training a deep learning model for food images using fastai
2. deploying a web app using Heroku and Flask
3. deploying a mobile app

# Heroku Web App Deployment

[Heroku](https://www.heroku.com/) was utilized to deploy the web app.

### Input to Heroku App

This output file, **`model.pth`** is the input to the Heroku app.  

 
### Test running the web app
This contains Python 3, Flask and fastai.
```
docker build -t app .
docker run -p 5000:5000 -it app 
```

## Heroku Setup
If you don't have a Heroku account, create one here: [www.heroku.com](https://www.heroku.com/).  Each line can be copied and submitted.  
```
wget -qO- https://cli-assets.heroku.com/install-ubuntu.sh | sh
heroku login
heroku container:login

APP_NAME="food-img-classifier"
heroku create $APP_NAME

heroku container:push web --app ${APP_NAME}

heroku container:release web --app ${APP_NAME}
heroku open --app $APP_NAME
heroku logs --tail --app ${APP_NAME}
```

Note:  After 15 minutes of inactivity, Heroku will suspend the app.  The next time the web app is called, Heroku will restart the app.  There could be a slight delay in starting the app.
 
## Our Flask Web Application
- Our Flask web app is available here:  [**foodgan-ai.herokuapp.com**](https://foodgan-ai.herokuapp.com/)
- Give it a try!  Upload an image or add a URL. 

# Our mobile apps are available:

iOS Apple store: 
Android Google Play:

# Our GitHub repositories:


