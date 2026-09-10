# Privacy-Preserving Human Activity Recognition with Thermal Imagery and Pose Cues
## Overview

Privacy-preserving human activity recognition using thermal imagery and pose signals.  
This work studies how multimodal fusion improves robustness under low-visibility and privacy constraints

## Repository Structure

```
notebooks/
├── Multimodal_Framework.ipynb
└── Unimodal_Benchmarking_Framework.ipynb
```

### Multimodal_Framework.ipynb

Implements the complete multimodal learning framework, including multimodal fusion methods, training, evaluation, and experiment management.

### Unimodal_Benchmarking_Framework.ipynb

Implements the benchmarking framework for unimodal thermal and pose models, including baseline architectures, loss function comparisons, classifier evaluation, profiling, and multi-seed experiments.

---

## Problem

Conventional HAR relies on RGB data, which introduces privacy concerns and degrades under poor lighting conditions.  
Thermal and pose provide complementary privacy-preserving signals, but effective integration remains underexplored.

---

## Approach

- Thermal encoder + pose encoder for complementary representation learning  
- Controlled multimodal benchmarking with multi-seed evaluation  
- Confidence-aware fusion mechanisms:
  - CGCA (Confidence-Gated Cross-Attention)  
  - CGHCA (Confidence-Gated Hierarchical Co-Attention)  
- Explicit modeling of modality reliability during fusion  

![Pipeline](assets/har_pipeline.png)

---

## Results

- Pose-only: **75.03% / 63.96%** (6-class / 8-class)  
- Thermal-only: **86.05% / 82.87%**  
- Multimodal (Ours):
  - **86.18% (CGHCA, 6-class)**  
  - **84.15% (CGCA, 8-class)**  

Consistent improvement over unimodal baselines with low variance across seeds.

![Results](assets/har_results.png)

# Data Availability

This work builds upon the publicly available **IS2AI Open Thermal Pose** dataset and extends it with new activity annotations for human activity recognition.

**Original Dataset**
- IS2AI Open Thermal Pose Dataset (public): https://github.com/IS2AI/OpenThermalPose

The original thermal images and pose annotations are available from the official IS2AI repository.

The additional **6-class and 8-class activity annotations**, together with the preprocessing pipeline introduced in this work, are not currently distributed through this repository.

These research artifacts are available from the authors upon reasonable request.

Please cite both the original IS2AI dataset and our paper when using the extended annotations.
---

## Key Insight

Multimodal gains arise from **complementary representations**, not just fusion complexity.  
Reliability-aware attention improves robustness under modality uncertainty.

---

## Contribution

- Systematic benchmark for thermal–pose multimodal HAR  
- Confidence-aware fusion (CGCA, CGHCA)  
- Demonstration of structured modality complementarity  

---
## Status
 First-author publication in *Knowledge-Based Systems* (2026)
 **Paper** : *Multimodal Learning With Thermal Imagery and Pose Cues for Privacy-Preserving Behaviour Recognition*

**DOI:** `10.1016/j.knosys.2026.116659`

**Paper:** [ScienceDirect]
(https://www.sciencedirect.com/science/article/pii/S0950705126013857)



# Citation

If you find this work useful, please cite:

```bibtex
The BibTeX citation will be added after the paper is published online.
```

---
## Note

This repository contains the complete implementation of the unimodal and multimodal learning frameworks presented in our paper.

The extended activity annotations introduced in this work are not included in this repository. Please refer to the **Data Availability** section for details.