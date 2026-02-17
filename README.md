# Polish Intent Classification with HerBERT

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![Transformers](https://img.shields.io/badge/library-HuggingFace-orange.svg)
![Framework](https://img.shields.io/badge/framework-PyTorch-red.svg)

## 📌 Project Overview
This repository contains a specialized Natural Language Processing (NLP) pipeline for **Intent Classification in Polish**. The project utilizes **HerBERT** (a state-of-the-art Polish BERT model) fine-tuned on a custom dataset of 13 unique user intents, ranging from weather queries to literature analysis.

The goal of this project is to demonstrate how to effectively handle Polish-specific linguistic nuances using Transformer-based architectures.



## 🧠 Model Choice: Why HerBERT?
For this task, I used `allegro/herbert-base-cased`. Unlike multilingual BERT models, HerBERT was trained specifically on massive Polish corpora (NKJP, Wikipedia, etc.). This ensures:
* Better handling of **Polish morphology** and inflection.
* Precise understanding of context and syntax.
* Superior performance in downstream tasks compared to general models.

## 📊 Dataset & Intents
The model is trained to recognize 13 distinct categories:
* **General:** Greeting (`przywitanie`), Calculation (`wykonanie_obliczenia`)
* **Services:** Food Ordering, Taxi Booking, Opening Hours
* **Daily Assistant:** Weather, Reminders, Music Control
* **Knowledge:** Definitions, Literature, Cooking, Electronics Search

## 🚀 Technical Stack
* **Language:** Python
* **Modeling:** `transformers` (Hugging Face), `torch` (PyTorch)
* **Data Processing:** `pandas`, `datasets`
* **Evaluation:** `scikit-learn` (Accuracy, F1-Macro, Classification Report)

## 📈 Performance
The training pipeline includes evaluation on a stratified test set. 
* **Training Loop:** 3 Epochs with Warmup and Weight Decay.
* **Best Model Selection:** Based on F1-Macro score to handle potential class imbalances.



## 🛠️ Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YourUsername/Polish-Intent-Classification-HerBERT.git](https://github.com/YourUsername/Polish-Intent-Classification-HerBERT.git)
   cd Polish-Intent-Classification-HerBERT
