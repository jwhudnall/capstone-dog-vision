# Capstone Project: Dog Breed CNN Model

This project involves convolutional neural networks. The end result is a model that accepts an image, and is able to:
* Determine it is a picture of a dog, along with the dog’s breed.
* Detect if the image includes the face of a human, alongside the dog breed that the human most resembles (great for party tricks!).
* If neither are detected, inform the user.

For example, if I input a picture of my face, the output should state that I am human, along with the dog breed most similar to my facial features. 
This is a supervised learning problem, as we will use labeled data to train the neural network.


### Project Design
1. Import the data (both human faces and dog breeds).
2. For human images, I will utilize OpenCV to detect human faces, writing a human face detector.
3. For dog images, I will use a model that has been pre-trained on ImageNet to:
    * First, detect dogs
    * Second, classify specific dog breeds by writing a CNN from scratch.
    * Third, create another CNN to classify breeds, this time using Transfer Learning. 
4. Construct an algorithm to:
    * Check to see if a human is present. If so, it acknowledges this and also returns the dog breed that the human most resembles.
    * If a dog is present, the algorithm returns the dog’s breed.
    * If neither is present, this is indicated in the output.
5. Test the algorithm with random pictures to see how accurate the predictions are.
