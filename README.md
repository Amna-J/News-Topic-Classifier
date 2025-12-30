News Topic Classifier Using BERT
Project Overview

This project fine-tunes a BERT model to classify news headlines and descriptions into four categories:

World

Sports

Business

Sci/Tech

It uses the AG News Dataset and demonstrates NLP transfer learning, evaluation metrics, and deployment using Gradio.

Features

Fine-tuned bert-base-uncased on AG News dataset

Uses both title and description for better classification

Evaluates model using Accuracy and F1-score

Deployable via Gradio for live interaction

Evaluation

Accuracy and F1-score metrics are used to evaluate the model

The model performs well on test data from AG News dataset

Deployment

The trained model is deployed using Gradio for real-time news classification

Users can input a news title and description to get the predicted category

Gradio Link

Try the live demo here:
[(https://e3aa1e772efbeec300.gradio.live)]

Dataset

AG News Dataset available on Hugging Face Datasets

Includes news title, description, and category label

License

This project is for educational purposes.
