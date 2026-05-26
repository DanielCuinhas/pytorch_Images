# PyTorch Image Classification & Generation

A comprehensive learning repository exploring image processing techniques using PyTorch, featuring hands-on implementations of both **classification** and **generation** models.

## 📋 Table of Contents

- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Classification Models](#classification-models)
- [Image Generation Models](#image-generation-models)
- [Requirements](#requirements)
- [Getting Started](#getting-started)
- [Notebooks Guide](#notebooks-guide)
- [Learning Outcomes](#learning-outcomes)

## Overview

This repository serves as a learning resource for understanding and implementing deep learning models for image processing. It contains interactive Jupyter notebooks that demonstrate the progression from basic neural networks (MLP) to advanced convolutional architectures (AlexNet) and modern generative models (DCGAN).

The project covers:
- **Image Classification**: Building models from scratch and fine-tuning pre-trained networks
- **Image Generation**: Implementing GANs to generate synthetic images
- **Dataset Handling**: Working with MNIST and CIFAR-10 datasets
- **Model Training & Optimization**: Learning rate selection, training loops, and model evaluation

## Repository Structure

```
pytorch_Images/
├── Classification/          # Image classification models
│   ├── 1_MLP_MNIST.ipynb               # Multi-Layer Perceptron on MNIST
│   ├── 2_LeNet_MNIST.ipynb             # Convolutional LeNet on MNIST
│   ├── 3_AlexNet_scratch_CIFAR.ipynb   # AlexNet architecture from scratch on CIFAR-10
│   └── 4_Pretrained_models(tests).ipynb # Transfer learning with pre-trained models
│
├── Generation/              # Image generation models
│   ├── DCGAN.ipynb                     # Deep Convolutional GAN
│   └── README                          # DCGAN reference notes
│
└── README.md               # This file
```

## Classification Models

### 1. **MLP on MNIST** (`1_MLP_MNIST.ipynb`)
**Objective**: Implement a basic Multi-Layer Perceptron for handwritten digit classification

**Key Concepts**:
- Flattening image data for dense network input
- Building fully connected neural networks
- Training and evaluating on MNIST dataset (60,000 training, 10,000 test images)
- Baseline performance metrics

**Architecture**: Simple feedforward network with multiple hidden layers

---

### 2. **LeNet on MNIST** (`2_LeNet_MNIST.ipynb`)
**Objective**: Implement the classic LeNet-5 convolutional architecture

**Key Concepts**:
- Convolutional layers for feature extraction
- Pooling operations for dimensionality reduction
- Learning rate selection using cyclical learning rate finder
- Optimization techniques (learning rate scheduling)

**Architecture**: Convolutional → ReLU → MaxPool → Dense layers

**Highlights**:
- Demonstrates learning rate selection methodology
- Shows how to interpret learning rate curves
- Achieves better performance than MLP due to spatial feature learning

---

### 3. **AlexNet on CIFAR-10** (`3_AlexNet_scratch_CIFAR.ipynb`)
**Objective**: Build AlexNet architecture from scratch and train on CIFAR-10

**Key Concepts**:
- Implementing a deeper convolutional architecture
- Training on color images (3-channel RGB)
- Handling more complex dataset (10 classes vs 10 digits)
- Data augmentation techniques
- Training complex models with proper regularization

**Architecture**: AlexNet - 8 layers (5 convolutional + 3 fully connected)

**Challenges Addressed**:
- Dealing with the complexity of CIFAR-10 dataset
- Computational requirements of deeper networks
- Generalization techniques to prevent overfitting

---

### 4. **Transfer Learning - Pre-trained Models** (`4_Pretrained_models(tests).ipynb`)
**Objective**: Leverage pre-trained models for faster and efficient classification

**Key Concepts**:
- Transfer learning and fine-tuning
- Using models pre-trained on ImageNet
- Adapting models to custom classification tasks
- Comparison of different pre-trained architectures
- Leveraging learned features for improved performance

**Techniques Covered**:
- Feature extraction using pre-trained backbones
- Fine-tuning vs. feature freezing strategies
- Efficient training with transfer learning

---

## Image Generation Models

### **DCGAN** (`Generation/DCGAN.ipynb`)
**Objective**: Implement Deep Convolutional Generative Adversarial Network

**Key Concepts**:
- Generative Adversarial Networks (GANs) architecture
- Generator and Discriminator networks
- Adversarial training process
- Loss functions and training stability
- Generating synthetic images from random noise

**Architecture**:
- **Generator**: Transposed convolutions to upsample noise to images
- **Discriminator**: Standard convolutional network for classification

**Highlights**:
- Follows official PyTorch DCGAN tutorial
- Demonstrates unsupervised learning for image generation
- Includes training visualization and generated sample analysis

---

## Requirements

```
torch>=1.9.0
torchvision>=0.10.0
numpy>=1.19.0
matplotlib>=3.3.0
jupyter>=1.0.0
```

Install dependencies:
```bash
pip install torch torchvision numpy matplotlib jupyter
```

**Note**: For GPU acceleration, install CUDA-enabled PyTorch version from [pytorch.org](https://pytorch.org)

## Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/DanielCuinhas/pytorch_Images.git
cd pytorch_Images
```

### 2. Create Virtual Environment (Recommended)
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt  # Or install manually from Requirements section
```

### 4. Launch Jupyter
```bash
jupyter notebook
```

### 5. Start Learning
- Begin with Classification notebooks in order (1 → 2 → 3 → 4)
- Explore Generation models after understanding classification
- Execute cells step-by-step and experiment with modifications

## Notebooks Guide

| Notebook | Dataset | Architecture | Complexity | Est. Time |
|----------|---------|--------------|-----------|-----------|
| 1_MLP_MNIST | MNIST | MLP | ⭐ Beginner | 5-10 min |
| 2_LeNet_MNIST | MNIST | LeNet-5 | ⭐⭐ Easy | 10-20 min |
| 3_AlexNet_scratch_CIFAR | CIFAR-10 | AlexNet | ⭐⭐⭐ Intermediate | 30-60 min |
| 4_Pretrained_models | ImageNet-trained | Various | ⭐⭐ Easy | 10-30 min |
| DCGAN | Custom/MNIST | DCGAN | ⭐⭐⭐ Intermediate | 20-40 min |

---

## Learning Outcomes

After working through this repository, you will understand:

### Classification
✅ How to build neural networks from scratch in PyTorch  
✅ Difference between fully connected and convolutional architectures  
✅ Data preprocessing and loading using DataLoaders  
✅ Training loops, loss functions, and optimization  
✅ Learning rate selection and scheduling  
✅ Transfer learning and fine-tuning strategies  
✅ Model evaluation metrics and interpretation  

### Generation
✅ Generative Adversarial Networks (GANs) fundamentals  
✅ Generator and Discriminator design principles  
✅ Adversarial training dynamics  
✅ Loss functions for generative models  
✅ Generating synthetic images from random noise  

### PyTorch Skills
✅ Building custom dataset classes  
✅ Creating and training neural network models  
✅ Working with GPU acceleration (CUDA)  
✅ Debugging training issues  
✅ Visualizing training progress and results  

---

## Recommended Learning Path

```
Start Here
    ↓
1_MLP_MNIST (Understand basics)
    ↓
2_LeNet_MNIST (Learn CNNs)
    ↓
3_AlexNet_scratch_CIFAR (Build deeper networks)
    ↓
4_Pretrained_models (Transfer learning)
    ↓
DCGAN (Generative models)
    ↓
Experiment & Extend!
```

---

## Key Takeaways

- **Start Simple, Scale Up**: Progress from MLP to LeNet to AlexNet teaches architectural evolution
- **Dataset Matters**: Compare MNIST (simple) vs CIFAR-10 (complex) to understand model requirements
- **Transfer Learning Works**: Pre-trained models provide excellent starting points
- **GANs Are Powerful**: Generative models open new possibilities beyond classification

---

## Tips for Learning

1. **Execute cells sequentially** - Understand each step before moving forward
2. **Modify and experiment** - Change hyperparameters and observe effects
3. **Monitor visualizations** - Loss curves and sample outputs reveal training dynamics
4. **Use GPU when possible** - Significantly speeds up training (especially AlexNet and DCGAN)
5. **Read inline comments** - Notebooks contain explanations for each operation

---

## References

- [PyTorch Official Tutorials](https://pytorch.org/tutorials/)
- [DCGAN Paper](https://arxiv.org/abs/1511.06434)
- [LeNet Architecture](http://yann.lecun.com/exdb/lenet/)
- [AlexNet Paper](https://papers.nips.cc/paper/2012/hash/c399862d3b9d6b76c8436e924a68c45b-Abstract.html)
- [Transfer Learning in PyTorch](https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html)

---

## License

This repository is open for learning and educational purposes.

---

**Author**: Daniel Cuinhas  
**Repository**: [pytorch_Images](https://github.com/DanielCuinhas/pytorch_Images)  
**Last Updated**: 2026-05-26
