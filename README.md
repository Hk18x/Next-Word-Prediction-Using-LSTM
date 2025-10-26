# 🧠 Next Word Prediction Using LSTM

This project predicts the **next word** in a given sequence of words using a **Long Short-Term Memory (LSTM)** Recurrent Neural Network.  
Next-word prediction is a fundamental Natural Language Processing (NLP) task with applications in **text generation, autocomplete systems, chatbots**, and **language modeling**.

---

## 📁 Dataset

The dataset used is **Shakespeare’s “Hamlet”**, chosen for its rich vocabulary and complex sentence structures.

- `text` → Contains lines from Shakespeare’s *Hamlet*  
- Sequences are generated based on word-level tokenization  
- Each training example consists of an input sequence of words and a target next word  

> Example:  
> Input: “To be or not to”  
> Target: “be”

---

## 🛠 Tech Stack

- Python  
- NumPy, Pandas  
- TensorFlow / Keras  
- Matplotlib  
- NLTK  
- Streamlit *(for optional deployment)*  

---

## ⚙️ Features

- **Word-Level Prediction:** Predicts the next word in a sentence  
- **Two Architectures:** Implemented both **LSTM** and **GRU** versions  
- **Tokenizer:** Converts words into integer sequences  
- **Padded Sequences:** Ensures uniform input length  
- **Next Word Generation Function:** Interactive testing for any text prompt  

---

## 🔧 Preprocessing Steps

1. Loaded Shakespeare’s *Hamlet* text file.  
2. Cleaned and tokenized the text using `Tokenizer`.  
3. Created word sequences for supervised learning.  
4. Applied `pad_sequences` to maintain consistent input length.  
5. Split data into training and validation sets.  

---

## 🧠 Model Architecture

### **LSTM Model**
- **Embedding Layer:** Input size = total vocabulary, Output dim = 100  
- **LSTM Layer 1:** 150 units, `return_sequences=True`  
- **Dropout Layer:** 0.2  
- **LSTM Layer 2:** 100 units  
- **Dense Layer:** `softmax` activation for next-word prediction  

### **GRU Model**
- **Embedding Layer:** Input size = total vocabulary, Output dim = 100  
- **GRU Layer 1:** 150 units, `return_sequences=True`  
- **Dropout Layer:** 0.2  
- **GRU Layer 2:** 100 units  
- **Dense Layer:** `softmax` activation  

**Loss Function:** Categorical Crossentropy  
**Optimizer:** Adam  
**Metrics:** Accuracy  

---

## 🚀 Training

- Training/Validation Split: 80% / 20%  
- Epochs: 50  
- Batch Size: 64  
- Callback: EarlyStopping (monitors `val_loss`)  

## Demo


https://github.com/user-attachments/assets/9ecf3078-c798-4eb3-b42b-cfdcf6479b81


