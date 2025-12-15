Fine-tuning DistilBERT for Named Entity Recognition (NER)
In this notebook I fine-tuned a pre-trained Transformer model for a token-level task: Named Entity Recognition (NER).
Unlike simple text classification, where the model predicts a single label per input, in NER we assign a label to each token in the sentence (e.g. B-PER, I-LOC, O).

We use:

The CoNLL-2003 https://huggingface.co/datasets/lhoestq/conll2003 dataset, a standard benchmark for NER in English newswire.
DistilBERT https://huggingface.co/distilbert/distilbert-base-uncased as a base model, which is a compressed version of BERT with fewer parameters and faster inference.
The HuggingFace 🤗 ecosystem (datasets, transformers, Trainer) to handle data, model, training loop, and evaluation.
The goal is to:

Prepare the CoNLL-2003 dataset for token classification.
Fine-tune DistilBERT on the training set.
Evaluate the model using sequence-level metrics (F1, precision, recall) suitable for NER.
Inspect qualitative examples of the model predictions.
The project can be executed by this link on google colab: https://colab.research.google.com/drive/1EtS2tQ7rTiQmjJuZITH_n8ooW3Yn1Kwi?usp=sharing
