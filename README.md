# CNN for Speech Enhancement

A deep learning approach to speech denoising using Convolutional Neural Networks (CNNs). This project trains a model to remove white noise from speech audio by learning the mapping between noisy and clean mel spectrograms.

## Overview

This project implements a neural network-based speech enhancement system that:

1. Takes noisy speech audio as input
2. Converts it to a mel-scaled spectrogram
3. Uses a CNN to predict the clean spectrogram
4. Reconstructs the denoised audio using the Griffin-Lim algorithm

## Data

- **Clean Speech**: [LibriSpeech ASR Corpus](https://www.openslr.org/12) (dev-clean subset)
- **Noise**: Synthetic white Gaussian noise added to clean signals

## Usage

This project was developed in Google Colab. To run:

1. Upload the notebook to Google Colab
2. Mount your Google Drive
3. Run all cells sequentially (the notebook will download LibriSpeech automatically)



## Notebook Structure

The notebook is organized into 11 sections:

1. **Imports** - Required libraries
2. **Datasets** - Data sources and download
3. **Configuration Parameters** - Audio and processing settings
4. **Data Preprocessing** - Creating noisy-clean audio pairs
5. **Mel Spectrogram Computation** - Feature extraction
6. **Visualizing Spectrograms** - Data inspection
7. **Data Preparation for Training** - Train/val/test splits
8. **Model Architecture** - CNN definition
9. **Model Training** - Training loop
10. **Training History Visualization** - Loss and metric plots
11. **Model Evaluation** - Spectrogram metrics (MSE, MAE) and listening