# Named Entity Recognition using BiLSTM + LSTM with GloVe Embeddings

This project implements a deep learning-based Named Entity Recognition (NER) model using a combination of BiLSTM and LSTM layers. It leverages pre-trained GloVe embeddings to enhance the model’s semantic understanding and generalization capabilities. The model is trained on a sequence-tagged dataset using the BIO format.

## 📌 Objective

To build a robust NER system that can automatically recognize and classify entities such as persons, locations, organizations, etc., using a deep learning architecture with minimal manual feature engineering.

## 🧠 Model Architecture

- **Embedding Layer**: Initialized using pre-trained GloVe vectors (`glove.6B.100d.txt`)
- **BiLSTM Layer**: Captures both past and future context in sequences
- **LSTM Layer**: Deepens contextual understanding
- **TimeDistributed Dense Layer**: Applies softmax classifier to each time step

## 📊 Dataset

We use a publicly available dataset from [Aman Kharwal’s GitHub repository][([https://github.com/amankharwal/Named-Entity-Recognition-NLP](https://github.com/amankharwal/Website-data))](https://github.com/amankharwal/Website-data). The dataset contains over 14 MB of labeled text with fields: `Sentence #`, `Word`, `POS`, and `Tag` (BIO format).

## 🔡 Word Embeddings (GloVe)

We use **100-dimensional GloVe vectors** trained on Wikipedia and Gigaword.

## 📈 Results

The model demonstrates strong performance in recognizing named entities using the BiLSTM + LSTM architecture with GloVe embeddings. Below are the key observations from the training:

### 🔻 Loss Over Epochs
- The **training loss** consistently decreases over time, indicating that the model is successfully learning patterns from the data.
- The **validation loss** remains relatively stable and only slightly higher than training loss, suggesting minimal overfitting.

### 📈 Accuracy Over Epochs
- **Training accuracy** shows a steady increase and surpasses **98.75%**, indicating effective learning.
- **Validation accuracy** closely follows training accuracy, reinforcing the model’s ability to generalize to unseen data.

---

#### 🔍 Key Insights:
- The model effectively uses GloVe embeddings to enhance semantic understanding.
- No signs of significant overfitting.
- Stable convergence achieved within **25 epochs**.
- Excellent balance between performance and complexity, considering the model doesn’t use advanced architectures like CRF or Transformers.

---

These results validate the reliability and generalizability of the approach for sequence labeling tasks such as Named Entity Recognition (NER).
