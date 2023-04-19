# Simple-VIT

This repository demonstrates how to use a pre-trained Vision Transformer (ViT) model for image classification using the timm library. The provided code includes steps to preprocess an input image, perform inference using a pre-trained model, and visualize some internal workings of the model, such as the attention mechanism and classification logits.

## Features
- Utilizes the pre-trained vit_base_patch16_224 model from the TIMM library.
- Applies image preprocessing techniques, including resizing and normalization.
- Extracts and visualizes image patches and position embeddings to better understand the model's inner workings.
- Employs multi-head self-attention mechanism within the transformer architecture to process image patches and extract relevant features.
- Visualizes the attention matrix to reveal relationships between different patches in the image.

## Steps
1. Loads the pre-trained Vision Transformer model.
2. Sets up the image transformation pipeline to preprocess the input image.
3. Downloads and sets up ImageNet class labels.
4. Downloads and preprocesses a sample image (hammer.png).
5. Performs inference on the sample image using the Vision Transformer model and prints the predicted class.
6. Visualizes the similarities between positional embeddings.
7. Computes and prints the shape of various intermediate tensors throughout the model, such as patch embeddings, positional embeddings, and transformer   input/output.
8. Analyzes the attention mechanism in the first Transformer block.
9. Computes and visualizes the attention matrix.
10. Applies the classification head to the transformer output and plots the resulting logits.
11. Prints the final classification result with the predicted class ID and label name.

  
