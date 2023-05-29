# Image-Classifier-with-CNN-and-DFT-preprocessing

This project aims to develop a Convolutional Neural Network (CNN) based image classifier for four weather conditions: cloudy, rain, shine, and sunrise. The images are preprocessed using Discrete Fourier Transform (DFT) to convert them into their frequency domain, which potentially reveals additional patterns or features not easily accessible in the spatial domain. This additional information might aid in the model's decision-making process, leading to improved performance.

## Installation
The code is written in Python, and uses tensorflow, keras, pandas, numpy, seaborn, matplotlib, sklearn, PIL, and cv2 libraries. Make sure these are installed in your environment.

## Dataset
The dataset should consist of grayscale images divided into four categories: cloudy, rain, shine, and sunrise. Place the training and test datasets in separate directories for each category.  
| label | cloudy | rain | sunrise |
|:-----:|:-----:|:-----:|:-----:|
|0|1|2|3|

## Model
![ALT](https://github.com/Potassium-chromate/CNN-for-recognizer-weather/blob/main/Picture/Model%20structure.png)
## Running the Code
To run the code, provide the appropriate paths for the training and test datasets. Also, specify the desired target size for resizing the images. The model is trained using the training dataset and evaluated on the test dataset. The training and validation accuracy and loss are plotted. The confusion matrix is also displayed for both the training and test sets.

The code also includes data augmentation (rotation and flipping) in the load function, but it's currently not being used. You can utilize it by passing 'yes' as the argument while loading the data.

## Results
### RGB
|       |train_acc|train_loss|test_acc|test_loss|
|:-----:|:-------:|:--------:|:------:|:-------:|
|CNN    |0.937    | 0.14     | 0.9067 |  0.8187 |  
|DFT + CNN|0.9494    | 0.14     | 0.92 |  0.698 |  
### Gray
|       |train_acc|train_loss|test_acc|test_loss|
|:-----:|:-------:|:--------:|:------:|:-------:|
|CNN    |0.9656   | 0.1078   | 0.7467 |  1.2034 |  
|DFT + CNN|0.9055 | 0.2641   | 0.7733 |  0.6454 |  






