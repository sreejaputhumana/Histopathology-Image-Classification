## Breast Cancer Histopathology-Image-Classification


# Introduction 
Analyzing pathology images is essential for accurate disease diagnosis and treatment but is often labor-intensive and inconsistent. Transformer-based models process large datasets and capture intricate relationships within medical images. This enhances precision in identifying patterns and anomalies, improving the speed and reliability of pathology image analysis. This project examines baseline CNN performance, and illustrates how transformer-based models (ViT, SWIN) and interpretability tools (Grad-CAM) can be integrated into a patch-level histopathology classification pipeline.
  # Method
### Data and Preprocessing

Image patches were obtained from a public histopathology dataset  PatchCamelyon (PCam) (1)(2) (Source**: https://github.com/basveeling/pcam )and resized to a
fixed input resolution prior to training. Standard normalization was applied, and
data were split into training and validation sets to ensure that evaluation was
performed on held-out samples.

All preprocessing steps were applied consistently across models.

### Training and Evaluation Protocol

Models were trained on the training split and evaluated exclusively on a held-out
validation set. Evaluation focused on patch-level binary classification performance
using accuracy and confusion matrices.

No test-set labels or external datasets were used for model selection or tuning.

### Models

#### i. Vision Transformer (Illustrative)
- Architecture
- Training 
- Evaluation (using model accuracy and confusion matrix)

#### ii. Swin Transformer
- Architecture
- Training
- Evaluation( using model accuracy and confusion matrix)

#### iii. CNN Baseline
- Architecture
- Training
- Evaluation( using model accuracy and confusion matrix)

### Interpretability
- Gradient-weighted Class Activation Mapping (Grad-CAM)

 
# Results

The models was evaluated on a held-out validation set using accuracy and confusion matrices. The confusion matrix provides insight into class-wise prediction behavior and highlights potential sources of misclassification. Among the evaluated architectures, the Swin Transformer achieved the strongest validation performance for patch-level benign vs malignant classification. Class-wise behavior was assessed using a confusion matrix to verify that performance was not driven by a single class.

To improve interpretability, Grad-CAM visualizations were generated for selected
validation images. The heatmaps highlight spatially localized regions within each
tissue patch that contribute most strongly to the model’s predictions, with minimal
activation in background areas.

Activation is concentrated around regions with dense cellular texture and strong
local color variation rather than being uniformly distributed across the image.
This suggests that model decisions are driven by structured visual features within
the patch rather than by global color or edge artifacts. Grad-CAM is used here as a
qualitative sanity check on model behavior and does not imply identification of
specific pathological structures or clinical relevance.


# Limitations

- This repository presents an applied machine learning case study using a public histopathology dataset. The analysis is limited to patch-level classification and does not model spatial context across whole-slide images.
- Labels are derived from competition annotations rather than clinical outcomes.
- No external dataset was used for validation.

These limitations motivate future work in representation learning and cross-dataset generalization.


[1] B. S. Veeling, J. Linmans, J. Winkens, T. Cohen, M. Welling. "Rotation Equivariant CNNs for Digital Pathology". arXiv:1806.03962

[2] Ehteshami Bejnordi et al. Diagnostic Assessment of Deep Learning Algorithms for Detection of Lymph Node Metastases in Women With Breast Cancer. JAMA: The Journal of the American Medical Association, 318(22), 2199–2210. doi:jama.2017.14585
