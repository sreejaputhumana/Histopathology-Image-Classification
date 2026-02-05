## Breast Cancer Histopathology-Image-Classification

# Dataset
- **Dataset**: PatchCamelyon (PCam) (1)(2)
- **Source**: https://github.com/basveeling/pcam

# Aim: 
Analyzing pathology images is essential for accurate disease diagnosis and treatment but is often labor-intensive and inconsistent. Transformer-based models process large datasets and capture intricate relationships within medical images. This enhances precision in identifying patterns and anomalies, improving the speed and reliability of pathology image analysis. In this study, I explore the use of Vision Transformers and SWIN Transformers for pathology image analysis and compare their performance with traditional CNN models like EfficientNet.

  # Method
       
       Tranformer Models
          i. Vision Transformer Model
               1. Architecture
               2. Training
               3. Evaluations
               4. Gradient-weighted class activation mapping (Grad-CAM)
         ii. SWIN Transformer Model
               1.Architecture
               2. Training
               3. Evaluations
         iii. CNN Model
               1.Architecture
               2. Training
               3. Evaluations
  
# Results 
Calibration of Tranformer Models using Temperature Scaling Calibration

## Scope and Intent

This repository presents an applied machine learning case study using a public histopathology dataset.
The goal is not to introduce a novel method, but to demonstrate a clean, reproducible analysis pipeline
and transparent evaluation.


## Limitations

- The analysis is limited to patch-level classification and does not model spatial context across whole-slide images.
- Labels are derived from competition annotations rather than clinical outcomes.
- No external dataset was used for validation.

These limitations motivate future work in representation learning and cross-dataset generalization.


[1] B. S. Veeling, J. Linmans, J. Winkens, T. Cohen, M. Welling. "Rotation Equivariant CNNs for Digital Pathology". arXiv:1806.03962

[2] Ehteshami Bejnordi et al. Diagnostic Assessment of Deep Learning Algorithms for Detection of Lymph Node Metastases in Women With Breast Cancer. JAMA: The Journal of the American Medical Association, 318(22), 2199–2210. doi:jama.2017.14585
