# Brain MRI Tumor Detection using HOG + SVM

## Project Overview
This project implements a brain tumor detection system using **Histogram of Oriented Gradients (HOG)** features and a **Linear SVM** classifier. Tumors in MRI images are localized using a **Sliding Window** approach with bounding boxes.

## Dataset
- Source: [Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)  
- Categories:
  - `yes` → images with tumor (label = 1)  
  - `no` → images without tumor (label = 0)  
- Images resized to 128×128 and converted to grayscale.

## Workflow
1. Load and split data into train/test.  
2. Extract HOG features from all images.  
3. Train a Linear SVM classifier.  
4. Evaluate using accuracy, confusion matrix, and classification report.  
5. Detect tumors on new images using Sliding Window + NMS.  
6. Draw bounding boxes around detected tumors.

## Results
- Test Accuracy: 88.24%  
- Confusion Matrix:  
              [[16  4]
               [ 2 29]]

- Sliding Window correctly detects tumor regions and ignores normal images.

## Requirements
- Python 3.x  
- Packages: `opencv-python`, `matplotlib`, `scikit-image`, `scikit-learn`, `imutils`, `numpy`

## Future Improvements
- Multi-scale detection using image pyramids.  
- Experiment with other classifiers (Random Forest, CNN).  
- Increase dataset size for better generalization.  
- Real-time tumor detection on full MRI scans.
