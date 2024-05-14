# Potato Disease Classification by Analysing Plant Leaves using Convolutional Neural Networks
## Problem Statement:
Plant diseases reduce the crop yield that can results in higher food costs and shortage of food. The staple food source potatoes are essential food crop due to its high nutritional value and global consumption. However, potato crops can severely damage by plant pathogens. Early Blight and Late Blight are two most common fungal diseases in potato crops. The conventional methods to identify diseases in potato crops are costly and cumbersome. An agriculture expert person is required to execute these conventional techniques. To manage diseases, farmers require new techniques that should be less expensive, fast, reliable, and highly accurate. Such techniques are considered as highly practical because they would assist farmers in efficient management of crops by applying treatments more efficiently, which can maintain overall economic value of potato crop. Additionally, it enables targeted use of fungicides where it is necessary, reduces the input costs of disease management. Recently, many researchers are using deep learning techniques into disease classification of crops because they facilitate automatic feature extraction from visible range images due to its multi-layer architecture, which contains convolutional layers that automatically acquire spatial hierarchies of features from images (e.g., from edges to shapes of object). Additionally, there exist several pre-trained transfer learning models such as AlexNet, ResNets, VGGNet, RFCN, R-CNN, SSD, YOLO, MobileNets, EfficientNets etc., which can be optimized or fine-tuned for disease identification in crops. However, these models are not specially designed for a particular objective, as they are trained on large dataset called "ImageNet" that has millions of labeled images across thousands of categories, which might generate possibilities for precision error. Additionally, pre-trained models have complex multi-layer architectures, which can lead to high computational burden and making it challenging to deploy in resource-constraint devices. Additionally, complex pre-trained models have less interpretability, which might create difficulty for researchers to understand essential contributing features of disease and decision-making.
## Aim:
The motivation of this work is to build a customized deep CNN model specifically designed to efficiently classify diseases in potato leaf plants with minimum number of layers, optimized hyper parameters, high accuracy, and less computational burden. The research aims to strike a balance between detection accuracy and computational efficiency, and build a robust and reliable tool to help farmers in managing potato crops.   
## Proposed Methodoly:
### Proposed Dataset:
The dataset proposed to meet objectives of this work is the Plant Village dataset, which is an open-source publicly available benchmark agriculture dataset. This dataset includes 1000 images for Potato Early Blight, 1000 images for Potato Late Blight, and 152 images for Potato Healthy.
### Data Pre-Processing:
- **Image Resizing and Rescaling:** Images are resized to height and width of 256×256. Additionally, the original range of pixel values of images are rescaled to the normalized value of [0,1] by the scaling factor of 1.0/255.
- **Data Preparation:** In dataset preparation, the images will be divided into train, test, and validation split. 80% of the data will be allocated as train split, which will be used to train the model and 10% of the data will be allocated as test split, which will be used to evaluate the model. 10% of the images will be allocated as validation split, which will be utilized to assess the model’s performance during training by supplying it to the model after each epoch.
- **Data Augmentation:** Data augmentation will make the dataset more robust and diverse by introducing slight variations. By this it will improve the generalizability of the model, prevents overfitting, and balance class distribution. The dataset proposed for this work includes 1000 images for Early blight, 1000 images for Late blight, and 152 images for healthy class. However, there are only 152 images for healthy class which might lead to biased result due to class imbalance. The proposed solution for class imbalance is Data augmentation pipeline, which augment the training images on-the-fly rather than increasing the number of images physically. To increase number of training data size, five run time data transformations are proposed: Random flip, Random rotation by 0.2 factor, Random zoom by 0.2 factor, Random translation by 0.2 factor, and Random contrast by 0.2 factor.
### Proposed CNN Model's Architecture:
![Proposed architecture of CNN model for disease classification](https://github.com/MadhuSainani/Potato-disease-classification-by-analysing-plant-leaves-using-Convolutional-Neural-Networks/blob/main/Proposed%20Architecture%20of%20CNN%20Model.png)

## Experimental Setup:
- Framework: TensorFlow’s Keras Open Source Library 
- Training Environment: Google Collaboratory’s GPU 
- Loss Function: Sparse Categorical Cross Entropy
- Optimizer: Adam (Adaptive Moment Estimation)
## Result and Analysis:
The proposed CNN model is trained on Potato leaf dataset from benchmark Plant Village dataset. In the proposed experiment, Sparse categorical cross entropy is utilized as a loss function to estimate loss value between true and predicted classes. Adam (Adaptive Moment Estimation) algorithm is utilized for gradient optimization with default exponential decay rates of β1 = 0.9 for first moment and β2 = 0.999 for second moment. Adam optimizer offers adaptive learning by computing the ratio of first moment and second moment, which allows model to adapt learning rate for individual parameters. Although, the Adam optimizer has integrated adaptive learning rate system. In this work, various learning rates and batch size are experimented to visualize their effects on disease classification task. 
The model architecture experimented for this work includes 3 convolutional layers, 3 max pooling layer, dropout rate of 0.4, one dense layer with 64 neurons, and SoftMax output layer. Below Table showing the training accuracy and validation accuracy when training the proposed deep CNN model on mini batch size of 16, 32, and 48 with 0.0001, 0.001, and 0.01 learning rates.


![Training of proposed CNN model on various batches and learning rates](https://github.com/MadhuSainani/Potato-disease-classification-by-analysing-plant-leaves-using-Convolutional-Neural-Networks/blob/main/Training%20of%20proposed%20CNN%20model%20on%20various%20batches%20and%20learning%20rates.png)

![Graphical representation of validation accuracy at different batch size and learning rates](https://github.com/MadhuSainani/Potato-disease-classification-by-analysing-plant-leaves-using-Convolutional-Neural-Networks/blob/main/Batch%20Size%20and%20Learning%20rate.png)





  


