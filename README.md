# deep_learning_project

# Seafood Image Dataset Classification using Deep Learning 

Sophie Wang and Flora Chen completed this project for the class MSDS631 Deep Learning during the Master's of Data Science program at University of San Francisco 


## Dataset 
We obtained our dataset from Kaggle [here](https://www.kaggle.com/crowww/a-large-scale-fish-dataset?select=NA_Fish_Dataset). The dataset size in total is 3.25 GB and contains nine different types of seafood image: Black Sea Sprat, Gilt Head Bream, Horse Mackerel, Red Mullet, Red Sea Bream, Sea Bass, Shrimp, Striped Red Mullet and Trout. Each species contains 1000 images. 


## Preprocessing the data
We used python package [Albumentations](https://albumentations.ai/docs/) to proprocess the image data before feeding them into neural networks. Some of the image augmentation techniques we used include: random crop, elastic transformation, RGB normalization, center crop. 


## CNN Architectures
We have run the following pre-trained CNN architectures (AlexNet, VGG-19, ResNet34) and only fine-tuned the last linear layer for seafood classification and the table below shows the training set loss and validation set accuracy after three epochs on GPU:

|      | AlexNet    | VGG19   | ResNet34    |
| :------------- | :----------: | -----------: | -----------: |
|  Train Loss | 0.45  | 0.18    | 11.3    |
| Validation Accuracy  | 0.88 | 0.97  | 0.98  |
|  Num of Params | 57,040,713 | 139,607,113  | 21,797,672 |

From the summary table above, we can clearly see that ResNet34 is the winner here, with the highest validation accuracy and least number of parameters (the most efficient architecture)
