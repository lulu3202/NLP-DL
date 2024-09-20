# Simplified Concepts in NLP + Deep Learning

## 1. Word Embedding: Converting Text to Numbers using Neural Networks
- **Intelligent 'Text to Number' Conversion**: Unlike traditional methods (e.g., Count Vectorizer, TF-IDF, One-hot encoding), word embeddings use neural networks to convert words into meaningful numerical vectors.
- **How It Works**: Words are converted to vectors using neural networks with feedforward and backpropagation. The goal is to place similar words closer together in vector space.
- **Pretrained Embedding Algorithms**: Common algorithms include Word2Vec, FastText, and Byte Pair Encoding.

### Word2Vec - CBOW (Continuous Bag of Words)
- **Data Preparation**: Uses supervised learning to split input (context words) and output (target word).
- **Training Process**: A sentence is provided with context words as input and the target word as output (e.g., “She is a great dancer” → ‘dancer’ is the output, while the rest are context words).
- **Key Elements**: [Context Word, Target Word, Window Size]. Uses 1-hot encoding to combine input, and outputs similarity in values like 0.4, 0.5.

### Word2Vec - Skip-Gram
- **Reciprocal of CBOW**: Here, the input is one word, and the output is the surrounding context words.
- **Comparison**: CBOW is more commonly used than Skip-Gram for word embeddings.

---

## 2. Long Short Term Memory (LSTM)
- **Background**: LSTM is an evolution of RNNs (Recurrent Neural Networks) designed to solve issues like exploding and vanishing gradients when dealing with sequential data.
  
### Key LSTM Concepts:
- **Perceptron Mechanism**: Each input is multiplied by weights (learning capacity), and passed through activation functions like ReLU to decide whether information should be retained.
- **Overcoming RNN Issues**:
  - **Exploding Gradient**: Happens when the weights grow too large.
  - **Vanishing Gradient**: Happens when the weights are too small, causing the model to struggle with learning.
  
### LSTM Architecture:
- **Sigmoid Function**: Output ranges between 0 and 1. For positive values, the output gets closer to 1, and for negative values, it approaches 0.
- **Tanh Function**: Output ranges between -1 and 1, capturing the positive and negative ranges more efficiently.
  
#### LSTM Block Diagram:
- **Forget Gate**: Determines how much long-term information to retain.
- **Input Gate**: Updates cell state based on new input.
- **Output Gate**: Decides what part of the current cell state to output.
- **No Weights & Biases for Long-term Memory**: Only short-term memory uses them.

---

## 3. Sequence to Sequence (Seq2Seq) with LSTM
- **Word Embedding as a Foundation**: Each word is converted into high-dimensional vectors.
- **Tokens**: `<SOS>` (start of sentence) and `<EOS>` (end of sentence) are used to denote the start and end.
  
### Seq2Seq Architecture:
- **Encoder LSTM**: Takes the input sequence and encodes it into a context vector.
- **Decoder LSTM**: Uses the context vector to produce the output sequence, one word at a time.
- **Teacher Forcing**: Even when the model predicts wrong, the correct input is fed back into the decoder to guide learning.
  
### Applications:
- **Machine Translation**: Translating sentences from one language to another while maintaining sequence (e.g., “How are you?” → “¿Cómo estás?”).
- **Text Summarization**: Summarizing a large paragraph into a shorter version.

---

## 4. Transformer Model
Check README file under transformer folder for a detailed writeup

---

