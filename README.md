# BERT from scratch

This project contains notebooks for preparing a text corpus, training a WordPiece tokenizer, and pretraining a BERT-base model with PyTorch.

## Notebooks

- `download_data.ipynb` downloads a FineWeb-Edu sample.
- `tokenizer.ipynb` cleans the text, trains the WordPiece tokenizer, and writes token sequences.
- `train_bert_base.ipynb` builds BERT-base and trains it with masked language modeling and next sentence prediction.
- `kaggle_submission/train_bert_base_kaggle.ipynb` is the version prepared for Kaggle GPU sessions.

The training notebook uses the local files `bert_tokenizer.json` and `bert_token_sequences.jsonl`. The Kaggle notebook looks for the same files under `/kaggle/input` and writes checkpoints under `/kaggle/working`.

## Checkpoints

At the end of each epoch, training saves `latest_checkpoint.pt`. When validation loss improves, it also saves `best_model.pt` under `checkpoints/bert_base_mlm/`.

The corpus files and checkpoints are not tracked in Git; see `.gitignore`. Keep the tokenizer JSON with the notebooks because the training code needs its vocabulary and token IDs.
