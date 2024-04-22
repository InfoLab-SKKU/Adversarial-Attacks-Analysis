# Unmasking the Vulnerabilities of Deep Learning Models: A Multi-Dimensional Analysis of Adversarial Attacks and Defenses

### Purpose: 
* Experiment 1: Correlation between model complexity and robustness 
* Experiment 2: Correlation between model diversity and robustness
* Experiment 3: Black-box attacks across different dataset 
* Experiment 4: Defenses against black-box attacks 


  ### Attacks 
  | Attack       | Attack Type | Parameters | 
  | ------------ | ----------- | ---------- | 
  | [SimBA](https://arxiv.org/pdf/1905.07121.pdf) | Decision Boundary Approximation  | epsilon = 0.05, max_iter=5000 | 
  | [HopSkipJump](https://arxiv.org/pdf/1904.02144.pdf) | Gradient Approximation  | max_iter=20 | 
  | [BoundaryAttack](https://arxiv.org/pdf/1712.04248.pdf) | Search-based | epsilon=0.01, max_iter=1000 |

  
### ImageNet - Models with different complexity  
  | Model        | Top 1% Accuracy | Top 5% Accuracy | Model Size | Total Params | 
  | ------------ | --------------- | --------------- | ---------- | ------------ | 
  | ResNet 18    | 69.758          | 89.078          | 44.7 MB    | 11,689,512   | 
  | ResNet 34    | 71.314          | 91.420          | 83.3 MB    | 21,797,672   | 
  | ResNet 50    | 76.130          | 92.862          | 97.8 MB    | 25,557,032   | 
  | ResNet 101   | 77.374          | 93.546          | 171 MB     | 44,549,160   |
  | ResNet 152   | 78.312          | 94.046          | 230 MB     | 60,192,808   | 
  | VGG 11       | 69.020          | 88.628          | 507 MB     | 132,863,336  |  
  | VGG 13       | 69.928          | 89.246          | 508 MB     | 133,047,848  | 
  | VGG 16       | 71.592          | 90.382          | 528 MB     | 138,357,544  | 
  | VGG 19       | 72.376          | 90.876          | 548 MB     | 143,667,240  | 
  | DenseNet 121 | 74.434          | 91.972          | 30.8 MB    | 7,978,856    |
  | DenseNet 169 | 75.600          | 92.806          | 54.7 MB    | **14,149,480**   |
  | DenseNet 201 | **76.896**      | **93.370**      | **77.4 MB**| **20,013,928**   | 
  
  #### ImageNet - Diverse Models  
  | Model        | Top 1% Accuracy | Top 5% Accuracy | Model Size | Total Params | Source    | 
  | ------------ | --------------- | --------------- | ---------- | ------------ | --------- | 
  | VGG 19       | 72.376          | 90.876          | 548 MB     | 143,667,240  | [PyTorch](https://pytorch.org/vision/stable/models.html) | 
  | ResNet 152   | 78.312          | 94.046          | 230 MB     | 60,192,808   | [PyTorch](https://pytorch.org/vision/stable/models.html) | 
  | DenseNet 161 | 77.138          | 93.560          | 110 MB     | 28,681,000   | [PyTorch](https://pytorch.org/vision/stable/models.html) | 
  | Inception V3 | 77.294          | 93.450          | 104 MB     | 27,161,264   | [PyTorch](https://pytorch.org/vision/stable/models.html) |   
  | Xception     | 78.888          | 94.292          | 87.4 MB    | 22,855,952   | [pretrainedmodels](https://github.com/Cadene/pretrained-models.pytorch) | 
  | GoogLeNet    | 69.778          | 89.530          | 49.7 MB    | 6,624,904    | [PyTorch](https://pytorch.org/vision/stable/models.html) | 
  | MobileNet V2 | 71.878          | 90.286          | 13.6 MB    | 3,504,872    | [PyTorch](https://pytorch.org/vision/stable/models.html) | 

  
  * VGG: [Very Deep Convolutional Networks for Large-Scale Image Recognition](https://arxiv.org/abs/1409.1556v6)
  * ResNet: [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385v1) 
  * DenseNet: [Densely Connected Convolutional Networks](https://arxiv.org/abs/1608.06993v5)   
  * Xception: [Xception: Deep Learning with Depthwise Separable Convolutions](https://arxiv.org/abs/1610.02357)
  * Inception: [Rethinking the Inception Architecture for Computer Vision](https://arxiv.org/abs/1512.00567v3)
  * GoogLeNet: [Going Deeper with Convolutions](https://arxiv.org/abs/1409.4842)
  * MobileNetV2: [MobileNetV2: Inverted Residuals and Linear Bottlenecks](https://arxiv.org/abs/1801.04381) 

  #### Defenses   
  | Defense Technique    | Parameter | Source    | 
  | -------------------- | --------- | --------- | 
  | JPEG Filter          | quality=75  | [AdverTorch](https://github.com/BorealisAI/advertorch) |
  | Median Smoothing     | kernel_size=2 (weak) | [AdverTorch](https://github.com/BorealisAI/advertorch) |
  | Bits Squeezing       | bit_depth=4 (weak) | [AdverTorch](https://github.com/BorealisAI/advertorch) | 


  #### Device Information 
  | Device           | Device Name                 | 
  | -----------------| ----------------------------|
  | GPU              | GeForce RTX 2080 Ti (12 GB) | 
  
  #### Metrics 
  | Metrics                                    | Description           | 
  | ------------------------------------------ | --------------------- |
  | Attack Success Rate                        | number of successful attacks | 
  | Misclassification confidence               | confidence for misclassified image after attack    | 
  | Structural Similarity (SSIM) - Noise Rate  | noise rate = 1 − SSIM (Structural Similarity)      | 
  | Attack Time                                | average attack time for each image (in secs)       | 
  | L1 distance                                | difference between benign and adversarial examples |

 ### Examples 
  <img src="images/hopskipjump_example.png" width="80%" height="80%"> 

### Defenses  
  
  ### Example 
  <img src="images/defense_examples.png" width="75%" height="75%"> 
