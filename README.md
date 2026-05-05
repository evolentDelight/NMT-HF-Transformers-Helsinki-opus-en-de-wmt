# English-to-German Neural Machine Translation with MarianMT

This repository contains a CMPE 252 neural machine translation project for English-to-German translation using a Transformer encoder-decoder model.

The project uses the pretrained `Helsinki-NLP/opus-mt-en-de` MarianMT model as the baseline system. The baseline is evaluated directly on the development set using SacreBLEU. The same model is then fine-tuned on a WMT-style English-German training subset, with experiments changing one hyperparameter at a time to study the effect on development SacreBLEU.

The project focuses on documenting the full machine translation workflow:

- loading local English-German parallel datasets,
- evaluating a pretrained baseline model,
- saving baseline and fine-tuned checkpoints,
- fine-tuning a Transformer-based NMT model,
- comparing experiments using SacreBLEU,
- visualizing training loss and decoder cross-attention,
- showing qualitative sample translations,
- selecting the final model using the development set,
- evaluating the final selected checkpoint on the held-out test set.

The final notebook is organized as a formal report and can be exported to PDF for submission.

## Task

- Source language: English
- Target language: German
- Model: `Helsinki-NLP/opus-mt-en-de`
- Architecture: MarianMT Transformer encoder-decoder
- Metric: SacreBLEU
- Dataset format: local parallel text files

## Dataset Files

The project expects local parallel text files:

```text
data/deu-eng/train.eng
data/deu-eng/train.deu
data/deu-eng/dev.eng
data/deu-eng/dev.deu
data/deu-eng/test.eng
data/deu-eng/test.deu
