# 🚀 Phase 1: Tokenization & Byte Pair Encoding (BPE)

## 📌 Overview
This module focuses on the fundamental step of any Large Language Model (LLM): converting raw text into numerical representations. It demonstrates how Byte Pair Encoding (BPE) is used to transform text into tokens and reconstruct it back, ensuring efficient and reversible processing. This forms the backbone for how models understand and generate language.

---

## ⚙️ Technical Logic

### 🔹 Tokenization
- Text is broken down into smaller units called tokens  
- Tokens are not always full words — they are often subword units  

---

### 🔹 Byte Pair Encoding (BPE)
- Starts with individual characters  
- Iteratively merges the most frequent character pairs  
- Builds a vocabulary of commonly occurring subword units  

---

### 🔹 Encoding (Text → Tokens)
- Input text is converted into a sequence of integers  
- Each integer represents a token from the vocabulary  
- Special tokens (like end-of-text markers) are handled explicitly  

---

### 🔹 Decoding (Tokens → Text)
- Token sequences are converted back into readable text  
- Ensures a lossless and reversible transformation  

---

### 🔹 Handling Unknown Words
- Rare or unseen words are broken into smaller known subword units  
- Prevents vocabulary explosion and improves generalization  

---

## 🧠 Why This Matters
- LLMs do not process raw text — they process numerical tokens  
- Efficient tokenization directly impacts model performance  
- BPE enables handling of unseen words without errors  
- Forms the input layer for embeddings and transformer models  

---

## ▶️ How to Run

### 🔹 Requirements
- Python environment  
- Jupyter Notebook or any Python IDE  

---

### 🔹 Steps
1. Install required libraries  
2. Open the notebook file  
3. Execute all cells sequentially  

---

## 📊 Expected Outcomes
- Text converted into token IDs  
- Tokens converted back into original text  
- Understanding of how unknown words are handled  

---

## 🎯 Key Takeaways
- Tokenization is the first step in building LLMs  
- BPE balances vocabulary size and flexibility  
- Subword representations improve language understanding  
- Reversible encoding is critical for model reliability  

---



# Data Sampling for Language Model Training

## Overview
This project focuses on preparing textual data for training a language model by converting raw text into tokenized sequences and structured input-target pairs. It demonstrates how to transform continuous text into meaningful training samples using sliding window techniques.

## Technical Logic
The workflow begins by loading raw text data and converting it into tokens using a tokenizer compatible with GPT-style models. These tokens are then segmented into fixed-length sequences using a sliding window approach.

Each sequence is split into:
- Input tokens (context)
- Target tokens (next-token prediction)

A custom dataset is built to store these input-target pairs, and a data loader is used to efficiently batch and feed them into a model during training.

## Why This Matters
Language models do not understand raw text directly—they learn patterns through token relationships. This step is critical because it defines how the model "sees" language, enabling it to learn context, sequence dependencies, and next-token prediction effectively.

## How to Run
- Prepare a raw text file as input data
- Load the text into memory
- Tokenize the text using a compatible tokenizer
- Create dataset sequences using a fixed context length and stride
- Initialize a data loader to generate batches
- Iterate through batches to verify inputs and targets

## Expected Outcomes
- Tokenized representation of raw text
- Structured input-target pairs for training
- Efficient batching of sequences
- Clear understanding of how context windows are formed

## Key Takeaways
- Tokenization is the foundation of language modeling
- Context windows define how much information the model sees at once
- Sliding windows help maximize data utilization
- Input-target shifting enables next-token prediction learning
- DataLoader improves training efficiency through batching

## Next Steps
- Build a simple neural language model using these batches
- Implement embedding layers for token representation
- Introduce attention mechanisms
- Scale to transformer-based architectures

## Position in LLM Journey
This project sits at the early data preparation stage of LLM development, right after tokenization and before model architecture implementation. It bridges raw text processing and model training, forming a critical foundation for building GPT-like models.
