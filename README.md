
# 🏏 Cricket Image Captioning using VGG16 and LSTM

This project builds a Cricket Image Captioning system — a deep learning model that automatically generates textual commentary-like descriptions for cricket match images.

It uses a Convolutional Neural Network (VGG16) for image feature extraction and a Recurrent Neural Network (LSTM) for generating natural language descriptions.

---

## 📘 Overview

The system uses a **CNN + RNN (Encoder–Decoder)** architecture to generate captions for cricket images.

* **VGG16 (Encoder):** extracts deep visual features (4096-dimensional vectors).
* **LSTM (Decoder):** learns to generate textual descriptions based on image features.
* **Goal:** automatically produce descriptive cricket commentary such as

  > “batsman hits the ball towards midwicket.”

---



## 🧠 Model Architecture

### Encoder (VGG16)

* Pretrained on ImageNet.
* Extracts visual features from images (layer before the classification layer).
* Output: 4096-dimensional feature vector.

### Decoder (LSTM)

* Embedding layer to convert words into dense vectors.
* LSTM (256 units) to generate sequential text.
* Fully connected layer + Softmax for predicting the next word.

### Combined Model

* Image feature vector and text sequence are **merged** (via element-wise addition).
* Trained using **categorical cross-entropy loss** with the **Adam** optimizer.

---

## ⚙️ Requirements

Install dependencies before running:

```bash
pip install requirements
```

---

## 📊 Results

Image	Predicted Caption
🏏 result_1_1_9.png	batsman is looking somewhere
🏏result_text2.jpg	bowler bowled the bal l and batsman played tremendous shot




---


