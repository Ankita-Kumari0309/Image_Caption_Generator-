# Image Caption Generator using CNN + LSTM

<img width="1695" height="801" alt="model" src="https://github.com/user-attachments/assets/bd77ec7b-7795-4d18-8b20-b2573ed9fe7c" />


## 📖 Project Overview

This project focuses on automatically generating descriptive captions for images using deep learning. The system combines:

1. **Convolutional Neural Networks (CNNs)** for extracting meaningful features from images.  
2. **Long Short-Term Memory networks (LSTMs)** for generating captions word by word.  

The goal is to enable computers to **“see” and “describe” images** in human-like language, bridging computer vision and natural language processing.

---

## Concept

The project workflow consists of the following steps:

### 1. Image Feature Extraction

- A pre-trained **VGG16** model (or optionally MobileNetV2) is used to extract feature vectors representing images.  
- These features capture important visual information such as shapes, textures, and objects.

### 2. Caption Preprocessing

- Captions are cleaned by converting to lowercase, removing punctuation, and adding **start/end tokens**.  
- Tokenization converts words into **numerical sequences** suitable for the model.

### 3. LSTM Caption Model

- The LSTM takes **image features** and **tokenized captions** as input.  
- It predicts the next word in a sequence to generate a complete caption.  
- The model is trained using **categorical cross-entropy loss**.

### 4. Evaluation

- **BLEU scores** are used to compare generated captions with human-written references.  
- Example results:  
  - BLEU-1: 0.397 → good single-word overlap  
  - BLEU-2: 0.188 → captures some word sequences  

---

## 🛠️ Project Workflow

1. Load **Flickr8k dataset** (8,091 images with 5 captions each).  
2. Extract **image features** using pre-trained CNN.  
3. **Preprocess captions** for model input.  
4. Train the **LSTM model** with image features and caption sequences.  
5. Evaluate the model using **BLEU metrics**.  
6. Generate captions for unseen images.  

---

## 📂 Dataset

- **Flickr8k Dataset:**  
  - 8,091 images, 40,455 captions (5 per image)  
  

## 🔮 Future Scope

- Integrate **attention mechanisms** for better caption accuracy.  
- Train on larger datasets like **Flickr30k** or **MS COCO**.  
- Extend to **multilingual captions**.  

---

## 💻 Requirements

- Python 3.x  
- TensorFlow / Keras  
- NumPy, Pandas  
- Matplotlib / Seaborn  
- NLTK  

Install dependencies:

```bash
pip install -r requirements.txt
