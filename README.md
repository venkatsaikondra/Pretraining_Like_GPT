DAY 1
____________

What is Language Modeling?

Language modeling is the process of a machine learning model learning to predict the next word in a sequence of text, based on the words that came before it.

![img.png](img.png)

We, humans, already have some feeling of "probability" when it comes to natural language. For example, when we talk, usually we understand each other quite well (at least, what's being said). We disambiguate between different options which sound similar without even realizing it!

But how a machine is supposed to understand this? A machine needs a language model, which estimates the probabilities of sentences. If a language model is good, it will assign a larger probability to a correct option.

Examples of language models include GPT-4, BERT, and Llama 3.

GPT{Generative Pretrained Transformer}

the core stages that a model like GPT (Generative Pre-trained Transformer) goes through are

📘 RAW TEXT DATA
      │
      ▼
🧹 1. DATA PREPROCESSING
   - Collect large text corpora (books, web, etc.)
   - Clean, normalize, remove duplicates
      │
      ▼
🔡 2. TOKENIZATION
   - Split text into subword tokens (e.g., BPE)
   - Convert words → numeric IDs
      │
      ▼
🧭 3. EMBEDDING LAYER
   - Token embeddings → represent meaning
   - Positional embeddings → represent order
      │
      ▼
🔁 4. TRANSFORMER BLOCKS (repeated N times)
   ├── Self-Attention (context across tokens)
   ├── Feed-Forward Network (nonlinear mapping)
   ├── Residual Connections + Layer Norm
      │
      ▼
🎯 5. OUTPUT HEAD
   - Linear projection to vocabulary size
   - Softmax → next-token probability
      │
      ▼
📉 6. TRAINING OBJECTIVE
   - Causal Language Modeling (predict next token)
   - Loss = Cross-Entropy between predicted vs actual token
      │
      ▼
⚙️ 7. OPTIMIZATION
   - Optimizer: AdamW
   - Learning rate schedule + gradient clipping
      │
      ▼
💪 8. PRETRAINED MODEL
   - Learns general language patterns
      │
      ▼
🎓 9. FINE-TUNING (optional)
   - Train on specific tasks (e.g., book verdicts)
   - Supervised fine-tuning or RLHF
      │
      ▼
💬 10. INFERENCE
   - Input prompt → model predicts next tokens
   - Generates text autoregressively

COLLECTING DATA

Now I am taking the data as the book "The Verdict"
![img_1.png](img_1.png)

Taking data from kaggle

---------------------------------------------------------------------------------------------------------

Day 2

TOKENIZATION

Byte pair encoder






