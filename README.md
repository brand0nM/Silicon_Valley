# Silicon_Valley
## Overview
This project was [Inspired](https://www.youtube.com/watch?v=ACmydtFDTGs) by a scene in Silicon Valley; Jin Yang created a Logistic Classifier that takes images as input and returns a boolean value of hotdog and not hotdog. To expand upon this idea I figured we could take an image as input and output a percentage for how likely it is each train group; The maxmimum predicted value is the most similar group- essentially a linear model

### Purpose
Using Beautiful Soup scrape a folder of images for each produce item, then train a neural network to classify new images. Tensorflow has a built in function called image_dataset_from_directory which allows us to input a directory containing folders for each produce item- these folders each hold a collection of images of that produce item.

## Analysis
### Scraping Produce Images
First we scrape a list of 100+ produce names, then each item is seached in google images; after converting the page to soup we collect the encoded src and convert the src to a useable link. Finally we decode its bits and save the image in the items directory. 
### Tensorflow Model
Before analyzing the images we must first scale each pixels color to be between 0 and 1. After we cache and prefetch necessary images to avoid bottlenecks in the model. Finally 7 hidden layers were used to train the model; These layers were chosen based on image preprocess theory- reducing images to their principle components
## Summary
We we're successful in creating an image classifier to predict the images superset. With more picture of each item the model will get more precise; To further refine this project I would create a scraping function that collects 1000+ pictures per category
