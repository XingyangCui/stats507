# Stats507-coursework
Data Science and Analytics using Python

# Cityscapes-Segmentation: SegFormer-B0 + Label Smoothing
Semantic segmentation using transformer-based models with loss-function comparison

> This repository contains the code and experiments for my final project,
> where I fine-tune a SegFormer-B0 segmentation model on the Cityscapes dataset and
compare standard cross-entropy with label-smoothed cross-entropy.

## 1. Project Overview
The goal of this project is to evaluate how **loss-function design** affects
street-view **semantic segmentation** performance::

- **Base model**: nvidia/segformer-b0-finetuned-cityscapes-1024-1024
- **Dataset**: Cityscapes (19 semantic classes)
- **Method1e**: Standard cross-entropy loss
- **Method2e**: Label-smoothed cross-entropy (ε = 0.05)
- **Task**: Generate captions that correctly mention the specific pet breed in the image


## 2. Repository Structure

```text
.
├── README.md
└── Final_Project.ipynb    # All code: data loading, training, evaluation
└── Requirement.txt # All Python dependencies

```

## 3. Installation
- Clone the repository:
  ```bash
  git clone https://github.com/<your-username>/<repo>.git
  cd <repo>
  ```

- Install Dependencies：
  ```bash
  pip install -r requirements.txt
  ```
  This will install:
  * `torch`, `ttorchvision`, `numpy`, `matplotlib`, `seaborn`
  * `scikit-learn`, `tqdm`

## 4. Data & Model

No manual download is required.
The scripts automatically fetch everything from Hugging Face:

* Model: Salesforce/blip-image-captioning-base

* Dataset: Oxford-IIIT Pet (via Hugging Face Datasets mirror)

Dataset loading and preprocessing are handled inside `data.py`, while the base model is loaded in `model.py`.



## 5. Acknowledgements
This project would not be possible without the following open-source resources:

- SegFormer-B0 model implementation by NVIDIA

- Cityscapes dataset (via Hugging Face Datasets)

- Transformers and Datasets libraries from Hugging Face

- The PyTorch ecosystem and its community

