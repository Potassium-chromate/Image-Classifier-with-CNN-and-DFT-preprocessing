# Image-Classifier-with-CNN-and-DFT-preprocessing

This project aims to develop a Convolutional Neural Network (CNN) based image classifier for four weather conditions: cloudy, rain, shine, and sunrise. The images are preprocessed using Discrete Fourier Transform (DFT) to convert them into their frequency domain, which potentially reveals additional patterns or features not easily accessible in the spatial domain. This additional information might aid in the model's decision-making process, leading to improved performance.

## Installation
The code is written in Python, and uses tensorflow, keras, pandas, numpy, seaborn, matplotlib, sklearn, PIL, and cv2 libraries. Make sure these are installed in your environment.

## Dataset
The dataset should consist of grayscale images divided into four categories: cloudy, rain, shine, and sunrise. Place the training and test datasets in separate directories for each category.

## Running the Code
To run the code, provide the appropriate paths for the training and test datasets. Also, specify the desired target size for resizing the images. The model is trained using the training dataset and evaluated on the test dataset. The training and validation accuracy and loss are plotted. The confusion matrix is also displayed for both the training and test sets.

The code also includes data augmentation (rotation and flipping) in the load function, but it's currently not being used. You can utilize it by passing 'yes' as the argument while loading the data.

## Results
After training, the model achieves an accuracy of 90.55% and a loss of 0.2641 on the training data, and an accuracy of 77.33% and a loss of 0.6458 on the validation data. These results show that the model has learned to classify the images with reasonable accuracy.

Note: The performance gain by using DFT preprocessing might vary depending on the specifics of the dataset, the model, and the task. Here, DFT preprocessing improves the model's performance slightly, but your mileage may vary.

Remember that DFT preprocessing and other transformations are tools in your toolkit, and their effectiveness will largely depend on the specifics of the task at hand. It's always good to experiment and find what works best for your particular problem.





