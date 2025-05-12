# SocioDiff Codebase

This repository contains the source code for our paper:

> **SocioDiff: A Socio-aware Diffusion Model for Residential Load Data Generation**  
> *(Under review)*

SocioDiff is a conditional diffusion model that generates realistic electricity consumption time series conditioned on structured socio-demographic information. It is specifically designed to address data scarcity and representational bias in underrepresented communities, and supports fairness-aware data generation for smart grid research.

---

## 📌 Key Features

- Conditional diffusion framework integrating social attributes
- Two-step generation mechanism: global trend + household-specific refinement
- Fairness-aware adversarial training for disadvantaged groups
- Compatible with real-world load datasets (e.g., Irish CER dataset)

---

## 📁 Repository Structure

```

├── src/                     # Core model components and training pipeline
│   ├── models/              # Diffusion and denoising networks (4SD)
│   ├── utils/               # Preprocessing, metrics, and functions
│   └── train.py             # Training entry point
├── configs/                 # Training configuration files
├── scripts/                 # Shell scripts for running experiments
├── requirements.txt         # Required Python packages
└── README.md

````

---

## 🧪 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Intelligame/SocialDiff_code.git
cd SocialDiff_code
````

### 2. Create environment and install dependencies

```bash
conda create -n sociodiff python=3.10
conda activate sociodiff
pip install -r requirements.txt
```

### 3. Prepare dataset

* The synthetic dataset used for evaluation can be found at
  🔗 [https://github.com/Intelligame/SocialDiff](https://github.com/Intelligame/SocialDiff)
* To use other datasets, ensure they are formatted as `.csv` files with socio-demographic fields and normalized load sequences.

### 4. Run training

```bash
python train.py --config configs/sociodiff.yaml
```

---

## 📊 Evaluation

We provide evaluation metrics including:

* Maximum Mean Discrepancy (MMD)
* Context-FID Score
* Discriminative Score
* Downstream forecasting performance (MSE, MAE, R²)

Pre-trained models and evaluation scripts will be released upon acceptance.

---

## 🔓 Release Policy

This repository is currently private. We will release the full codebase publicly **upon acceptance of the paper**. If you are a reviewer and need access, please contact us directly.

---

## 📜 Citation

If you use this framework or dataset, please cite:

```bibtex
@article{SocioDiff2025,
  title={SocioDiff: A Socio-aware Diffusion Model for Residential Load Data Generation},
  author={Chen, Weilong and others},
  journal={IEEE Transactions on Smart Grid},
  year={2025},
  note={Under review}
}
```

---

## 📬 Contact

For questions or collaborations, feel free to contact:
**Weilong Chen**
Email: [chenweilong921@gmail.com](mailto:chenweilong921@gmail.com)
