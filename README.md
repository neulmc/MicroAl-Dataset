# MicroAl-Dataset

A curated dataset of aluminum alloy microstructures under weak annotations, supporting research in visual perception and measurement for materials science.

## 📖 Overview

MicroAl-Dataset is a collection of aluminum alloy microstructural images captured at both micron and nano scales, including:

- **Micron-scale**: Si particles and Al grains (optical microscopy, SEM)
- **Nano-scale**: Precipitates (TEM)

The dataset is designed to facilitate research on **weakly supervised learning** for industrial vision applications, addressing the challenge of high annotation costs in materials science.

## 🗂️ Dataset Structure

MicroAl-Dataset/
├── micron/
│   ├── si_particles/     # SEM images of Si particles
│   ├── al_grains/        # Optical images of Al grains
│   └── annotations/      # Weak annotations (inaccurate/incomplete/inexact)
├── nano/
│   ├── precipitates/     # TEM images of nano-scale precipitates
│   └── annotations/      # Weak annotations
└── docs/
    └── description.pdf   # Detailed dataset description

## 🏷️ Annotation Types

Following the taxonomy of weakly supervised learning, three types of weak annotations are provided:

| Type | Description | Format |
|------|-------------|--------|
| Inaccurate | Annotator disagreements or ambiguous boundaries | Multiple labels per region |
| Incomplete | Only partial pixels/regions annotated | Sparse pixel-wise labels |
| Inexact | Coarse-grained annotations | Bounding boxes or image-level tags |

## 🎯 Intended Use

This dataset is intended for:

- Developing weakly supervised learning methods for microstructure analysis
- Benchmarking visual perception models under limited/imperfect annotations
- Exploring uncertainty estimation and domain knowledge integration in materials science

## 📊 Statistics

| Category | #Images | Resolution | Annotation Type |
|----------|---------|------------|-----------------|
| Si particles (micron) | XXX | 1024×1024 | Inaccurate / Incomplete |
| Al grains (micron) | XXX | 1024×1024 | Inexact / Incomplete |
| Precipitates (nano) | XXX | 2048×2048 | Inaccurate / Inexact |

Detailed statistics will be updated upon publication.

## 🔗 Access

The dataset is available upon request for research purposes. Please submit an access request via GitHub Issues or contact the authors.

## 📚 Citation

If you use this dataset in your research, please cite:

@dataset{yourname2025microal,
  title={MicroAl-Dataset: A Weakly Annotated Aluminum Alloy Microstructure Dataset},
  author={Your Name},
  year={2025},
  publisher={GitHub},
  url={https://github.com/yourname/MicroAl-Dataset}
}

## 📄 License

This dataset is provided for academic research purposes only. Commercial use is not permitted without prior authorization.

## 📧 Contact

For questions or collaboration opportunities, please contact: your-email@example.com.
