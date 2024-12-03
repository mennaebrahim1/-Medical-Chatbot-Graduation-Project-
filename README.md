# Diagnosy: Arabic Healthcare Chatbot

Diagnosy is an AI-powered chatbot designed to assist in diagnosing health conditions using natural language processing (NLP) techniques, specifically tailored for the Arabic language and its diverse dialects. It leverages deep learning models such as LSTM, Bi-LSTM, and Transformer for text classification and disease prediction. This chatbot helps to bridge the healthcare access gap, especially in regions with limited medical resources, by providing automated medical consultations.

## Project Overview

The **Diagnosy** project addresses the growing need for accessible healthcare solutions, particularly in the wake of the COVID-19 pandemic. By using state-of-the-art NLP techniques, this chatbot can process questions in Arabic, provide relevant medical advice, and suggest potential diagnoses. It is built using the largest Arabic healthcare Q&A dataset, **MAQA**, which consists of over 430,000 questions across 20 medical specializations. The system has been evaluated using various models, including LSTM, Bi-LSTM, and Transformer, with promising results.

---

## Features

- **Arabic Language Support**: Tailored to handle diverse Arabic dialects, making it suitable for a wide audience.
- **Medical Assistance**: Provides automated responses based on user queries related to healthcare, covering over 20 medical specialties.
- **High Accuracy**: Uses state-of-the-art deep learning models (LSTM, Bi-LSTM, Transformer) to provide accurate predictions and diagnoses.
- **Scalability**: Handles large datasets and can be fine-tuned to specific medical fields.
- **Data Preprocessing**: Features advanced preprocessing techniques for cleaning and preparing Arabic data for NLP tasks.

---

## Usage

1. **Preprocessing Data**: Before training, preprocess the dataset using the provided `preprocessing.py` script. This will handle tasks such as:

   - Text cleaning
   - Tokenization
   - Padding sequences
   - Diacritic removal
   - Handling missing values

## Preprocessing

### Data Balancing

The dataset is preprocessed using techniques such as:

- **Translation-based Augmentation**: To balance underrepresented classes.
- **Word Swap**: A simple data augmentation technique to generate new samples.
- **Scraping Technique**: For enhancing dataset diversity.

### Text Preprocessing

- Removed unnecessary columns (e.g., answer body, answer count).
- Tokenization and padding are applied to ensure consistent input lengths.
- Standardization of Arabic letters and removal of diacritics for uniform text representation.

---

## Models Used

1. **Machine Learning Models**:
   - **Random Forest**: An ensemble method for classification tasks.
   - **SVM (Support Vector Machine)**: For classification tasks, especially useful for high-dimensional data.
   - **Multinomial Naive Bayes**: For text classification based on probability.

2. **Deep Learning Models**:
   - **LSTM**: Long Short-Term Memory networks for capturing long-term dependencies.
   - **Bi-LSTM**: Bidirectional LSTM for better context understanding.
   - **Transformer**: A powerful architecture based on attention mechanisms, used for sequence-to-sequence tasks.
   - **BERT (Fine-Tuning)**: Pre-trained transformer-based model fine-tuned for specific medical text classification.

---

## Results

### Unbalanced Data:
- **Transformer Model**: Achieved 91.8% average similarity and 63.1% BLEU score on unbalanced data.
- **Class Performance**: Classes like "أمراض الجهاز التنفسي" performed better, while "أمراض نسائية" showed slightly lower performance.

### Balanced Data:
- **Fine-Tuning Model**: Achieved 96.6% similarity and 63% BLEU.
- **Transformer Model**: Achieved 95.4% similarity and 61.5% BLEU.

### Full Dataset:
- **Transformer Model**: Achieved 96.2% similarity and 63% BLEU when trained on the full dataset.

---

## Acknowledgements

This project would not have been possible without the support and contributions of several individuals and organizations. Special thanks to:

- **Prof. Dr. Dina El-Sayad** and **T.A. Radwa El-Hussieny** for their guidance and expertise throughout this project.
- **Google Colab** for providing the computational resources to train the deep learning models.
- The creators of the **MAQA** dataset for enabling research into Arabic healthcare chatbots.

