# Multi-View Datasets Survey (The Visual Computer 2026)
An extensive collection of more than 120 multi-view datasets with links, modalities, and applications. Companion resource for The Visual Computer paper.

[![DOI](https://img.shields.io/badge/DOI-10.1007/s00371-026-xxxxx-blue)](https://doi.org/10.1007/s00371-026-xxxxx)
[![Paper](https://img.shields.io/badge/Paper-Springer-red)](https://link.springer.com/article/xxx)
[![Datasets](https://img.shields.io/badge/Datasets-120-green)](datasets.csv)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey)](LICENSE)

> **A Comprehensive Review of Multi-View Datasets and Applications**  
> *Feten Hajri,  Hajer Fradi and Mohamed Ali Mahjoub*  
> *The Visual Computer, 2026*

This repository provides a **living resource** of multi-view datasets for computer vision research, accompanying our survey paper. It includes all datasets reviewed (2018–2025), organized by modality, application, and cross-modal annotations.

---

## 📚 What is this repository?

Our survey identified **120 public multi-view datasets** published since 2018. This repository provides:

- ✅ A **searchable CSV file** of all datasets with links, modalities, and tasks
- ✅ A **decision flowchart** (Fig. 2) to select the right dataset
- ✅ **Cross-modal annotation tables** for vision-language research
- ✅ **Domain-specific recommendations** (autonomous driving, medical, crowd analysis, etc.)

---

## 📚 Table of Contents

- [Quick Overview](#quick-overview)
- [Dataset Statistics](#dataset-statistics)
- [Dataset Selection Decision Framework](#dataset-selection-decision-framework)
- [Repository Contents](#repository-contents)
- [How to Use This Resource](#how-to-use-this-resource)
- [Domain-Specific Recommendations](#domain-specific-recommendations)
- [Cross-Modal Annotations](#cross-modal-annotations)
- [How to Cite](#how-to-cite)

## 📚 Table of Contents

- [Quick Overview](#quick-overview)
- [Dataset Statistics](#dataset-statistics)
- [Dataset Selection Decision Framework](#dataset-selection-decision-framework)
- [Repository Contents](#repository-contents)
- [How to Use This Resource](#how-to-use-this-resource)
- [Domain-Specific Recommendations](#domain-specific-recommendations)
- [Cross-Modal Annotations](#cross-modal-annotations)
- [How to Cite](#how-to-cite)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
------

## 📊 Quick Overview
#quick-overview

| Category | Number of Datasets | Key Applications |
|----------|-------------------|------------------|
| 🖼️ Single-modality Images | ~15 | 3D reconstruction, novel view synthesis |
| 🎥 Single-modality Videos | ~50 | Activity recognition, surveillance, sports |
| 🔀 Multi-modal | ~45 | Autonomous driving, medical imaging, robotics |
| 🏥 Medical | ~7 | CT/MRI analysis, VQA |
| 🛰️ Remote Sensing | ~6 | Aerial/Satellite object detection |
| **TOTAL** | **~120+** | |

---

## 📈 Dataset Statistics

- **120+ datasets** reviewed
- **Release years:** 2018–2025
- **Most represented applications:** 
  - Autonomous driving (12+)
  - Activity recognition (10+)
  - 3D reconstruction (9+)
  - Crowd analysis (8+)
  - Medical imaging (7+)
- **Fastest growing category:** Multi-modal vision-language (2023–2025)

---

## 🗺️ Dataset Selection Decision Framework

Use our decision flowchart (Fig. 2 from the paper) to select the right dataset:

📌 **All dataset names include reference numbers** to locate descriptions in the paper.

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| [`datasets.csv`](datasets.csv) | **Master list** of 120+ datasets with columns: Name, Year, Modality, Application, #Views, Resolution, Overlap, Link |
| [`tables/table1_single_modality.csv`](tables/table1_single_modality.csv) | Single-modality image & video datasets (Table 1 from paper) |
| [`tables/table2_multi_modality.csv`](tables/table2_multi_modality.csv) | Multi-modal datasets (Table 2 from paper) |
| [`tables/table13_cross_domain.csv`](tables/table13_cross_domain.csv) | Cross-domain comparison (Table 13) |
| [`tables/table14_cross_modal.csv`](tables/table14_cross_modal.csv) | Cross-modal annotations for vision-language reasoning (Table 14) |
| [`docs/taxonomy.md`](docs/taxonomy.md) | Full taxonomy of multi-view data (Section 2) |
| [`docs/selection-guide.md`](docs/selection-guide.md) | Detailed guidelines for dataset selection (Section 5.5) |
| [`docs/future-directions.md`](docs/future-directions.md) | Future research directions (Section 6) |
| [`assets/fig1_taxonomy.png`](assets/fig1_taxonomy.png) | Multi-view data taxonomy diagram |
| [`assets/fig2_decision_flowchart.png`](assets/fig2_decision_flowchart.png) | Dataset selection flowchart |

---

## 🔍 How to Use This Resource

### 1. Find a dataset for your task
- Open [`datasets.csv`](datasets.csv) and filter by "Application" column
- Or follow the decision flowchart above
- Or check domain-specific recommendations below

### 2. Get the dataset
- Click the official link in the "Repository" column of the CSV
- Links are also available in Appendix B.3 of the paper

### 3. Understand the dataset's limitations
- Check Tables 3-12 in the paper for strengths/limitations analysis

---

## 🎯 Domain-Specific Recommendations

| Domain | Recommended Datasets | Key Characteristics |
|--------|---------------------|---------------------|
| **Autonomous Driving** | nuScenes [70], BDD100K [71], Argoverse [97] | 360° cameras, LiDAR, radar, GPS |
| **3D Reconstruction** | BlendedMVS [43], CO3D [84], MVImgNet [85] | Multi-view stereo, point clouds, meshes |
| **Activity Recognition** | MVHumanNet [3], Assembly101 [73], HOMAGE [74] | Multi-view video, pose, actions |
| **Medical Imaging** | RadImageNet-VQA [102], UniMed [104], LIDC-IDRI [63] | CT, MRI, X-ray, VQA pairs |
| **Crowd Analysis** | WILDTRAK [56], DroneCrowd [61], CityStreet [58] | Dense crowds, multi-camera tracking |
| **Remote Sensing** | xView [64], DOTA-v2.0 [65], SpaceNet 8 [67] | Satellite, aerial, multi-temporal |
| **Anomaly Detection** | MVTec 3D-AD [99], UCSD [33] | Industrial defects, crowd anomalies |

---

## 🔗 Cross-Modal Annotations
#cross-modal-annotations
Datasets that support vision-language and multi-modal reasoning:

| Dataset | Modalities | Annotation Type |
|---------|-----------|----------------|
| MVHumanNet [3] | RGB + Text | Human masks, SMPL parameters, text descriptions |
| RadImageNet-VQA [102] | CT/MRI + QA pairs | 7.5M medical question-answer pairs |
| EmbodiedScan [72] | RGB-D + Language | 3D boxes, semantic occupancy, language prompts |
| Assembly101 [73] | RGB + Depth | Fine-grained actions, 3D hand poses |
| UniMed [104] | Multi-modal medical + Text | 1M image-text pairs |

---

## 📖 How to Cite

If you use this resource for your research, please cite our paper:

```bibtex
@article{hajri2026comprehensive,
  title={A Comprehensive Review of Multi-View Datasets and Applications},
  author={Hajri, Feten and [other authors]},
  journal={The Visual Computer},
  year={2026},
  publisher={Springer}
}
## 🤝 Contributing

This is a **living resource**. To add a new multi-view dataset or correct an entry:

1. Open an issue or pull request
2. Provide: Name, year, modality, application, number of views, resolution, and official link
3. We will verify and update

**Note:** Only datasets that are:
- ✅ Publicly available
- ✅ Multi-view (at least 2 views/modalities)
- ✅ Published after 2018
- ✅ Well documented

### How to contribute a new dataset

You can contribute by:
- **Creating an issue** with the dataset details
- **Submitting a pull request** adding the dataset to `datasets.csv`

---

## 📜 License

This repository is under **CC BY-NC 4.0** (attribution, non-commercial). 

The paper is published by Springer under their copyright policy.

You are free to:
- **Share** — copy and redistribute the material
- **Adapt** — remix, transform, and build upon the material

Under the following terms:
- **Attribution** — You must give appropriate credit
- **NonCommercial** — You may not use the material for commercial purposes

---

## ✉️ Contact

**Corresponding author:** Feten Hajri  
📧 feten.hajri@isitcom.u-sousse.tn

**Institution:**  
University of Sousse  
Higher Institute of Computer Science and Communication Technologies (ISITCom)  
Sousse, Tunisia

**Co-authors:** (add your co-authors' affiliations as needed)

### Connect with us:
- GitHub Issues: For questions about the repository
- Email: For direct correspondence about the paper

---

## ⭐ Star this repo

If you find this resource useful for your research, please **star** this repository and share it with colleagues!
