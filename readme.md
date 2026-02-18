# Advanced Autoencoder Models

This repository contains experimental implementations of advanced autoencoder variants on the Fashion-MNIST dataset.

The goal of this project is to compare different reconstruction strategies and analyze how architectural choices influence performance and training behavior.

---

## Implemented Models

### Sparse Autoencoder
- Dense encoder–decoder structure
- L1 activity regularization applied at latent layer
- Tuned to avoid reconstruction collapse

### Denoising Autoencoder
- Gaussian noise added to inputs (noise factor = 0.35)
- Clean images used as reconstruction targets
- Demonstrates robustness to corrupted inputs

### Dense Deep Autoencoder
- Fully connected encoder–decoder architecture
- Serves as baseline for reconstruction comparison

### CNN-Based Autoencoder
- Convolution + MaxPooling encoder
- Convolution + UpSampling decoder
- Preserves spatial structure
- Achieved best reconstruction performance

---

## Dataset

- Fashion-MNIST (28×28 grayscale images)
- Images normalized to [0,1]
- Training performed in an unsupervised manner

---

## Training Configuration

- Optimizer: Adam
- Loss Function: Mean Squared Error (MSE)
- Epochs: 20
- Batch Size: 256

---

## Performance Summary

| Model                  | Validation MSE |
|------------------------|---------------|
| Sparse Autoencoder     | 0.0230        |
| Denoising Autoencoder  | 0.0142        |
| Dense Deep Autoencoder | 0.00795       |
| CNN Autoencoder        | 0.002915      |

---

## Key Findings

- Sparse autoencoders require careful regularization tuning.
- Denoising autoencoders improve reconstruction robustness.
- CNN autoencoders outperform dense models in reconstruction accuracy.
- CNN models require significantly longer training time per epoch.

---

