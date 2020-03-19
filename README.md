# Kaggle's Digit Recognizer Competition
### March 6, 2020
### Lisa Hwang
### https://www.kaggle.com/c/digit-recognizer


### Objective
To become more familiar with neural networks by entering Kaggle's Digit Recognizer competition.


### Repo Contents
- README.md
- preds.csv - MNIST number predictions that were submitted to Kaggle
- DigitRecognizerNotebook.ipynb - Jupyter Notebook for modeling


### Competition Description From Kaggle
> MNIST ("Modified National Institute of Standards and Technology") is the de facto “hello world” dataset of computer vision. Since its release in 1999, this classic dataset of handwritten images has served as the basis for benchmarking classification algorithms. As new machine learning techniques emerge, MNIST remains a reliable resource for researchers and learners alike.

> In this competition, your goal is to correctly identify digits from a dataset of tens of thousands of handwritten images. We’ve curated a set of tutorial-style kernels which cover everything from regression to neural networks. We encourage you to experiment with different algorithms to learn first-hand what works well and how techniques compare.


### Data
The ```train.csv``` and ```test.csv``` were downloaded from https://www.kaggle.com/c/digit-recognizer/data.


### EDA
From Kaggle:
> Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255, inclusive.

There were 42,000 rows and 785 columns in the ```train.csv``` dataset. No null rows were present. The ```label``` column was for the actual numbers represented in the hand-drawn images, and the other 784 columns were for each pixel. The ```label``` variables were changed from continuous to categorical and normalized due to being image data. Pixel variables were normalized by dividing by 255 and scaled prior to modeling.


### Modeling
#### Model 1: Sequential Network
Using Keras, I created a sequential network which performed relatively well on the test data, with ```0.9515``` accuracy and ```0.9670``` accuracy on the train data.

#### Model 2: Convolutional Network (CNN)
Again with Keras, I set up a CNN which  performed well on the test data, with ```0.9771``` accuracy. The train accuracy was ```0.9982```. I used this model and the ```test.csv``` data to generate predictions for the Kaggle competition.


### Conclusions
I was able to practice creating neural networks by handling the MNIST data from Kaggle. My convolutional neural network outperformed the sequential neural network, with accuracy of ```0.9771``` . My accuracy on the Kaggle leaderboard was ```0.97742```.
