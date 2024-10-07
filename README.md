# CLIP from Scratch on MNIST Dataset

This repository contains an implementation of CLIP (Contrastive Language-Image Pre-training) from scratch, tailored for the MNIST dataset. The goal is to demonstrate how CLIP can be applied to a simple dataset like MNIST.

## Introduction

CLIP is a powerful model that learns visual concepts from natural language supervision. While it's typically applied to large-scale datasets, this project implements CLIP from scratch on the Fashion MNIST dataset to illustrate the core concepts.

Fashion MNIST is a dataset of 70,000 grayscale images of clothing items spanning 10 categories, such as T-shirts, trousers, and sneakers. Each image is 28x28 pixels in size. Designed as a direct drop-in replacement for the original MNIST dataset of handwritten digits, Fashion MNIST provides a more challenging classification task due to its increased complexity and variability, making it ideal for benchmarking machine learning algorithms in computer vision.

## Model Architecture

The CLIP model consists of two main components:

1. **Image Encoder**: A neural network that encodes images into a fixed-size embedding vector.
2. **Text Encoder**: A neural network that encodes text descriptions into a fixed-size embedding vector.

The model learns to align these embeddings in a shared space using a contrastive loss function.

### Image Encoder
For the image encoder, we use a vision transformer (ViT). 

### Text Encoder
For the text encoder, we use the regular transformer with positional encoding. 


### Contrastive Loss

We use a symmetric cross-entropy loss that encourages the model to assign high similarity scores to matching image-text pairs and low scores to non-matching pairs.

The script includes:

- Loading the Fashion MNIST dataset with appropriate transformations.
- Initializing the image and text encoders.
- Defining the contrastive loss function.
- Training the model over several epochs.
- Saving the trained model checkpoints.
- Evaluating the model on test dataset.

# Refrences
- [CLIP paper](https://arxiv.org/abs/2103.00020)
- [Building CLIP from scratch](https://medium.com/correll-lab/building-clip-from-scratch-68f6e42d35f4)
- [ViT paper](https://arxiv.org/abs/2010.11929)
