# Multimodal Human Activity Recognition (Thermal + Pose)

## Overview

Privacy-preserving human activity recognition using thermal imagery and pose signals.  
This work studies how multimodal fusion improves robustness under low-visibility and privacy constraints.

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

Paper under review (Q1 journal)

---

## Note

Full code is not public due to ongoing research submission.  
Implementation details can be discussed upon request.