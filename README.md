# 🧠 Next Word Predictor using LSTM (Trained on *Alice in Wonderland*)

This project demonstrates a **Next Word Prediction** model using deep learning architectures—**LSTM** and **GRU**—trained on Lewis Carroll's *Alice’s Adventures in Wonderland*, sourced from the **NLTK Gutenberg corpus**. The model is deployed via a **Streamlit** interface for interactive next-word prediction.

---

## 📌 Features

- Trained on the full text of *Alice in Wonderland*
- Sequence-based next word prediction using LSTM and GRU
- Early stopping for training efficiency and overfitting prevention
- Streamlit app for real-time word prediction
- Saved and reusable tokenizer and model

---

## 📁 Dataset

- 📚 **Source**: NLTK's Gutenberg Corpus
- 📄 **File Used**: `carroll-alice.txt`
- The text is preprocessed (lowercased, tokenized, and converted to padded n-gram sequences)

---

## ⚙️ Tech Stack

- **Python**
- **TensorFlow / Keras**
- **NLTK**
- **Streamlit**
- **NumPy / Pandas**
- **Scikit-learn**

---

## 🚀 How It Works

1. **Data Collection**: Load and extract raw text from the Gutenberg corpus using `nltk.corpus.gutenberg`.
2. **Preprocessing**:
   - Lowercasing and tokenizing using Keras’ `Tokenizer`
   - Generate padded n-gram sequences
   - One-hot encode target labels
3. **Model Training**:
   - Build LSTM/GRU models with `Embedding`, `Dropout`, and `Dense` layers
   - Apply EarlyStopping to prevent overfitting
4. **Prediction**:
   - Input any partial sentence into the Streamlit app
   - Model returns the next likely word
5. **Deployment**:
   - Save the trained model as `Next_word_lstm.h5`
   - Save the tokenizer using `pickle`
   - Load both in a Streamlit interface

---


## 🧪 Run Locally

### 🔧 Install Requirements

Make sure you have Python 3.7+ installed, then run:

```bash
pip install -r requirements.txt
```

### ▶️ Run the Streamlit App

```bash
streamlit run app.py
```

> Ensure `Next_word_lstm.h5` and `tokenizer.pickle` are present in the same directory as `app.py`.

---

## 🎯 Example Prediction

**Input:**  
```
ALL PERSONS MORE THAN A MILE HIGH TO LEAVE THE
```

**Predicted Next Word:**  
```
court
```

---
