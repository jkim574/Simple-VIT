# Simple-VIT

This repository contains a simple implementation of a Vision Transformer (ViT) model for image classification using PyTorch and the TIMM library. The project demonstrates fine-tuning a pre-trained ViT model, image preprocessing, patch extraction, position embedding visualization, and end-to-end inference.

## Features
- Utilizes the pre-trained vit_base_patch16_224 model from the TIMM library.
- Applies image preprocessing techniques, including resizing and normalization.
- Extracts and visualizes image patches and position embeddings to better understand the model's inner workings.
- Employs multi-head self-attention mechanism within the transformer architecture to process image patches and extract relevant features.
- Visualizes the attention matrix to reveal relationships between different patches in the image.

## Steps
1. Split Image into Patches
  - The input image is split into N patches (N = 14 x 14 for ViT-Base) and converted to D=768 embedding vectors by learnable 2D convolution
2. Add Position Embeddings
  - To make patches position-aware, learnable 'position embedding' vectors are added to the patch embedding vectors. The position embedding vectors learn distance within the image thus neighboring ones have high similarity.
3. Transformer Encoder
  - N (=197) embedded vectors are fed to the L (=12) series encoders.
  - The vectors are divided into query, key and value after expanded by an fc layer.
  - q, k and v are further divided into H (=12) and fed to the parallel attention heads.
  - Outputs from attention heads are concatenated to form the vectors whose shape is the same as the encoder input.
  - The vectors go through an fc, a layer norm and an MLP block that has two fc layers.
