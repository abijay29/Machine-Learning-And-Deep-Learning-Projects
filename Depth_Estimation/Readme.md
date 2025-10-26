# Depth Estimation using U-Net

## Overview
I have used a  **U-Net model** for depth estimation. The model is optimized using the Adam optimizer and evaluated based on Root Mean Square Error (RMSE).

## Training Details

- **Model Used:** U-Net
- **Optimizer:** Adam
- **Learning Rate:** 1e-3
- **Evaluation Metric:** Root Mean Square Error (RMSE)
- **Batch Size:** 32
- **Image Size:** 128x128
- **Epochs:** 10
- **Early Stopping:** Enabled (Patience = 3)
- **Device:** CUDA (GPU)
- **Best Model Saving Criteria:** RMSE on validation data

## Steps to Run
1. Install dependencies (if not installed)
2. Import necessary libraries   
3. Run the notebook in a GPU environment with accelerator set to T4 * 2.
4. Run all cells sequentially (install dependencies → load data → train model → evaluate →  predict test data).
5.Submission file (predictions.csv) will be generated.
6.Submit to the competition