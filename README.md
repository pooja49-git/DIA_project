# Image Segmentation for Biomedical Applications: Classical Approaches on Retinal Images

## Authors
- Pooja Naveen Poonia (M24CSA020)
- Pranjal Malik (M24CSA021)
- Prathmesh Chintamani Gosavi (M24CSA023)

**Course**: CSL7320: Digital Image Analysis, AY 2024-25, Semester II


## 📄 Project Overview

Biomedical image segmentation is a crucial step for tasks such as disease detection, treatment planning, and quantitative analysis in medical imaging. In this project, we explore classical (non-deep-learning) image segmentation techniques, applied to retinal images.

Our focus is on interpretable and resource-efficient methods that lay the groundwork for future comparative studies with deep learning approaches.


## 🧪 Problem Statement

Accurate segmentation of anatomical structures like blood vessels in retinal images is vital for biomedical research and clinical diagnostics. We evaluate traditional segmentation algorithms on a publicly available retinal image dataset to analyze their effectiveness.


## 💡 Methods Explored

### 1️⃣ Thresholding Methods
- **Global Thresholding**: Simple intensity-based method, fast but fails under uneven illumination.
- **Otsu's Method**: Maximizes between-class variance.
- **Adaptive Thresholding**: Calculates local thresholds; handles varying lighting conditions better.

### 2️⃣ Region-Based Methods
- **Seeded Region Growing**: Regions expand from manually defined seeds.
- **Watershed Segmentation**: Uses gradient information and markers to separate touching structures.

### 3️⃣ Edge-Based Methods
- **Active Contours (Snakes)**: Evolve contours to match object boundaries, robust against edge noise.
- **Chan-Vese Model**: Handles missing edges via energy minimization.


## ⚙️ Methodology

### Preprocessing
- LAB color conversion and CLAHE enhancement.
- Morphological top-hat filtering to highlight vessels.
- Gaussian blurring.

### Workflow
1. Load and preprocess retinal images.
2. Apply segmentation algorithms (thresholding, region growing, watershed, active contours).
3. Visualize results and compare with ground truth masks.
4. Evaluate using metrics (Precision, Recall, F1 Score, Jaccard Index, Accuracy).


## 📊 Dataset

- **Source**: Public retinal dataset.
- **Contents**:
  - `images/`: Original retinal images.
  - `1st_manual/`: Ground truth vessel segmentations.
  - `mask/`: Field-of-view masks.
    

## ✅ Results

### Quantitative Metrics (Region Growing Example)
- **Precision**: 0.5612
- **Recall**: 0.9504
- **F1 Score**: 0.7057
- **Jaccard Index**: 0.5452
- **Accuracy**: 0.9316

### Observations
- **Thresholding**: Simple and fast, but struggles with uneven illumination.
- **Region-Based**: Effective at connected structures but sensitive to noise.
- **Edge-Based**: Captures smooth, continuous boundaries well, robust to noise.


## 💬 Conclusion

Classical segmentation methods provide interpretable and lightweight solutions for biomedical image analysis. However, they have limitations in challenging conditions such as noise and lighting variations. Future work can explore hybrid or deep learning-based techniques (e.g., U-Net) to improve accuracy.

## 🔗 Resources

- [Project Code on Google Colab](https://colab.research.google.com/drive/1HCUQTQhh8mI9bvd-z8uIz60TlCfctdAX?usp=sharing)
- [scikit-image](https://scikit-image.org/)
- [OpenCV Documentation](https://docs.opencv.org/)


## 📄 References

- Kass, M., Witkin, A., & Terzopoulos, D. (1988). Snakes: Active contour models. IJCV.
- Ronneberger, O., Fischer, P., & Brox, T. (2015). U-Net: Convolutional Networks for Biomedical Image Segmentation. MICCAI.
- Gonzalez, R. C., & Woods, R. E. (2002). Digital Image Processing.


## 💻 How to Run

1. Open the [Google Colab notebook](https://colab.research.google.com/drive/1HCUQTQhh8mI9bvd-z8uIz60TlCfctdAX?usp=sharing).
2. Upload dataset folders (`images/`, `1st_manual/`, `mask/`).
3. Run each section step by step to preprocess, segment, and evaluate.
