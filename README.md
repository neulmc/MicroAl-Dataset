# MicroAl-Dataset

🎉 **News:** Our paper **Shape2Mask: A Weakly Supervised Instance Segmentation Method for Aluminum Alloy Precipitations Based on Prior Shape Knowledge** has been published in *IEEE Transactions on Instrumentation and Measurement* (TIM). [[View Paper]](https://ieeexplore.ieee.org/document/11449477)

A curated dataset of aluminum alloy microstructures under weak annotations, supporting research in visual perception and measurement for materials science.

## 📖 Overview

MicroAl-Dataset is a collection of aluminum alloy microstructural images captured at both micron and nano scales, including:

- **Micron-scale**: Micron-scale: Si particles, Al grains, Fe-bearing phases, and other intermetallic compounds (optical microscopy, SEM)
- **Nano-scale**: Precipitates (TEM)

For detailed descriptions, representative images, and annotation examples, please refer to:
[`docs/description.pdf`](./docs/description.pdf) - Detailed dataset description and visualization.

The dataset is designed to facilitate research on **deep learning** for industrial vision applications, addressing the challenge of high annotation costs in materials science.

## 🗂️ Dataset Structure
```
MicroAl-Dataset/
├── Metallo/                   # Metallographic Microscope Images
│   ├── Pre-heat-treated/        # Pre-heat-treated images: Si particles, Fe-bearing phases
│   │   ├── pre-img/               # Metallographic images (1 pixel = 0.1 μm)
│   │   └── pre-gt/                # Second-phase segmentation labels 
│   ├── Heat-treated/            # Heat-treated images: grains, Si particles
│   │   ├── image/                 # Metallographic images (1 pixel = 0.1 μm)
│   │   ├── mask/                  # Si particle segmentation labels 
│   │   └── label/                 # Al grain boundary detection labels 
│   ├── Nanshan/                 # Nanshan alloy metallographic images
│   │   ├── As-cast/                  # As-cast aluminum alloys [sample only, pending authorization]
│   │   └── Film-coated/              # Film-coated aluminum grain [sample only, pending authorization]
│   └── NEU-As-cast/             # NEU as-cast aluminum images
│       ├── 5xxx/                  # 5xxx series alloys [sample only, annotation in progress]
│       └── 6xxx/                  # 6xxx series alloys [sample only, annotation in progress]
├── Electron/                  # Electron Microscope Images
│   ├── TEM image/               # TEM images of nano-scale precipitates
│   │   ├── TEM-img/               # TEM images (1 pixel = 0.16 nm)
│   │   └── annotation/            # Precipitate instance segmentation labels 
│   ├── TEM dark-field image/    # TEM dark-field images of nano-scale precipitates [sample only, annotation in progress]
│   ├── HRTEM image/              # HRTEM images for precipitate phase identification [sample only, annotation in progress]
│   └── Nanshan SEM image/        # SEM images of Nanshan aluminum alloy microstructures [sample only, pending authorization]
└── docs/
    └── description.pdf          # Detailed dataset description
```
## 🏷️ Annotation Types

Following the taxonomy of weakly supervised learning, three types of weak annotations are provided:

| Type | Description | Format                             |
|------|-------------|------------------------------------|
| Inaccurate | Annotator disagreements or ambiguous boundaries | Fuzzy labels per region            |
| Incomplete | Only partial pixels/regions annotated | Sparse pixel-wise labels           |
| Inexact | Coarse-grained annotations | Bounding boxes or image-level tags |
| **Standard** | Fully annotated with precise pixel-wise labels by domain experts | Dense pixel-wise masks             |

## 🎯 Intended Use

This dataset is intended for:

- Developing fully/weakly supervised learning methods for microstructure analysis
- Benchmarking visual perception models under limited/imperfect annotations
- Exploring uncertainty estimation and domain knowledge integration in materials science

## 📊 Statistics

| Dataset | Task | Images | Category | Annotation Type                        |
|---------|------|--------|------------|----------------------------------------|
| Pre-heat-treated | Semantic Segmentation | 1584   | Si particles / Fe-bearing phases (micron) | Inaccurate/ Incomplete/ Standard       |
| Heat-treated | Boundary Detection / Semantic Segmentation | 1400   | Al grains/ Si particles (micron) | Inaccurate/ Incomplete/ Standard       |
| TEM image | Instance Segmentation | 330    | Precipitates (nano) | Inaccurate/ Inexact/ Incomplete/ Standard |

The datasets listed in the table above are fully publicly available. 
Additional datasets in this repository, including images, annotations, and corresponding statistics, 
will be continuously updated upon the completion of data acquisition, 
**expert annotation**, and **necessary authorizations**. 
Please stay tuned for further releases.

## 📚 Citation

We hope this dataset benefits your research. If you use it, please cite our papers and give this repository a star ⭐. 
Thanks for your support!

```bibtex
@article{li2023semisupervised,
  title={Semisupervised boundary detection for aluminum grains combined with transfer learning and region growing},
  author={Li, Mingchun and Chen, Dali and Liu, Shixin and Liu, Fang},
  journal={IEEE Transactions on Neural Networks and Learning Systems},
  volume={34},
  number={9},
  pages={6158--6172},
  year={2023},
  publisher={IEEE}
}

@article{li2021prior,
  title={Prior mask R-CNN based on graph cuts loss and size input for precipitation measurement},
  author={Li, Mingchun and Chen, Dali and Liu, Shixin and Liu, Fang},
  journal={IEEE Transactions on Instrumentation and Measurement},
  volume={70},
  pages={1--15},
  year={2021},
  publisher={IEEE}
}

@article{li2025uncertainty,
  title={Uncertainty estimation method based on Dirichlet distribution for microstructure segmentation and measurement in aluminum alloy metallographic images},
  author={Li, Mingchun and Liu, Yang and Chen, Dali and Wang, Qiang},
  journal={Measurement},
  volume={246},
  pages={116744},
  year={2025},
  publisher={Elsevier}
}
```

## 📄 License & Access

This dataset is provided **for academic research purposes only**. Commercial use is strictly prohibited without prior written authorization from the data owners.

**Data Ownership**:  
The images and annotations contained in this dataset are jointly owned by **Northeastern University, Shenyang University, and Shandong Nanshan Aluminum Co., Ltd.** Unauthorized distribution, reproduction, or commercial use is not permitted.

**Current Release**:  
- **Google Drive**: https://drive.google.com/file/d/1lh3QeOb6iy1B9NJHq32pt1nBvyuBOUDv/view?usp=sharing
- **Baidu Netdisk**: [https://pan.baidu.com/s/1My7PmglxRcJCKeTPTqwagw](https://pan.baidu.com/s/1My7PmglxRcJCKeTPTqwagw) (Extraction code: `mico`) 

Please note that this is a **sample release** for reference only. The **full public version** will be released upon the publication of related papers.

**Early Access**:  
If you have an urgent need for the complete dataset, feel free to contact us  with a brief introduction of your research purpose. We are happy to share the full dataset with qualified academic researchers.
Alternatively, you may explore our previously released datasets and code repositories listed in the [References](#references) section below.

## 📧 Contact

For questions or collaboration opportunities, please contact: limingchun_cn@qq.com

## References (our available datasets)
To support open research and reproducible science, 
**we have been actively working in this direction over the past three years**, 
publicly releasing several microstructure image datasets and the corresponding code repositories from our previous studies, as listed below.
If you find these resources helpful, please consider citing our related papers.

[1] <a href="https://github.com/CHENDL-SHEN/SemiRCF"> **[2023 TNNLS]** (Heat-treated dataset) Semi-Supervised Boundary Detection for Aluminum Grains Combined with Transfer Learning and Region Growing  </a>

[2] <a href="https://github.com/neulmc/BetaNet"> **[2023 Knowl. Based Syst.]** (Natural image dataset) Beta Network for Boundary Detection under Nondeterministic Labels.</a>

[3] <a href="https://github.com/neulmc/Shape2Mask"> **[2026 TIM]** (TEM image dataset) Shape2Mask: A Weakly Supervised Instance Segmentation Method for Aluminum Alloy Precipitations Based on Prior Shape Knowledge.</a>

[4] <a href="https://github.com/neulmc/PSCL"> **[2026 SR]** (Pre-heat-treated dataset) Patch-Sampled Contrastive Learning for Dense Prediction Pretraining in Metallographic Images.</a>

[5] <a href="https://github.com/neulmc/dir-network"> **[2025 Measurement]** (Pre-heat-treated dataset) Dirichlet Network for Microstructure Segmentation of Aluminum Alloy </a>
