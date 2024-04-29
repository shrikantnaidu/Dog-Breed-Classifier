# Dog Breed Classifier

This project builds a pipeline to process real-world images of dogs and humans to identify dog breeds. 

## Project Overview

The goal of this project is to build an algorithm that can be used within a web or mobile app to process real-world images of dogs and humans. The algorithm will:

- Accept any user-supplied image as input 
- Detect humans in images and provide an estimate of the most resembling dog breed
- Detect dogs in images and provide an estimate of the dog's breed

The project explores convolutional neural networks (CNNs) for classification and localization tasks. Design decisions are made about the user experience of the app.

## Contents

The Jupyter notebook `dog_app.ipynb` contains the following steps:

1. Import Datasets
2. Detect Humans
3. Detect Dogs
4. Create a CNN to Classify Dog Breeds from Scratch  
5. Use Transfer Learning to Create a CNN to Classify Dog Breeds
6. Write the Algorithm
7. Test the Algorithm

## Usage

To run the app:

1. Clone this repository
2. Install requirements
3. Run Jupyter notebook
4. Open `dog_app.ipynb`
5. Run the notebook from top to bottom

The notebook accepts image paths as input to test the algorithm.

## Model Overview

The algorithm uses pre-trained VGG16 model for feature extraction and a custom classifier for dog breed prediction. Humans are detected using a Haar cascade classifier.

Key points:

- VGG16 is used for feature extraction 
- Custom fully-connected classifier is trained for dog breed prediction
- Haar cascade classifier detects human faces
- Dog detector checks if VGG16 prediction is between dog breeds

## Results

The algorithm achieves:

- 86% accuracy in predicting dog breeds on test set
- 100% accuracy in detecting dogs in sample dog images
- 1% false positive rate in detecting dogs in sample human images

## References

- VGG16: https://arxiv.org/abs/1409.1556
- Haar cascades: https://docs.opencv.org/2.4/modules/objdetect/doc/cascade_classification.html
