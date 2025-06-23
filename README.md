# Tweet Profession Classifier 🧠🇪🇸

This project trains a machine learning model to **classify Spanish-language tweets** based on whether they **mention a profession or not**. It is designed for tasks such as social media content analysis, text mining, or sociolinguistic studies.

> 🔧 Fully developed in **Google Colaboratory**, using Python and modern NLP libraries like Hugging Face 🤗 Transformers.

---

## 📊 Objective

Train a Spanish BERT model to classify tweets into two categories:
- **Class 0 (NO_PROFESSION)**: Does not mention professions.
- **Class 1 (WITH_PROFESSION)**: Explicitly mentions professions.

---

## 🧪 Best Model Metrics

| Class                 | Precision | Recall | F1-Score |
|-----------------------|-----------|--------|----------|
| **NO_PROFESSION (0)** | 0.98      | 0.94   | 0.96     |
| **WITH_PROFESSION (1)** | 0.83    | 0.95   | 0.89     |

> Overall accuracy: **93.8%**  
> Average macro F1 score: **0.938**

---

## 🧼 Preprocessing

- Tokenization using Hugging Face's `AutoTokenizer`

---

## 🧾 Data Source

We used a subset of social media data, specifically from Task 1 of the shared task [**ProfNER**](https://temu.bsc.es/smm4h-spanish), focused on detecting mentions of professions in tweets published during the COVID-19 pandemic.

The original goal of the task was to analyze which professions might have been particularly vulnerable during the health crisis.

The dataset was downloaded from the [Hugging Face repository](https://huggingface.co/datasets/luisgasco/profner_classification_master), and includes:

- **Training set**: with IDs, text, and labels.
- **Validation set**: same structure as training.
- **Test set**: includes only IDs and text (no labels).

---

## 🤖 Model

- Base model: [`dccuchile/bert-base-spanish-wwm-cased`](https://huggingface.co/dccuchile/bert-base-spanish-wwm-cased)
- Trained using `transformers.Trainer`

---

## 🧪 Required Libraries

```bash
pip install numpy==1.26.4 fsspec==2023.9.2 transformers datasets evaluate accelerate bitsandbytes transformers-interpret scikit-learn

## 🧪 Librerías necesarias

```bash
pip install numpy==1.26.4 fsspec==2023.9.2 transformers datasets evaluate accelerate bitsandbytes transformers-interpret scikit-learn


