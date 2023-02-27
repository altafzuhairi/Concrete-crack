# Identifying Concrete Cracks with Image Classification using Neural Network
# 1. Summary 
The aim of the project is identify cracks on concrete images using convolutional neural network. This project is a computer vision task where it is a binary classification problem. The model is trained with a dataset of 400000 images where 200000 images is divided equally between positive (cracks) and negative (no cracks) classes. The source of the dataset can be found https://data.mendeley.com/datasets/5y9wdsg2zt/2
# 2. IDE and Framework
This project is completed mainly using VS Code IDE. The main frameworks used in this project are Numpy, Matplotlib and TensorFlow Keras.
# 3. Methodology
The methodology for this project is inspired by a documentation on the official TensorFlow website. The documentation can be refer https://www.tensorflow.org/tutorials/images/transfer_learning

3.1 Model Pipeline

The input layer of the model is designed to receive coloured images with dimension of (180,180,3). Data augmentation layers is used on the input images with random rotation and random flip.

Transfer learning approach is used in this project. Preprocessing layer is created to transform the images so that the pixel values is standardised to range between -1 and 1. This layer acts as a feature scaler of the input images.

For feature extractor, a pretrained model of MobileNetV3 is used. The model is readily available within TensorFlow package, with ImageNet pretrained parameters.

A global average pooling and dense layer are used as the classifier to output softmax activation function. The sofmax are used to predict the class of the input images.

The simplified illustration of the model is shown in the figure below.

![model](https://user-images.githubusercontent.com/124944787/221598005-05b8f398-e59b-4800-b6de-33d6955b7f5a.png)

# 4. Results
The model is evaluated with test data. Some predictions are made with the model are shown in the figure below.

![image](https://user-images.githubusercontent.com/124944787/221610974-e45ab8d0-a2be-4134-a0c1-94e832031d31.png)

