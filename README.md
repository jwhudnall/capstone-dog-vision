# Capstone Project: Dog Breed CNN Model
This project involves convolutional neural networks. The end result is a model that accepts an image, and is able to:
* Determine it is a picture of a dog, along with the dog’s breed.
* Detect if the image includes the face of a human, alongside the dog breed that the human most resembles (great for party tricks!).
* If neither are detected, inform the user.

This project tackles the difficult problem of solving a multiclass classification problem. Quite difficult for us mere mortals; nothing for a well-tuned model. I will implement a convolutional neural network using Pytorch to identify the presence of humans and dogs, assigning each subject the dog breed they most resemble based on the model. At
first, I will train a CNN from scratch; later, I’ll improve my results by leveraging a pretrained model via transfer learning.

For example, if I input a picture of my face, the output should state that I am human, along with the dog breed most similar to my facial features. 
This is a supervised learning problem, as we will use labeled data to train the neural network.
### Software/Libraries Used
* cv2
* glob
* matplotlib.pyplot
* numpy
* os
* PIL
* torch
* torch.nn
* torch.nn.functional
* torch.optim
* torch.utils.data
* torchvision
* torchvision.models
* torchvision.transforms
* tqdm



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


### Sample Model Output
![Human Detected](/model-predictions/result-img-1.jpg) 
![Dog Detected](/model-predictions/result-img-2.jpg) 
![Neither Detected](/model-predictions/result-img-3.jpg)
