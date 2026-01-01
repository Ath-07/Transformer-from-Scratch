# 🧠 Transformer From Scratch: English → French

A clean, from-scratch implementation of the **Transformer architecture** for **English-to-French machine translation**, built using **PyTorch**.  
The focus of this project is to **expose the inner workings of attention-based sequence models** by implementing every core component manually.

---

## ✨ Highlights

- End-to-end **Encoder–Decoder Transformer**
- Manual implementation of all architectural blocks
- Trained on a real **English–French parallel dataset**
- Covers preprocessing, training, and inference
- Optimized for **learning and interpretability**

---

## 📘 Dataset

- Parallel English–French sentence pairs  
- Automatically downloaded and extracted  
- Vocabulary created directly from the corpus  
- Special tokens for padding, start, and end of sequence are handled explicitly  

---

## 🏗 Architecture Overview

The model is composed of the following building blocks:

- Token embeddings for source and target languages  
- Sinusoidal positional encoding  
- Multi-head self-attention  
- Decoder-side masked self-attention  
- Encoder–decoder attention  
- Position-wise feed-forward layers  
- Residual connections with layer normalization  
- Final linear projection to vocabulary space  

---

## 🔄 Data Flow

Input Sentence  
→ Embedding + Positional Encoding  
→ Encoder Layers  
→ Decoder Layers (with causal masking)  
→ Token-wise Vocabulary Scores

---

## 🎭 Masking Logic

- Padding tokens are excluded from attention and training  
- Look-ahead masking enforces autoregressive decoding  
- Metrics are computed only on valid (non-padding) tokens  

---

## 🚀 Training Setup

- Teacher forcing during training  
- Padding-aware loss and accuracy computation of about 71%
- Explicit training and validation loops  

---

## 🧰 Tech Stack

- **Python 3**
- **PyTorch**
- **TensorFlow** (dataset handling only)
