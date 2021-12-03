# Protecting the Animals of the Mountain West Using Deep Learning

Every year in U.S. National Parks and recreation areas, wild animals and humans come into contact. From feeding wild animals and taking pictures too close to leaving food out, human behavior can cause animals to become accustomed to these interactions. Despite officials' attempts at wilderness education, we continue to see instances of people getting injured or killed in dangerous animal encounters. 

While we hear these humans' stories, we don't often know what such an encounter means for the animal. Unfortunately, the animals involved are often euthanized because they have become a threat to human life. Colorado averages 100 black bear euthanizations per year because the animals are becoming conditioned to interact with humans. I plan to build a model that detects the presence of four potentially dangerous species - black bears, moose, coyotes, and cougars. The purpose of this model is to flag the selected animals' appearance near campsites and towns, alerting park rangers and decreasing the likelihood for a encounter that turns deadly - for both the human and the animal. 

## Question/Need
Primary problem: 
- Animals are being killed due to human negligence 
- Human/animal encounters are common but often preventable

Benefit:
- Protecting local wildlife & habitats, reducing human impact on the ecosystem

## Data
- [LiLA North American Camera Trap Images dataset](https://lila.science/datasets/nacti) - collected image data for 10 categories : black bear, moose, cougar, coyote, squirrel, chipmunk, raccoon, deer, elk, empty
- This will be a binary classification task - looking for 'dangerous' animals (bear, moose, cougar, coyote) as the positive cases

## Tools
- Cleaning, EDA with Python, Pandas, Seaborn 
- Modelling using Keras/Tensorflow convolutional neural networks

## MVP Goal 
- End-to-end model built (ideally a CNN)
- Optimizing model for species detection - focus on recall as a main metric in order to flag as many sightings as possible 



