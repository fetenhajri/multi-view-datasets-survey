# Taxonomy of Multi-View Data

This document expands on **Section 2** of the paper: *"Taxonomy of Multi-View Data"*.

## Overview

In multi-view learning, real-world datasets contain multiple views representing different perspectives of the same data. These views provide complementary information and, when integrated, often lead to improved performance.

The taxonomy is organized along two main dimensions:

1. **Source-based classification** (platforms vs. sensors)
2. **Modality-based classification** (single-modal vs. multi-modal)

---

## 1. Source-Based Classification

The term *source* encompasses a broad range of origins, including sensors, databases, web platforms, and organizations.

### 1.1 Platforms

Platforms enable comprehensive data collection from multiple perspectives. Examples include:

| Platform Type | Examples |
|---------------|----------|
| Databases | Medical records, financial databases, academic databases |
| Web services | Social media platforms, e-commerce websites |
| Documents | Research papers, legal documents |
| Organizations | Company reports, research institutions |

### 1.2 Sensors

Sensors include cameras, LIDAR, RADAR, microphones, GPS, accelerometers, and other devices.

#### Homogeneous Multi-View Data

Multiple views derived from the **same feature space or modality** but captured from different perspectives.

**Example:** Temperature values collected from multiple sensors across a room.

**Characteristics:**
- Same data type across all views
- Different perspectives on the same phenomenon
- Simpler fusion compared to heterogeneous data

#### Heterogeneous Multi-View Data

Information originating from **different sources or feature spaces** that may differ in structure, format, or statistical distribution.

**Example:** Satellite imagery combined with weather station numerical measurements.

**Note:** Heterogeneity does NOT necessarily imply multi-modality. A dataset that integrates numerical sensor measurements with human-written reports is heterogeneous but not necessarily multi-modal.

---

## 2. Modality-Based Classification

### 2.1 Single-Modal Data

Characterized by uniformity, which simplifies data processing and analysis.

#### Images
- Captured from different viewpoints or angles at a specific moment
- **Applications:** 3D reconstruction, object recognition, photogrammetry
- **Key characteristics:**
  - Spatial relationships between views
  - Static analysis using CNNs
  - No temporal synchronization required

#### Videos
- Multiple video streams from different viewpoints
- Each view provides a sequence of frames
- **Applications:** 3D reconstruction, surveillance, sports analytics, VR
- **Key characteristics:**
  - Temporal synchronization required
  - Temporal dynamics (RNNs, 3D CNNs)
  - High storage and processing requirements

### 2.2 Multi-Modal Data

Encompasses information derived from multiple modalities with heterogeneous characteristics.

**Examples:**
- **Autonomous vehicles:** LIDAR + RADAR + camera data
- **Healthcare:** Patient records (text) + medical images (X-ray, MRI) + genomic information

**Key challenges:**
- Cross-modal alignment
- Synchronization of different data types
- Fusion of heterogeneous representations

---

## 3. Visual Representation
