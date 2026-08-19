---
layout: default
---

# Learning-Based Single-Projection Multi-View Phase Unwrapping for Fringe Projection Profilometry

**Won-Hoe Kim¹, Seung-Geun Chi², and Jae-Sang Hyun¹**

¹ Department of Mechanical Engineering, Yonsei University
² School of Electrical and Computer Engineering, Purdue University

[Paper](PAPER_LINK) | [Dataset](https://www.dropbox.com/scl/fo/tj2zz3168nunw0zwm4a3r/AD_V8ZW130B8rNeGu5qGFak?rlkey=gm9e176947185c2djo9gbqli4&st=ust96qvy&dl=0)

## Overview

![Graphical abstract](asset/Graphical_Abstract.png)

We present a learning-based single-projection multi-view phase unwrapping method for fringe projection profilometry. Four synchronized cameras capture a single projected sinusoidal fringe pattern.

PRNet estimates the wrapped phase of each view, while PUNet estimates the reference-view absolute phase by aggregating phase-aligned multi-view evidence. PUNet is developed upon the coarse-to-fine iterative framework of [DI-MVS](https://github.com/JianfeiJ/DI-MVS), reformulating its depth-space inference for phase-domain estimation and incorporating wrapped-phase guidance, phase-plane-induced homography warping, and cross-view reprojection supervision.

The resulting framework combines global multi-view unwrapping information with local wrapped-phase details, enabling accurate and structurally consistent reconstruction using only a single temporal projection.

## Dataset

Our newly constructed synthetic dataset was generated in Blender using **6,300 diverse 3D object models** under a calibrated four-camera and one-projector configuration. It covers a wide range of object geometries and surface appearances for training and evaluating multi-view phase unwrapping methods.

[**Download Dataset**](https://www.dropbox.com/scl/fo/tj2zz3168nunw0zwm4a3r/AD_V8ZW130B8rNeGu5qGFak?rlkey=gm9e176947185c2djo9gbqli4&st=ust96qvy&dl=0)

### Representative Samples in the Dataset

![Representative dataset samples](asset/dataset_example.png)

## Results

Representative qualitative results are shown below. Our method compares favorably with conventional multi-view phase unwrapping and learning-based multi-view stereo methods adapted to the fringe-phase task.

![Qualitative results](asset/result.png)

## Citation

Citation information will be added upon publication.

## Acknowledgements

The implementation of PUNet is developed based on the publicly available [DI-MVS](https://github.com/JianfeiJ/DI-MVS) codebase. We thank the authors for releasing their code.
