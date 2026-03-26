# Phase 1: Building a Custom Tokenizer from Scratch for LLMs

---

## 📌 Overview

This module implements a **basic tokenizer pipeline from scratch**, a foundational component in building Large Language Models (LLMs).  

It converts raw text into **numerical token IDs** and reconstructs text back from those IDs. The implementation evolves from a simple tokenizer to a more robust version handling **unknown tokens** and **special tokens**.

---

## ⚙️ Technical Logic

### 🔹 Text Preprocessing

- Uses **regular expressions (`re.split`)** to split text into tokens:

(\W|_)

→ splits on non-alphanumeric characters and underscores  

- Removes empty/whitespace tokens:
```python
[item.strip() for item in preprocessed if item.strip()]

Vocabulary Creation

Extracts unique tokens:

set(preprocessed)

Sorts tokens for consistency:

sorted(set(preprocessed))

Maps tokens to integers:

vocab = {token: integer for integer, token in enumerate(all_words)}


🔹 Vocabulary Creation
Handling unknown tokens
Special tokens for sequence boundaries

🔹 Tokenizer V1 (Basic)
Encode:
Splits text → maps tokens → IDs
Assumes all tokens exist in vocabulary
Decode:

Converts IDs back to tokens:

" ".join([...])

⚠️ Limitation:

Fails if a token is not present in the vocabulary
🔹 Tokenizer V2 (Improved)
Enhancements:
Introduces special tokens:
<|unk|> → Unknown token
<|endoftext|> → Sequence separator
Encode Logic:

Replaces unseen tokens:

item if item in vocab else "<|unk|>"
Decode Logic:
Converts IDs → tokens
Attempts to reconstruct structure using regex split
🔹 Key Concepts Implemented
Tokenization using regex
Vocabulary mapping (token ↔ ID)
Handling unknown tokens
Special tokens for sequence boundaries

---

