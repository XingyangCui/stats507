# Stats507-coursework(Xingyang Cui)
Data Science and Analytics using Python

# Cityscapes-Segmentation: SegFormer-B0 + Label Smoothing
Semantic segmentation using transformer-based models with loss-function comparison

> This repository contains the code and experiments for my final project,
> where I fine-tune a SegFormer-B0 segmentation model on the Cityscapes dataset and
compare standard cross-entropy with label-smoothed cross-entropy.

## 1. Project Overview
The goal of this project is to evaluate how **loss-function design** affects
street-view **semantic segmentation** performance::

- **Dataset**: Cityscapes (19 semantic classes)
- **Base model**: nvidia/segformer-b0-finetuned-cityscapes
- **New model**: Label-smoothed cross-entropy (ε = 0.05/0.1)
- **Task**: Generate captions that correctly mention the specific pet breed in the image


## 2. Repository Structure

```text
.
├── README.md
└── Final_Project.ipynb    # All code: data loading, training, evaluation
└── Requirement.txt        # All of thr Python dependencies

```

## 3. Installation
- Clone the repository:
  ```bash
  git clone https://github.com/XingyangCui/stats507.git
  cd stats507
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
All data and pretrained weights are automatically fetched from Hugging Face.

* Dataset:

Cityscapes (19-class semantic segmentation), hosted on Hugging Face:
👉 https://huggingface.co/datasets/tanganke/cityscapes

Covers 19 semantic classes(road, sidewalk, building, vegetation, car, bus, pedestrian, etc.)
## Example Visualization
![Cityscapes sample](Figure.png)


The dataset is automatically downloaded using the datasets library:
```bash
from datasets import load_dataset
ds = load_dataset("tanganke/cityscapes")
```

* Model:

SegFormer-B0 (from Hugging Face Transformers)

The model architecture and training configuration are defined in Final_Project.ipynb, including:

SegFormer encoder–decoder initialization, loss smoothing model



## 5. Acknowledgements
This project would not be possible without the following open-source resources:

- SegFormer-B0 model implementation by NVIDIA

- Cityscapes dataset (via Hugging Face Datasets)

- Transformers and Datasets libraries from Hugging Face

- The PyTorch ecosystem and its community

