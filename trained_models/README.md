# Trained Models 
Purpose: Training models on CIFAR-10 and CIFAR-100 for our research

### CIFAR-10 
  | Model        | Accuracy (Train 1) | Accuracy (Train 2) | 
  | ------------ | ------------------ | ------------------ |
  | ResNet 18    | 91.73%             | 94.79%     | 
  | ResNet 34    | **92.19%**         | 94.77%     | 
  | ResNet 50    | 90.66%             | 95.30%     | 
  | ResNet 101   | 89.94%             | 94.99%     | 
  | ResNet 152   | 90.50%             | 94.60%     | 
  | DenseNet 121 | 91.75%             | 95.06%     | 
  | DenseNet 161 | 92.15%             | **95.43%** | 
  | DenseNet 169 | 92.06%             | 95.10%     | 
  | DenseNet 201 | 91.70%             | 95.17%     | 
  | VGG 11       | 89.03%             | 91.94%     |
  | VGG 13       | 90.61%             | 93.70%     | 
  | VGG 16       | 90.95%             | 93.30%     | 
  | VGG 19       | 91.23%             | 93.18%     | 
  | MobileNet V2 | 88.54%             | 94.20%     | 
  | GoogLeNet    | 89.95%             | 95.01%     | 
  | DLA          | 91.42%             | 94.64%     |  
  | DPN 26       | 88.33%             | 94.30%     | 
  | Inception V3 | 91.23%             | 94.77%     | 
  | Xception     | 88.10%             | 93.49%     | 
  
  Training parameters 
  | Parameter     | Value (Train 1) | Value (Train 2) | 
  | ------------- | --------------- | --------------- | 
  | epochs        | 200             | 200             | 
  | batch size    | 128             | 128             | 
  | learning rate | 0.001           | **0.01**        | 
  | image size    | 32x32           | 32x32           |  
  
  ### The CIFAR-10 Dataset: 
  
  The CIFAR-10 dataset consists of 60000 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images.
  
  ---
  ### CIFAR-100  
  
  | Model        | Accuracy (Train 1) |
  | ------------ | ------------------ | 
  | ResNet 18    | 75.94%   |
  | ResNet 34    | 76.72%   | 
  | ResNet 50    | 76.96%   |
  | ResNet 101   | 76.22%   | 
  | ResNet 152   | 74.88%   |
  | VGG 11       | 71.08%   | 
  | VGG 13       | 73.50%   | 
  | VGG 16       | 72.86%   | 
  | VGG 19       | 71.84%   | 
  | DenseNet 121 | 77.54%   |
  | DenseNet 161 | 79.05%   | 
  | DenseNet 169 | 78.67%   | 
  | DenseNet 201 | 78.63%   | 
  | MibileNet V2 | 69.44%   | 
  | Xception     | 74.67%   | 
  | Inception V3 | 77.12%   | 
  
  
  Training parameters 
  | Parameter     | Value (Train 1) | 
  | ------------- | --------------- | 
  | epochs        | 200             | 
  | batch size    | 128             | 
  | learning rate | 0.01            | 
  | image size    | 32x32           | 
  | device        | Tesla V100-SXM2-32GB | 
  
