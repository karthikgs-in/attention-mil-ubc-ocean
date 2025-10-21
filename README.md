# 🧠 Attention Based Multiple Instance Learning for Generalizing on the UBC-OCEAN Dataset
## Ovarian Cancer Subtype Classification and Outlier Detection (OCEAN)

### 📍 Project Overview
This repository contains the implementation and materials for my **M.Tech (AI & DS)** final project at **SRM Institute of Science and Technology (SRMIST)**, guided by **Dr. S. Ganesh Kumar**.  
The work was presented and published in the **Proceedings of ICMBNT 2025** under the title *"Optimizing an Attention-based MIL Architecture for Generalizing on the UBC-OCEAN"*.

---

### 🧩 Abstract
> Early and accurate diagnosis of epithelial ovarian cancer is crucial for timely intervention. AI-driven subtype classification addresses subjective variability in histopathological assessment and is key to treatment management. To improve applicability, rare subtypes need to be flagged as outliers. Whole slide images (WSIs) and Tissue Microarray (TMA) images from the UBC-OCEAN dataset were used for ovarian cancer subtyping. WSIs are large (600MB+) with sparsely distributed disease tissue, requiring careful feature extraction and use.  
> Multiple Instance Learning (MIL), a form of weakly supervised learning, enables generalization on such datasets. Neural approaches like Attention-based MIL (ABMIL) offer interpretability and performance advantages. This work presents results from an optimized architecture using a **double Vision Transformer (ViT) backbone** pretrained on diverse pathology datasets with **self-supervised learning (Lunit DINO)**. The approach generalizes effectively to the diverse, unseen test set of the UBC-OCEAN dataset.

---

### ⚙️ Key Insights
- Implemented and optimized an **Attention-based MIL (ABMIL)** architecture using **double Vision Transformer (ViT) backbones** with patch sizes 8×8 and 16×16.  
- Demonstrated improvement from a **[baseline](https://www.kaggle.com/code/skarthikguruswamy/inceptionv3-tl-classifier) private score of 0.26** (rank 855/1326) to **0.42**, matching the **top 10%** of the Kaggle leaderboard (ranks 132–159).  
- Leveraged **self-supervised pretrained pathology weights (Lunit DINO)** to enhance generalization without additional compute.  
- Utilized **entropy-based outlier detection** for rare ovarian cancer subtypes.  
- Achieved results aligned with **UN SDG 3 (Health)** and **SDG 10 (Reduced Inequalities)** by improving diagnostic generalization across global datasets.

---

### 🧰 Skills and Technologies
| Category | Tools / Libraries |
|-----------|------------------|
| **Languages** | Python |
| **Frameworks** | PyTorch, scikit-learn, timm, NumPy, pandas, OpenCV, pyvips |
| **ML Concepts** | Multiple Instance Learning, Attention Mechanisms, Transfer Learning, Vision Transformers |
| **Domains** | Medical Imaging, Weakly Supervised Learning |
| **Visualization** | Matplotlib |
| **Deployment / Collaboration** | Kaggle Notebooks |

---

### 🧪 Dataset
**UBC-OCEAN Dataset**  
A large-scale ovarian cancer histopathology dataset comprising Whole Slide Images (WSI) and Tissue Microarrays (TMA) from over 20 centers worldwide.  
- Publicly available at: [UBC-OCEAN on Kaggle](https://www.kaggle.com/competitions/UBC-OCEAN/data)  
- Challenge objective: Subtype classification and outlier detection.  
- Balanced accuracy on unseen private test set used as evaluation metric.  
- Dataset licensed for research use only.

---

### 📊 Results Summary

| Model | Public Test Score | Private Test Score | Validation Balanced Accuracy |
|--------|------------------|--------------------|------------------------------|
| **Baseline (InceptionV3, 512×512)** | 0.27 | 0.24 | 0.54 |
| **ABMIL (InceptionV3, 384×384, 20 tiles)** | 0.36 | 0.33 | 0.72 |
| **ABMIL (Double ViT, Lunit DINO, 100 tiles)** | 0.42 | 0.35 | 0.78 |
| **ABMIL (Double ViT, Lunit DINO, 400 tiles optimized)** | 0.48 | **0.42** | 0.77 |

🟢 **Improvement:** Baseline private score **0.26 → 0.42**, equivalent to **top 10% of leaderboard (ranks 132–159/1326).**


---

### 🔗 External Resources
- **Conference Paper:** [ICMBNT 2025 Proceedings PDF](paper/ICMBNT25_KarthikGS_DrGanesh_paper.pdf)  
- **Presentation:** [Final_Presentation.pdf](presentation/abmil-ocean-final-ppt.pdf)  
- **Kaggle Notebooks:**  
  - [Training Notebook](https://www.kaggle.com/code/skarthikguruswamy/jan16-inf-attmil-lunit-224-400tiles-29c766)  
  - [Best Inference Notebook](https://www.kaggle.com/code/skarthikguruswamy/fork-of-jan9-train-attmil-lunit-224-400tile-f5dd51)  
- **LinkedIn Project:** [LinkedIn Project Link](https://www.linkedin.com/in/karthikgs/details/projects/)

---

### 📚 References
1. Ilse, M., Tomczak, J.M., & Welling, M. (2018). *Attention-based Deep Multiple Instance Learning.* ICML.  
2. Kang, M., et al. (2023). *Benchmarking self-supervised learning on diverse pathology datasets.* CVPR.  
3. Courtiol, P., et al. (2019). *Deep learning-based classification of mesothelioma improves prediction of patient outcome.* Nature Medicine.  
4. Asadi-Aghbolaghi, M., et al. (2024). *Machine Learning-driven Histotype Diagnosis of Ovarian Carcinoma: Insights from the OCEAN AI Challenge.* medRxiv.  
5. Breen, J. et al. (2024). *Histopathology Foundation Models Enable Accurate Ovarian Cancer Subtype Classification.* arXiv:2405.09990.  
[Full citation list available in published paper above.]

---

### 🙏 Acknowledgments
- **Guide:** Dr. S. Ganesh Kumar, Department of Data Science and Business Systems, SRMIST  
- **Institution:** SRM Institute of Science and Technology (SRMIST), Kattankulathur  
- **Conference:** ICMBNT 2025, Society for Cyber Intelligent Systems, Puducherry  
- **Dataset Provider:** UBC-OCEAN Research Team, University of British Columbia  

---

### 🧾 License
This repository is shared for academic and educational use.  
For dataset usage and derivative works, please follow the original dataset’s license and citation requirements.
