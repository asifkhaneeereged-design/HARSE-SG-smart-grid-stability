# HARSE-SG: Smart Grid Stability Assessment

[![DOI](https://img.shields.io/badge/DOI-10.1038%2Fs41598--026--75252--2-blue)](https://doi.org/10.1038/s41598-026-75252-2)
[![DOI](https://img.shields.io/badge/DOI-10.1016%2Fj.meaene.2026.100117-blue)](https://doi.org/10.1016/j.meaene.2026.100117)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Leakage-free and explainable **HARSE-SG** (Hybrid Adversarially Robust Stacking Ensemble for Smart Grid Stability Assessment) framework for robust smart grid stability assessment under cyber–physical disturbances.

---

## 📄 Publications

Both of the following peer-reviewed articles use the same dataset (`smart_grid_stability_augmented.csv`) provided in this repository:

1. **Explainable hybrid stacking ensemble for robust smart grid stability assessment under cyber–physical disturbances**<br>
   Abu Shufian, Md. Asif Khan, Rajin Al Fatemi, F. M. Mahir Daiyan, Md. Ashiquzzaman, Shaikh Anowarul Fattah — *Scientific Reports*, 16, Article 32080 (2026).<br>
   **DOI:** [10.1038/s41598-026-75252-2](https://doi.org/10.1038/s41598-026-75252-2)

2. **Physics-informed graph-attention feature fusion network for renewable-integrated smart grid stability assessment**<br>
   Abu Shufian, Md. Asif Khan, Rajin Al Fatemi, F. M. Mahir Daiyan, Shaikh Anowarul Fattah — *Measurement: Energy*, 12, Article 100117 (2026).<br>
   **DOI:** [10.1016/j.meaene.2026.100117](https://doi.org/10.1016/j.meaene.2026.100117)

If you use this dataset, please cite both papers. If you use a specific method, cite the corresponding paper (see [Citation](#-citation) below).

---

## 🔍 Overview

Modern smart grids depend on renewable generation, decentralized control, and communication-dependent monitoring, which makes reliable stability assessment difficult when measurements are noisy, incomplete, or manipulated. HARSE-SG addresses this with:

- **Leakage-free evaluation** – the target-derived stability index (`stab`) is excluded from the inputs.
- **Group-aware partitioning** – related augmented observations are kept in the same split to avoid optimistic bias.
- **Hybrid stacking** – Random Forest, Extra Trees, XGBoost, and CatBoost base learners combined through a Logistic Regression meta-learner trained on out-of-fold predictions.
- **Robustness testing** – evaluation under cyber–physical disturbance scenarios.
- **Explainability** – model-agnostic XAI analysis of feature contributions.

---

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `smart_grid_stability_augmented.csv` | Augmented smart grid stability dataset used in both studies |
| `CITATION.cff` | Citation metadata |
| `LICENSE` | MIT License |
| `README.md` | Project documentation |

---

## 📊 Dataset

The same dataset is used in both studies listed above: the HARSE-SG hybrid stacking framework (*Scientific Reports*) and the physics-informed graph-attention feature fusion network (*Measurement: Energy*).

The dataset is an augmented version of the Electrical Grid Stability Simulated Dataset (four-node star topology, Decentralized Smart Grid Control). Input features include reaction times (`tau1`–`tau4`), power values (`p1`–`p4`), and price-elasticity coefficients (`g1`–`g4`). The binary target is `stabf` (`stable` / `unstable`). The continuous `stab` column is **not** used as an input, to prevent target leakage.

---

## 📝 Citation

If you find this work useful, please cite:

```bibtex
@article{harsesg2026,
  title   = {Explainable hybrid stacking ensemble for robust smart grid stability assessment under cyber--physical disturbances},
  author  = {Shufian, Abu and Khan, Md. Asif and Al Fatemi, Rajin and Daiyan, F. M. Mahir and Ashiquzzaman, Md. and Fattah, Shaikh Anowarul},
  journal = {Scientific Reports},
  volume  = {16},
  pages   = {32080},
  year    = {2026},
  doi     = {10.1038/s41598-026-75252-2},
  url     = {https://doi.org/10.1038/s41598-026-75252-2}
}

@article{pigaffn2026,
  title   = {Physics-informed graph-attention feature fusion network for renewable-integrated smart grid stability assessment},
  author  = {Shufian, Abu and Khan, Md. Asif and Al Fatemi, Rajin and Daiyan, F. M. Mahir and Fattah, Shaikh Anowarul},
  journal = {Measurement: Energy},
  volume  = {12},
  pages   = {100117},
  year    = {2026},
  doi     = {10.1016/j.meaene.2026.100117},
  url     = {https://doi.org/10.1016/j.meaene.2026.100117}
}
```

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

## 📬 Contact

**Md. Asif Khan** – Research Centre for Green Energy, Electro-Anatomy, and Digital Intelligence (ReGED), Dhaka, Bangladesh<br>
GitHub: [@asifkhaneeereged-design](https://github.com/asifkhaneeereged-design)
