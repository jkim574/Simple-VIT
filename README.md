# Simple-VIT

This repository contains a simple implementation of a Vision Transformer (ViT) model for image classification using PyTorch and the TIMM library. The project demonstrates fine-tuning a pre-trained ViT model, image preprocessing, patch extraction, position embedding visualization, and end-to-end inference.

## Features
- Utilizes the pre-trained vit_base_patch16_224 model from the TIMM library.
- Applies image preprocessing techniques, including resizing and normalization.
- Extracts and visualizes image patches and position embeddings to better understand the model's inner workings.
- Employs multi-head self-attention mechanism within the transformer architecture to process image patches and extract relevant features.
- Visualizes the attention matrix to reveal relationships between different patches in the image.
