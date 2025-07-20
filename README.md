# IndoBERT vs SVM
## IndoBERT Fine-Tuning for Sentiment Classification on #KaburAjaDulu Tweets 🚀
## IndoBERT Embeddings + SVM for Sentiment Classification on #KaburAjaDulu Tweets 🚀

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/EricoAstama/IndoBERTvsSVM/blob/main/LICENSE)
[![Hugging Face Model](https://img.shields.io/badge/HuggingFace-Model-red.svg)](https://huggingface.co/indobenchmark/indobert-base-p2)

Proyek ini berfokus pada fine-tuning model [IndoBERT] dan [IndoBERT] Embeddings sebagai feature exctration dengan [SVM] (https://huggingface.co/indobenchmark/indobert-base-p2) untuk tugas klasifikasi sentimen terhadap tweet berbahasa Indonesia yang menggunakan tagar **#KaburAjaDulu**.

## 🔍 Latar Belakang
"#KaburAjaDulu" menjadi tagar yang cukup viral di media sosial Indonesia, mencerminkan opini publik terhadap isu-isu sosial, politik, atau lingkungan. Penelitian ini mencoba mengklasifikasikan sentimen dari tweet-tweet tersebut ke dalam 3 kelas:
- **0: Positif**
- **1: Netral**
- **2: Negatif**

## 📊 Dataset
Dataset yang digunakan adalah hasil crawling dari Twitter menggunakan tagar **#KaburAjaDulu**. Dataset ini terdiri dari 20.968 tweet yang telah dilabeli secara pseudo-labeling ke dalam 3 kelas sentimen.

## 🧠 Model
Model yang digunakan untuk pseudo-labeling adalah [IndoBERT] (https://huggingface.co/ayameRushia/bert-base-indonesian-1.5G-sentiment-analysis-smsa) yang merupakan model BERT yang telah dilatih pada korpus bahasa Indonesia. Model ini diambil dari Hugging Face Model Hub dan digunakan untuk menghasilkan representasi teks yang lebih baik untuk klasifikasi sentimen.
Model yang digunakan untuk fine-tuning dan embeddings extraction adalah `indobenchmark/indobert-base-p2`, dilatih menggunakan Hugging Face `Trainer` dengan parameter fine-tuning sebagai berikut:

```python
learning_rate = 2e-5
batch_size = 16
epochs = 5
weight_decay = 0.01
```

## 🛠 Teknologi & Tools
Hugging Face Transformers 🤗

PyTorch

Scikit-learn

Evaluate (accuracy, F1-score)

Matplotlib (visualisasi loss & akurasi)


## 🤝 Kontribusi
Kontribusi terbuka! Jangan ragu untuk membuat issue atau pull request jika ingin meningkatkan proyek ini.

## 📜 Lisensi
License © 2025 Erico Astama
