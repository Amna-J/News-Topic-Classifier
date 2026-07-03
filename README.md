# News-Topic-Classifier
# News Topic Classifier — Fine-tuned BERT

A transformer-based text classifier that categorizes news headlines and descriptions into topic categories, using a fine-tuned `bert-base-uncased` model trained on the AG News dataset. Deployed with Gradio for live interaction.

## Project Overview

This project fine-tunes BERT to classify news text into four categories:

- **World**
- **Sports**
- **Business**
- **Sci/Tech**

It demonstrates NLP transfer learning, evaluation with standard classification metrics, and lightweight deployment.

## Features

- Fine-tuned `bert-base-uncased` on the AG News dataset
- Uses both title and description for richer input signal
- Evaluated with Accuracy and F1-score
- Deployed via Gradio for real-time predictions

## Results

| Metric | Score |
|---|---|
| Accuracy | 0.9482 |
| F1 Score | 0.9482 |

Evaluated on the AG News test set (7,600 held-out examples).

## Demo

Try the live demo here: **[Gradio Demo](https://e3aa1e772efbeec300.gradio.live)**

> **Note:** Gradio share links (`*.gradio.live`) expire after ~72 hours since they're temporary tunnels, not permanent hosting. If this link is dead by the time you're reading this, clone the repo and run `python app.py` locally, or see [Permanent Deployment](#permanent-deployment) below.

## Dataset

[AG News Dataset](https://huggingface.co/datasets/ag_news) — 120,000 training and 7,600 test articles across the four categories above. Includes title, description, and category label for each article.

## Project Structure

```
.
├── train_bert_classifier.py   # data loading, tokenization, fine-tuning, evaluation
├── app.py                     # Gradio deployment app
├── requirements.txt
├── bert-news-classifier/      # saved fine-tuned model + tokenizer
├── train.csv                  # AG News training data (not included — see Setup)
└── test.csv                   # AG News test data (not included — see Setup)
```

## Setup

```bash
git clone <your-repo-url>
cd news-topic-classifier
pip install -r requirements.txt
```

Download the AG News CSVs (from [Kaggle](https://www.kaggle.com/datasets/amananandrai/ag-news-classification-dataset) or Hugging Face Datasets) and place `train.csv` / `test.csv` in the project root.

### Train

```bash
python train_bert_classifier.py
```

### Run the demo

```bash
python app.py
```

## Permanent Deployment

To replace the temporary Gradio link with something that stays up indefinitely, push this repo (including the `bert-news-classifier/` model folder) to a free [Hugging Face Space](https://huggingface.co/spaces) — it hosts `app.py` on a persistent URL at no cost.

## Tech Stack

Python · PyTorch · Hugging Face Transformers · Datasets · scikit-learn · Gradio

## License

This project is licensed under the [MIT License](LICENSE).
