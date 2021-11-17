# Protecting the Animals of the Mountain West Using Deep Learning

Every year, humans and animals interact in U.S. National Parks and other recreational areas. From feeding wild animals to taking pictures to close, to even leaving food out, human behavior can cause animals to become accustomed to these interactions. Despite officials' attempts at wilderness education, we continue to see instances of people getting hurt or killed in dangerous animal encounters. 

While we hear about what this means for the injured person, we don't often know what it means for the animal. Unfortunately, the animals involved are often euthanized because they have become a threat to human life. Colorado averages 100 black bear euthanizations per year because the animals are becoming conditioned to interact with humans. I plan to build a model that detects the presence of four potentially dangerous species - black bears, moose, coyotes, and cougars. The purpose of this model is to flag the selected animals' appearance near campsites and towns, alerting park rangers and decreasing the likelihood for a encounter that turns deadly - for both the human and the animal. 

## Question/Need
Primary problem: 
- Animals are being killed due to human negligence 
- Human/animal encounters are common but somewhat preventable

Benefit:
- Protecting local wildlife & habitats, reducing human impact on ecosystem

## Data
- [LiLA North American Camera Trap Images dataset](https://lila.science/datasets/nacti) - collected image data for 10 categories : black bear, moose, cougar, coyote, squirrel, chipmunk, raccoon, deer, elk, empty

## Tools
- Cleaning, EDA with Python, Pandas, Seaborn 
- Modelling using Keras/Tensorflow 

## MVP Goal 
- End-to-end model built 
- Optimizing model for species detection - focus on recall as a main metric



