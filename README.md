# Transformer From Scratch (English → French)

## Overview

This project implements a **Transformer-based encoder–decoder model from scratch using TensorFlow/Keras** for **English-to-French machine translation**.  
All core components—attention, masking, encoder–decoder interaction, and inference—are explicitly defined without using high-level Transformer APIs.

---

## Dataset

- **English–French parallel corpus (`fra-eng`)**
- Loaded using TensorFlow utilities
- Preprocessing includes:
  - Tokenization and text vectorization
  - Fixed-length padding
  - `[start]` and `[end]` tokens for decoder sequences

---

## Model Architecture

- Token embeddings with positional encoding  
- Multi-head self-attention  
- Encoder–decoder attention  
- Feed-forward networks  
- Residual connections and normalization  
- Vocabulary projection layer  

---

## Training

- Trained for **20 epochs**
- **1828 steps per epoch**
- Masked loss used for optimization
- Masked accuracy tracked during training

---

## Results

- Training converges steadily across epochs
- Validation metrics remain stable after early training
- Final masked accuracy:
  - **Training:** ~74%
  - **Validation:** ~64%
- Model generates coherent French translations using greedy decoding

---

## Inference

- Custom autoregressive decoding function
- Decoding starts with `[start]` token
- Tokens generated step-by-step
- Decoding stops when `[end]` token is produced or sequence limit is reached

---

## Usage

Run the notebook end-to-end:

```bash
jupyter notebook transformer_from_scratch.ipynb
