# Bird-Text-to-Image-cGAN 🐦✨

A **Conditional Generative Adversarial Network (cGAN)** that generates bird images from textual descriptions using **BERT embeddings**, trained on the **CUB-200-2011 dataset**.

---

## Description
This project implements a **text-conditioned cGAN** to generate **64x64 RGB bird images** from textual descriptions. The model leverages **BERT embeddings** to condition the generator on textual inputs, enabling semantic control over the generated outputs. The pipeline includes:
- **BERT-based text preprocessing**: Tokenizes textual descriptions using the `bert-base-uncased` model.
- **Image resizing and normalization**: Resizes images to 64x64 pixels and normalizes pixel values to [0, 1].
- **Custom cGAN architecture**: Includes a generator and discriminator conditioned on BERT embeddings.
- **Training loop with loss tracking**: Implements a custom training loop to update the generator and discriminator.
- **Synthetic image generation and evaluation**: Generates synthetic bird images and evaluates their quality.

This project is part of the **CS495 - Machine Learning** course at the Mediterranean Institute of Technology.

---

## Dataset
The [CUB-200-2011 dataset](http://www.vision.caltech.edu/visipedia/CUB-200-2011.html) is used, containing **11,788 images** of **200 bird species**. Key metadata files include:
- `classes.txt`: Species labels.
- `images.txt`: Image paths.
- `train_test_split.txt`: Training/validation split.

---

## Features
- **BERT Embeddings**: Textual descriptions tokenized using `bert-base-uncased`.
- **cGAN Architecture**:
  - **Generator**: Transposed CNN layers conditioned on BERT embeddings.
  - **Discriminator**: CNN + Dense layers with joint image-text input.
- **Training Pipeline**: Custom training loop with dynamic loss tracking.
- **Visualizations**: Model architecture diagrams and loss curves.
