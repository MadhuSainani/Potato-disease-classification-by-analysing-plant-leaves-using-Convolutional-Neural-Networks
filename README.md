# Potato Disease Classification by Analysing Plant Leaves using Convolutional Neural Networks
As part of disseration for MSc at Northumbria University, I have worked on this project. Please explore my presentation and code files to delve deeper into the proposed methodolgy, results, analysis, and future recommendations.
Presentation Link: https://docs.google.com/presentation/d/1gvJ8ozz0DUqWvbCvfTa-BeLgDfSSbgIu/edit?usp=sharing&ouid=108050464650727057070&rtpof=true&sd=true

## Problem Statement:
Plant diseases, particularly Early Blight and Late Blight can significantly reduce potato crop yields, leading to higher food costs and shortages. Traditional disease identification methods are costly and require expert intervention. Farmers need more affordable, fast, reliable, and accurate techniques for efficient disease management. Recently, deep learning techniques (CNN) have been used for crop disease classification due to their ability to automatically extract features from images. Pre-trained models like InceptionV3, ResNets, and VGGNet can be fine-tuned for this purpose. However, these models are not specifically designed for disease identification and can lead to precision errors and limited interpretability. Additionally, pre-trained models have complex multi-layer architectures, which can lead to high computational burden and making it challenging to deploy in resource-constraint devices. 
## Aim:
The motivation of this work is to build a customized deep CNN model specifically designed to efficiently classify diseases in potato leaf plants with minimum number of layers, optimized hyper parameters, high accuracy, and less computational burden. The research aims to strike a balance between detection accuracy and computational efficiency, and build a robust and reliable tool to help farmers in managing potato crops.   
## Key Contribution:
- Proposed a 3-layer deep CNN architecture, specifically designed to classify 2 diseases in potato leaves: Potato Early Blight and Potato Late Blight.
- Implemented effective on-the-fly data augmentation techniques to increase the training dataset and avoid class-imbalance.
- Tuned the model with various batch sizes (16, 32, 64) and learning rates (0.0001, 0.001, 0.01) to stabilize performance.
- Replaced multiple fully-connected layers and the flatten layer with a Global Average Pooling (GAP) layer, significantly reducing the number of trainable parameters and computational burden.
- Employed dropout regularization techniques to stimulate ensemble modeling and experimented with various dropout rates (e.g., 0.1, 0.2, 0.3, 0.4, 0.5) to prevent overfitting.
- Achieved balanced test accuracy of 99.11% and an F1-score of 99% on unseen data.
- Compared the proposed model with pre-trained models (InceptionV3, MobileNetV2, MobileNet, ResNet50), outperforming InceptionV3 by 5.6%, surpassing ResNet50 by 35.4%, and matching the accuracy of MobileNet and MobileNetV2.
- Reduced prediction time to 1 second and model size to 109.14 KB, significantly outperforming benchmark models such as InceptionV3 (16 seconds, 83.19 MB), ResNet50 (27 seconds, 90.00 MB), MobileNetV2(5S, 8.63MB).







  


