🧠 GPT-Style Transformer (From Fundamentals)

A learning-focused implementation of a GPT-style Transformer language model, trained on the Tiny Shakespeare dataset, built using PyTorch.
The goal of this project is to understand how Transformers work internally by implementing their core components step by step.

⚠️ This project is not a production-grade GPT.
It is a foundational, educational implementation aimed at gaining architectural and conceptual clarity.

📌 Motivation

Transformers and Large Language Models are often used through high-level APIs, which can hide the underlying mechanics.
As a fresher, implementing a Transformer entirely from scratch is extremely challenging, but this project represents a best-effort attempt to build and understand as much of the architecture as possible.

The focus was on learning:

How attention works

How context is modeled

How individual components interact to produce coherent text

🧩 Project Structure
.
├── bigram.py      
├── gpt.py        
├── input.txt    
└── README.md

📚 Learning Progression
1️⃣ Bigram Language Model (bigram.py)

A minimal language model where each token predicts the next token directly.

Purpose:

Understand tokenization

Learn next-token prediction

Build intuition for language modeling loss

2️⃣ GPT-Style Transformer (gpt.py)

An extension of the bigram model into a simplified Transformer-based architecture.

🏗 Architecture Overview

The Transformer model includes:

Character-level tokenization

Token embedding layer

Positional embedding layer

Masked (causal) self-attention

Multi-head attention

Feed-forward neural networks

Residual connections

Layer normalization

Autoregressive text generation

This closely follows the decoder-only Transformer (GPT-style) design.

⚙️ Training Details

Dataset: Tiny Shakespeare

Model Type: Character-level language model

Loss Function: Cross-entropy loss

Optimizer: AdamW

Training: Autoregressive next-token prediction

Evaluation: Train/validation loss monitoring


🚀 GPU & CUDA Support

Automatic device selection using:

device = 'cuda' if torch.cuda.is_available() else 'cpu'

CUDA-enabled training via Google Colab GPU

The model runs on CPU or GPU depending on availability.

▶️ How to Run
1️⃣ Install dependencies
pip install torch


2️⃣ Prepare dataset

Download the Tiny Shakespeare dataset as input.txt.

3️⃣ Run the bigram model
python bigram.py

4️⃣ Run the Transformer model
python gpt.py


🧪 Output

The model generates Shakespeare-like text character by character after training.

⚠️ Limitations

Small model size

Character-level tokenization (no BPE)

Trained on a small dataset

Not intended for production use

These limitations are intentional and align with the project’s learning-focused goals.

🔮 Future Improvements

Increase model depth and embedding size

Implement better sampling strategies

Add temperature and top-k sampling

Experiment with larger datasets

Implement Byte Pair Encoding (BPE)

👤 Author

Hitesh Kumar
Computer Science Undergraduate
Aspiring AI / ML Engineer
