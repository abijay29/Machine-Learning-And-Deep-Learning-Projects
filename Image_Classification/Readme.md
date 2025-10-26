# Vision Transformer (ViT) Model for Image Classification

## Overview
I have used a pre-trained Vision Transformer (ViT) model (`vit_h_14`) on Image Classification dataset. The model is optimized using AdamW and evaluated based on  F1 score.

## Model Architecture
- Pre-trained **ViT-H-14** from `torchvision.models`
- Modified classification head with:
  - 128 hidden units
  - Batch Normalization
  - GELU Activation
  - Dropout (0.25)
  - 10 output classes

## Dataset Preprocessing
- **Training Augmentations:** Random cropping, horizontal flipping, and normalization.
- **Testing Augmentations:** Resizing, center cropping, and normalization.

## Training Details
- Optimizer: AdamW
- Learning Rate: 3e-4
- Weight Decay: 1e-4
- Learning Rate Scheduler: StepLR (step size: 3, gamma: 0.5)
- Loss Function: CrossEntropyLoss
- Best model is saved based on F1 score.

## How to Run
1. Install dependencies (if not installed):
    ```bash pip install torch torchvision tqdm numpy matplotlib ```
2. import necessary libraries   
3. Run the notebook in a GPU environment (e.g., Kaggle, Google Colab, or local GPU)with accelerator set to T4 * 2.
4. Modify paths to dataset if necessary.
5. Run all cells sequentially (install dependencies → load data → train model → predict test data).
6.Submission file (21f3000728.csv) will be generated.
7.Submit to the competition
