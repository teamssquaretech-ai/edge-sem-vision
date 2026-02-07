# edge-sem-vision
Edge AI project for detecting and classifying defects in SEM images, with defect localization, yield calculation, and ONNX deployment.

# Edge SEM Vision
Edge AI system for detecting and classifying defects in SEM images using deep learning.

## Features
- SEM image classification
- Patch-based defect localization
- Yield calculation
- ONNX model export for edge deployment
- Visualization dashboard

## Dataset Structure
dataset/
 ├── train/
 ├── val/
 └── test/
Each of the above folders contains the following class subfolders:
- Bridge  
- Clean  
- CMP  
- Crackes  
- LER  
- Missing patterns  
- Multiple defects in one image  
- Open  
- Ripple  
- Scratch  
- Stain and Edge Contamination  
- VIAS  

Total Classes: 12 (1 Clean + 11 Defect Categories)

## Model
- Backbone: MobileNetV2 (Transfer Learning)
- Framework: PyTorch
- Deployment: ONNX (Edge Deployment)

## Results (Test Set)
- Accuracy: 95.45%
- Precision: 95.93%
- Recall: 95.45%
- F1 Score: 95.11%
- Model Size: 8.78 MB

## How to Run
1. Open notebook in Google Colab or Jupyter
2. Upload dataset
3. Run cells from top to bottom
4. Results and dashboards are saved automatically

## Outputs
- inspection_result_*.png  (random 3 samples)
- confusion_matrix.png
- training_history.png
- ONNX model

## Platform
- PyTorch 2.9.0 (CPU)
