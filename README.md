# GDMA-Net

**GDMA-Net: Geometric Prior-Driven Manifold and Topology-Aware Network for Pavement Crack Segmentation**

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8-blue.svg)]()
[![Framework](https://img.shields.io/badge/Framework-MMSegmentation%200.x-orange.svg)]()
[![PyTorch](https://img.shields.io/badge/PyTorch-1.9%2Bcu111-red.svg)]()

---

![GDMA-Net Architecture](figures/Fig_1.tif)

## 📖 Introduction

Accurate crack segmentation is essential for intelligent infrastructure maintenance, yet existing
methods face two persistent challenges: low-contrast crack tips that blur boundaries, and interwoven
branching structures that disrupt connectivity.

**GDMA-Net** introduces explicit geometric priors into the whole segmentation pipeline:

- **AGMP (Anisotropic Geometric Manifold Projection)**
- **TAFM (Topology-Aware Fusion Modulation)**
- **MGAL (Multi-dimensional Geometric Alignment Loss)**

On four pavement-crack datasets, GDMA-Net demonstrates that geometric priors precisely target the
structural essence of cracks, outperforming ten leading methods.

## 🆕 News

- **2026-10** — Initial code release.

## 📂 Datasets

Datasets are organized in the standard VOC layout. Place them under `dataset/`:

```
dataset/
└── DeepCrack/            # e.g. DeepCrack / Crack5K / CFD / GAPS384 / ...
    ├── JPEGImages/            # *.jpg input images
    ├── SegmentationClass/    # *.png binary masks (0=background, 1=crack)
    └── ImageSets/Segmentation/
        ├── trainval.txt       # training list (one image name per line)
        ├── val.txt
        └── test.txt
```

Supported datasets in this release: **DeepCrack, Crack5K, CFD, CrackTree260/CrackMap,
GAPS384, CRACK500, SUT-Crack**, and any custom dataset converted to the above VOC format.

## 📊 Evaluation

**mIoU, mDice, mRecall, BoundaryF1, SkeletonF1, CI (Connectivity Index)**.
