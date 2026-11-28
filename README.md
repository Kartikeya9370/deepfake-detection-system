# DeepFake Detection System

A notebook workflow for binary real/fake image classification, comparing a SmallCNN baseline with pretrained ResNet18, VGG16, and Vision Transformer models.

## Canonical notebook

Open [Deepfake_Detection.ipynb](./Deepfake_Detection.ipynb) in Jupyter Notebook, JupyterLab, or Google Colab. Run the cells from top to bottom.

## Setup

Use Python 3.11 or newer.

1. Install a PyTorch and TorchVision pair matching your operating system and compute platform from the [official PyTorch selector](https://pytorch.org/get-started/locally/).
2. Install the project dependencies:
   ```bash
   python -m pip install -r requirements.txt
   ```
3. Open the notebook and run its setup and dataset cells before training.

The notebook downloads the [DeepFake vs Real 60K dataset](https://www.kaggle.com/datasets/prithivsakthiur/deepfake-vs-real-60k) with KaggleHub. If Kaggle requests account access or acceptance of dataset terms, complete that through Kaggle's supported flow; do not store credentials in the notebook or repository. A GPU is recommended because training four models may take hours on a CPU.

## Training and evaluation

The notebook documents the random seed, dataset split, model settings, and epoch batch cap in its configuration cell. Set `max_batches_per_epoch` to `None` to use all batches. Model comparison is reported on the validation split. The notebook notes the project's dataset-integrity concern and does not present validation metrics as an independent test benchmark.

Model checkpoints and metadata are written under `artifacts/checkpoints/`, which is ignored by Git.
