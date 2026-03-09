# Synthetic Tabular Data Generation using GANs

This project demonstrates how to generate synthetic tabular data using a Generative Adversarial Network (GAN) implemented in PyTorch.

## Project Overview

Synthetic data generation is useful for:

- Data privacy protection
- Data augmentation
- Training machine learning models when data is limited

This project trains a GAN to learn the distribution of a tabular dataset and generate new synthetic samples.

## Technologies Used

- Python
- PyTorch
- Pandas
- Scikit-Learn
- NumPy

## Workflow

1. Load dataset using Pandas
2. Preprocess data
   - MinMax scaling for numerical features
   - One-hot encoding for categorical variables
3. Train a GAN model
   - Generator
   - Discriminator
4. Generate synthetic samples
5. Convert synthetic data back to original format

## Model Architecture

Generator:
- Linear layers
- LeakyReLU activation
- Tanh output

Discriminator:
- Linear layers
- LeakyReLU activation
- Sigmoid output

## Results

The trained GAN can generate synthetic tabular records that follow the statistical patterns of the original dataset.

## How to Run

Install dependencies:
