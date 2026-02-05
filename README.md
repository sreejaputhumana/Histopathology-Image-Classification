## Breast Cancer Histopathology-Image-Classification

# Dataset
- **Dataset**: PatchCamelyon (PCam) (1)(2)
- **Source**: https://github.com/basveeling/pcam

# Introduction 
Analyzing pathology images is essential for accurate disease diagnosis and treatment but is often labor-intensive and inconsistent. Transformer-based models process large datasets and capture intricate relationships within medical images. This enhances precision in identifying patterns and anomalies, improving the speed and reliability of pathology image analysis. This project examines baseline CNN performance, and illustrates how transformer-based models (ViT, SWIN) and interpretability tools (Grad-CAM) can be integrated into a patch-level histopathology classification pipeline.
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

The model was evaluated on a held-out validation set using accuracy and confusion matrices. The confusion matrix provides insight into class-wise prediction behavior and highlights potential sources of misclassification. 

To improve interpretability, Grad-CAM visualizations were generated for selected validation images. These visualizations highlight image regions that contributed most strongly to the model’s predictions and provide a qualitative check on whether the model attends to localized tissue patterns rather than background artifacts.

The Grad-CAM results are intended for model interpretability and sanity checking only. They do not establish biological or clinical significance. All results reflect patch-level classification performance and should be interpreted within this methodological scope.


# Limitations

- This repository presents an applied machine learning case study using a public histopathology dataset. The analysis is limited to patch-level classification and does not model spatial context across whole-slide images.
- Labels are derived from competition annotations rather than clinical outcomes.
- No external dataset was used for validation.

These limitations motivate future work in representation learning and cross-dataset generalization.


[1] B. S. Veeling, J. Linmans, J. Winkens, T. Cohen, M. Welling. "Rotation Equivariant CNNs for Digital Pathology". arXiv:1806.03962

[2] Ehteshami Bejnordi et al. Diagnostic Assessment of Deep Learning Algorithms for Detection of Lymph Node Metastases in Women With Breast Cancer. JAMA: The Journal of the American Medical Association, 318(22), 2199–2210. doi:jama.2017.14585
