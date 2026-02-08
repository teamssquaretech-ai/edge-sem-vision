# edge-sem-vision
Edge AI project for detecting and classifying defects in SEM images, with defect localization, yield calculation, and ONNX deployment.

## Features
- SEM image classification
- 4-stage inspection pipeline:
  1. Whole image classification
  2. Patch-wise defect analysis (image divided into grid and each patch analyzed)
  3. Defect heatmap generation
  4. Yield calculation (percentage of clean regions vs total regions)
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
Dataset link: [Download CleanDataset.zip](https://drive.google.com/uc?export=download&id=1bWkKMjLqghkPmVGUKR6vS9YlTUVqHSfg)


## Model
- Backbone: MobileNetV2 (Transfer Learning)
- Framework: PyTorch
- Deployment: ONNX (Edge Deployment)

## Results (Test Set)
- Accuracy: 95.45% (How often the model is correct overall.)
- Precision: 95.93% (How many predicted defects are truly defects.)
- Recall: 95.45% (How many real defects the model successfully finds.)
- F1 Score: 95.11% (Balance between precision and recall.) 
- Model Size: 8.78 MB

## How to Run
1. Open notebook in Google Colab or Jupyter
2. Upload dataset
3. Run cells from top to bottom
4. Results and dashboards are saved automatically

## Outputs
- inspection_result_*.png  (random 3 samples)
- confusion_matrix.png (Table showing correct and incorrect predictions for each class.)
- training_history.png
- ONNX model

## Platform
- PyTorch 2.9.0 (CPU)
