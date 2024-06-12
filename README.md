# Potato Disease Classification by Analysing Plant Leaves using Convolutional Neural Networks
As part of disseration for MSc at Northumbria University, I have worked on this project. Please explore my presentation and code files to delve deeper into the proposed methodolgy, results, analysis, and future recommendations.
Presentation Link: https://docs.google.com/presentation/d/1DkCnJGNQ_zmSacotN8w85mcsu8AovZ-4/edit?usp=sharing&ouid=108050464650727057070&rtpof=true&sd=true

## Problem Statement:
Plant diseases, particularly Early Blight and Late Blight can significantly reduce potato crop yields, leading to higher food costs and shortages. Traditional disease identification methods are costly and require expert intervention. Farmers need more affordable, fast, reliable, and accurate techniques for efficient disease management. Recently, deep learning techniques (CNN) have been used for crop disease classification due to their ability to automatically extract features from images. Pre-trained models like InceptionV3, ResNets, and VGGNet can be fine-tuned for this purpose. However, these models are not specifically designed for disease identification and can lead to precision errors and limited interpretability. Additionally, pre-trained models have complex multi-layer architectures, which can lead to high computational burden and making it challenging to deploy in resource-constraint devices. 
## Aim:
The motivation of this work is to build a customized deep CNN model specifically designed to efficiently classify diseases in potato leaf plants with minimum number of layers, optimized hyper parameters, high accuracy, and less computational burden. The research aims to strike a balance between detection accuracy and computational efficiency, and build a robust and reliable tool to help farmers in managing potato crops.   
## Key Contribution:
- A novel lightweight deep CNN model has been developed for detecting Early Blight and Late Blight in potato crops. This customized deep CNN, with 3 convolutional layers, is specifically designed for disease detection in potato leaves. Additionally, the model has been tuned with various batch sizes (16,32,64) and learning rates (0.0001, 0.001, 0.01) to stabilize its performance.
- Multiple fully-connected layers and flatten layer have been replaced by Global Average Pooling (GAP) layer, resulting in significant reduction in number of trainable parameters and computational burden.
- Dropout regularization technique is employed to stimulate ensemble modelling. The model is experimented with various dropout rates (e.g., 0.1, 0.2, 0.3, 0.4, 0.5) to prevent overfitting.
- The model has obtained balanced test accuracy of 99.11% and f1-score of 99% on unseen data. 
- The model has been compared with pre-trained models InceptionV3, MobileNetV2, MobileNet, ResNet50. The proposed model has outperforms InceptionV3 by 5.6%, surpasses ResNet50 by 35.4%, and matches the accuracy of MobileNet and MobileNetV2.
- Enhanced computational efficiency by reducing prediction time to 1 second and model size to 109.14 KB, significantly outperforming larger models such as InceptionV3 (16 seconds, 83.19 MB) and ResNet50 (27 seconds, 90.00 MB).
- Optimized for resource-constrained devices with a model size of only 109.14 KB, making it much smaller and more deployable than MobileNet (12.33 MB) and MobileNetV2 (8.63 MB).







  


