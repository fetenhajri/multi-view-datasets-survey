# Dataset Selection Guide

This document expands on **Section 5.5** of the paper: *"Dataset Selection Guidelines"*.

## Decision Framework

Use the following criteria to select the most appropriate multi-view dataset for your research:

### Step 1: Define Your Task

| Task Category | Recommended Dataset Types |
|---------------|--------------------------|
| 3D Reconstruction | Multi-view stereo, synthetic or real scans |
| Object Detection | Multi-camera, multi-modal (RGB + LiDAR) |
| Activity Recognition | Multi-view video with pose annotations |
| Crowd Analysis | Overlapping cameras, dense annotations |
| Autonomous Driving | 360° cameras, LiDAR, GPS |
| Medical Imaging | Volumetric (CT/MRI), cross-modal |
| Remote Sensing | Satellite, aerial, multi-temporal |

---

## Step 2: Consider Key Trade-Offs

### 2.1 Collection Cost vs. Generalization

| Domain | Collection Cost | Annotation Difficulty | Generalization |
|--------|---------------|----------------------|----------------|
| Autonomous Driving | Very High | Very High | Moderate |
| Medical Imaging | Very High | Very High | Low |
| Human Pose Estimation | Medium-High | High | Limited |
| Crowd Analysis | Low-Medium | Medium | Low-Moderate |
| Remote Sensing | High | Medium | Moderate |

### 2.2 Real vs. Synthetic

| Aspect | Real-World Datasets | Synthetic Datasets |
|--------|--------------------|--------------------|
| **Pros** | Realistic, no domain gap | Perfect ground truth, controllable |
| **Cons** | Noisy, expensive to annotate | Domain gap, less realistic |
| **Best for** | Deployment, real-world testing | Algorithm development, ablation studies |

**Examples of synthetic datasets:**
- GMVD [52], MultiviewX [53], CVCS [60], Synthehile [1]

---

## Step 3: Match by Application Domain

### Autonomous Driving

| Dataset | #Views | Modalities | Key Feature |
|---------|--------|------------|-------------|
| nuScenes [70] | 6 | RGB + LiDAR + Radar | 360° coverage |
| BDD100K [71] | 1 | RGB | 100K videos, diverse conditions |
| Argoverse [97] | 7 | RGB + LiDAR + GPS | 3D tracking + maps |
| Waymo Open [93] | 5 | RGB + LiDAR | Large scale, high quality |
| VoD [87] | 4 | RGB + LiDAR + Radar | Dutch urban scenes |

**Recommendation:** Start with **nuScenes** for BEV perception, **BDD100K** for diverse driving conditions.

---

### Activity Recognition

| Dataset | #Views | #Samples | Key Feature |
|---------|--------|----------|-------------|
| MVHumanNet [3] | 8-12 | 645M frames | Largest, text descriptions |
| Assembly101 [73] | 12 | 4,321 videos | Fine-grained actions |
| IKEA ASM [38] | 3 | 35 hours | Furniture assembly |
| HOMAGE [74] | 2-5 | 1.75K seq | 12 sensor types |

**Recommendation:** Use **MVHumanNet** for general activity recognition, **Assembly101** for procedural activities.

---

### 3D & 4D Reconstruction

| Dataset | Type | #Images | Ground Truth |
|---------|------|---------|--------------|
| BlendedMVS [43] | Synthetic | 17K | Depth maps, 3D models |
| CO3D [84] | Real | 1.5M | Camera poses, point clouds |
| MVImgNet [85] | Real | 6.5M | Masks, camera params |
| OmniObject3D [81] | Real | 6K objects | Meshes, point clouds |

**Recommendation:** **CO3D** for category-centric reconstruction, **BlendedMVS** for multi-view stereo.

---

### Crowd Analysis

| Dataset | #Views | #Frames | Density |
|---------|--------|---------|---------|
| WILDTRAK [56] | 7 | 400 annotated | ~24 people/frame |
| DroneCrowd [61] | 1 (drone) | 33,600 | 4.8M annotations |
| CityStreet [58] | 5 | 500 multi-view | Dense urban |
| MultiviewX [53] | 6 | 400 | 40 people/frame |

**Recommendation:** **WILDTRAK** for multi-camera tracking, **DroneCrowd** for aerial crowd counting.

---

### Medical Imaging

| Dataset | Modality | Size | Task |
|---------|----------|------|------|
| RadImageNet-VQA [102] | CT/MRI + QA | 7.5M pairs | Visual question answering |
| LIDC-IDRI [63] | CT | 1,018 scans | Lung nodule detection |
| DeepLesion [62] | CT | 32,735 lesions | Universal lesion detection |
| UniMed [104] | Multi-modal + Text | 1M pairs | Vision-language pre-training |

**Recommendation:** **RadImageNet-VQA** for medical VQA, **LIDC-IDRI** for nodule detection.

---

### Remote Sensing

| Dataset | Resolution | #Images | Task |
|---------|-----------|---------|------|
| xView [64] | 0.3m | 1M objects | Object detection |
| DOTA-v2.0 [65] | Varies | 11,268 | Oriented object detection |
| SpaceNet 8 [67] | 0.3-0.5m | 850 km² | Change detection |
| OmniCity [106] | Multi-scale | 100K+ | Cross-view understanding |

**Recommendation:** **xView** for general object detection, **SpaceNet** for temporal change detection.

---

## Step 4: Check Dataset Quality Criteria

Before selecting a dataset, verify:

- ✅ **Public availability** (links in Appendix B.3)
- ✅ **Explicit multi-view properties** (≥2 views or modalities)
- ✅ **Sufficient documentation** (camera parameters, annotations)
- ✅ **Release date ≥ 2018** (per survey scope)

---

## Step 5: Use Our Decision Flowchart

Refer to **Fig. 2** in the paper or in the main README for a visual decision tree.
