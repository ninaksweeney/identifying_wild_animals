# Protecting Colorado Wildlife with Computer Vision : Using CNNs to Reduce Human/Animal Interactions

## Abstract

In the Rocky Mountains and around the country, human interactions with native animal species are putting animals in danger. Whether it's leaving out trash, taking pictures too close, or trying to feed an animal, human behaviors condition animals to be comfortable approaching people. When this finally happens, even if nobody is hurt, the animal is often deemed a public safety risk and euthanized. Since 2015, [592 bears](https://www.summitdaily.com/news/local/colorado-parks-and-wildlife-urges-reductions-in-human-bear-conflicts-after-euthanizing-120-animals-last-year/) have been euthanized in Colorado alone. The goal of this project is to alert park rangers and other authorities to the presence of dangerous animals near campsites and tourist attractions so they can step in before a risky interaction occurs. Using a convolutional neural network and transfer learning, I was able to flag the presence of bears, cougars, moose, and coyotes with 91% recall.

## Design

Though many species are present in the dataset, I only marked the four mentioned above as 'dangerous', converting a multiclass problem into a binary classification. The entire NACTI dataset was very unbalanced, so I selected a subset of images, with 57% positive cases, to train my CNN. I chose to focus on recall as my primary metric to emphasize risk mitigation, even if some harmless species are incorrectly identified. Once my model was trained, I adjusted my probability threshold to 25% in order to maximize recall while maintaining high accuracy & precision. 

## Data

To train this model, I used a subset of images (4,187) from the [North American Camera Trap Images dataset from LILA BC](https://lila.science/datasets/nacti). There are many species present in the full dataset (around 600,000 images), but I only included 10: bear, moose, coyote, cougar, squirrel, chipmunk, raccoon, deer, elk, and empty. The images were kept in color and resized to 224x224. 

## Algorithms

I trained 3 separate models - one RandomForest, one Convolutional Neural Net, and one Convolutional Neural Net with transfer learning. The transfer learning model, developed using Keras and MobileNetV2, performed the best upon validation. I reduced the learning rate to .0001 and implemented Early Stopping and ReduceLRonPlateau in order to maximize performance. I also utilized ImageDataGenerator to incorporate data augmentation, though it was not used in the final model due to reduced performance. Model performance was primarly judged on recall, with accuracy and precision monitored for balance. 

## Tools 

Data Manipulation: Numpy and Pandas   
Model Training: Scikit-Learn, Tensorflow/Keras, MobileNetV2   
Visualization: Matplotlib, Seaborn

## Communication

I completed a 5-minute presentation of model performance and architecture. Slides and visuals for this project are included in this repository. Future work includes bounding boxes to identify multiple individuals, allowing for flagging of more dangerous situations such as packs and offspring. 
