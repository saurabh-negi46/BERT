# Kaggle notebook

The notebook is set up for Kaggle GPU sessions and uses PyTorch `DataParallel` when two CUDA GPUs are available. It expects the token sequences and tokenizer to be attached as inputs:

- `negi69/bert-token-sequences` (`bert_token_sequences.jsonl`)
- `negi69/bert-tokenizer` (`bert_tokenizer.json`)

It searches `/kaggle/input` for both files and writes checkpoints to `/kaggle/working/checkpoints/bert_base_mlm/`. The notebook is configured as private and requests the dual-T4 machine shape. The 3 GB token file is attached from Kaggle rather than copied into this folder.

Notebook: [BERT-BASE from Scratch with PyTorch](https://www.kaggle.com/code/negi69/bert-base-from-scratch-with-pytorch)
