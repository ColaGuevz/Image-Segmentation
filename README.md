# Enhanced Leaf Segmentation in Cassava Plant Images using CNN

## Repository Overview
This repository contains an implementation of a **Convolutional Neural Network (CNN)** approach for leaf segmentation in cassava plant images. The study demonstrates the advantages of deep learning over traditional image thresholding techniques by leveraging the **U-Net architecture** for accurate segmentation.

## Objective
The goal of this research is to improve leaf segmentation accuracy in cassava plant images by:
- Implementing **U-Net CNN** for adaptive thresholding.
- Comparing CNN-based segmentation with **Otsu thresholding and median blur**.
- Evaluating the model's performance using **precision, recall, F1-score, and noise/white region analysis**.

## Dataset
- **23,000+ cassava plant images** collected from Brgy. Pangasugan, Baybay City, Leyte.
- Captured using a **SONY ZV-1 camera** at **3648 x 3648** resolution.
- Resized to **500 x 500** for faster processing.
- **1,040 manually segmented images** using Adobe Photoshop as ground truth.

## Model and Methodology
1. **Data Preprocessing**
   - Image resizing
   - Manual segmentation for ground truth labels
   - Conversion to binary images (PNG format for lossless compression)
2. **CNN Model: U-Net Architecture**
   - Encoder-decoder structure with skip connections
   - Adam optimizer and categorical cross-entropy loss
   - **Trained on Google Colab (GPU T4)** for enhanced performance
3. **Performance Evaluation**
   - Comparison with **Otsu thresholding and median blur**
   - Evaluated using **precision, recall, F1-score, and noise reduction**

## Results and Key Findings
### **Segmentation Performance Comparison**
| Method                 | Average Precision | Average Recall | Average F1-Score |
|------------------------|------------------|----------------|------------------|
| **CNN-U-Net**         | **0.9956**       | **0.9963**     | **0.9959**       |
| **Otsu Thresholding** | **0.9927**       | **0.9869**     | **0.9948**       |
| **Adaptive Threshold** | **0.1029**       | **0.8037**     | **0.1812**       |
| **Otsu + Median Blur**| **0.8956**       | **0.9984**     | **0.9441**       |

### **Noise/White Region Analysis**
| Method                | Average Noise/White Regions |
|-----------------------|---------------------------|
| **CNN-U-Net**        | **0.49**                  |
| **Otsu Thresholding**| **74.905**                |
| **Adaptive Threshold**| **35.295**                |
| **Otsu + Median Blur** | **146.75**              |
| **Ground Truth (Manual)** | **0.02**            |

- **CNN significantly outperformed Otsu thresholding and median blur**, demonstrating superior segmentation.
- **Otsu + Median Blur had high recall but struggled with precision due to noise artifacts**.
- **CNN-U-Net maintained high accuracy while minimizing noise/white regions**.

## Future Work
- **Expand dataset** to include different plant species and environments.
- **Improve segmentation metrics** by incorporating **IoU and Dice coefficient**.
- **Optimize model for real-time deployment** in agricultural monitoring systems.
- **Explore transfer learning** using pre-trained models.
- **Integrate with other computer vision tasks such as disease detection and plant monitoring**.

## How to Use This Repository
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name/Leaf-Segmentation-CNN.git
   ```
2. Prepare the dataset by resizing and labeling images.
3. Train the U-Net model using TensorFlow and Google Colab.
4. Evaluate the model's performance using segmentation accuracy metrics.

## Authors
- **Marcelo Rc. D Guevarra**
- **mrrcguevarra@gmail.com**

## Full Paper
- https://drive.google.com/file/d/14IcSrgvJnxrYR-5KRkRxX2SGtxhORQzk/view?usp=sharing

---
