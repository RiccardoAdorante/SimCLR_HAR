# Human Activity Recognition with Self-Supervised Learning (SimCLR)

This project leverages self-supervised learning to perform human activity recognition (HAR) using the MobiAct dataset. The approach involves pretraining a neural network using SimCLR, a contrastive learning framework, and subsequently fine-tuning the network with a supervised classifier using a smaller labeled dataset.
Human Activity Recognition (HAR) has a wide range of applications, including health monitoring, fitness tracking, and human-computer interaction. Traditional supervised learning approaches for HAR often require large labeled datasets, which can be expensive and time-consuming to collect.
This project adopts a self-supervised learning approach using SimCLR, which enables the network to learn meaningful representations from unlabeled data. Once pretrained, the network is fine-tuned with a smaller labeled dataset to achieve accurate classification of human activities.

## Dataset
The MobiAct dataset was used in this project. This dataset contains motion sensor data collected from smartphones during various human activities, such as walking, running, sitting, and more.

#### Key characteristics of the dataset:

- Includes diverse human activities.
- Collected using accelerometers and gyroscopes.
- Suitable for HAR tasks in both supervised and self-supervised settings.
## Methodology
This project is divided into two main phases:

### 1. Self-Supervised Pretraining
- The SimCLR framework is employed for pretraining.
- SimCLR learns representations by maximizing agreement between differently augmented views of the same data sample in the latent space.
- Key steps:
  - Data Augmentation: Sensor data is augmented using techniques like cropping, scaling, and noise addition.
  - Contrastive Learning: The network is trained to bring embeddings of augmented views of the same sample closer while pushing apart embeddings of different samples.
### 2. Supervised Fine-Tuning
- After pretraining, a classifier is attached to the pretrained network.
- The combined model is fine-tuned using a smaller labeled subset of the data.
- This step leverages the representations learned during pretraining to achieve robust classification with limited labeled data.
## Results
The self-supervised pretraining approach enabled the network to learn meaningful representations from unlabeled data, significantly improving performance when fine-tuned on a smaller labeled dataset.

#### Key performance metrics:

- Accuracy: 84%
- Precision: 85.7%
- Recall: 84%
- F1-Score: 84.5%
