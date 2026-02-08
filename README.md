# SimCLR: Self-Supervised Visual Representation Learning

This project implements **SimCLR** from scratch using PyTorch to study self-supervised visual representation learning.  
The model learns meaningful image representations **without using labels** by contrasting different augmented views of the same image.

## Method
- Backbone: ResNet-18 encoder
- Projection head: 2-layer MLP
- Training objective: NT-Xent (contrastive) loss
- Dataset: CIFAR-10 (labels unused during pretraining)
- 
## Architecture
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/fd904748-476f-4cee-9bca-38acf0a3ba92" />

## Evaluation
Learned representations are evaluated using a **linear probing protocol**:
- Encoder is frozen after self-supervised training
- A linear classifier is trained on top of extracted features
- Performance reflects the quality of learned representations

## Results
- Linear evaluation accuracy: ~25%
- Demonstrates non-trivial semantic representations learned without supervision

## Key Concepts
- Self-supervised learning
- Contrastive learning
- Representation learning
- Linear evaluation protocol

## Tools
- PyTorch
- torchvision
- Google Colab
