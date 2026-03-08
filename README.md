#  IMDb Movie Review Sentiment Analysis (Bidirectional LSTM)
---------------------------------------------------------------------

A deep learning project that predicts whether a movie review is **Positive** or **Negative** using a **Bidirectional LSTM (BiLSTM)** model.
This project uses the **IMDb dataset (50,000 reviews)** built directly into Keras.

---

###  Project Overview

This project performs **sentiment analysis** on movie reviews. The model learns emotional patterns from thousands of reviews and predicts the sentiment of new unseen text.

* Dataset: IMDb (50,000 reviews)
* Task: Binary Classification (Positive / Negative)
* Model: Bidirectional LSTM
* Framework: TensorFlow/Keras
* Visualizations: Accuracy & Loss graphs (Matplotlib)

---

##  Objective

* Train a BiLSTM on IMDb's 50K reviews
* Understand NLP preprocessing (tokenization, padding, embedding)
* Build a deep learning model that reads text forward + backward
* Predict sentiment of new custom movie reviews

---

##  Dataset Details

IMDb dataset is built into Keras—no manual download required.

* 25,000 training reviews
* 25,000 testing reviews
* Labels:

  * **1 → Positive Review**
  * **0 → Negative Review**

Keras provides reviews in tokenized (number) format.

---

##  Model Architecture

```
Embedding → Bidirectional(LSTM) → Dropout → Dense → Dropout → Dense(Output)
```

### Layers Used:

* **Embedding(10000, 128)**
* **Bidirectional(LSTM(64))**
* **Dense(64, activation='relu')**
* **Dropout layers (0.4, 0.3)**
* **Output: Dense(1, activation='sigmoid')**

---

##  Workflow

1. Import IMDb dataset from Keras
2. Pad sequences to fixed length (200)
3. Build Bidirectional LSTM model
4. Compile with binary crossentropy & Adam optimizer
5. Train with validation split
6. Plot accuracy/loss graphs
7. Evaluate on test data
8. Predict custom sentences

---

##  Visualizations

The project includes:

* Training Accuracy vs Validation Accuracy
* Training Loss vs Validation Loss

These help understand model performance and overfitting.

---

##  Prediction Example

Input:

```
"The movie was emotional and beautifully directed"
```

Output:

```
Positive Review 😊
```

Input:

```
"The film was boring and poorly executed"
```

Output:

```
Negative Review 😔
```

 ## Author -- Ankit Kashyap
