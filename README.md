# *Electrolytomics*

This repository contains codes, datasets, model checkpoints and hyperparameters for the article "Electrolytomics: A unified big data approach for rational design and discovery of liquid electrolytes". The main objective of this work is to utilize machine learning models to screen efficient electrolytes for next-generation batteries, e.g., lithium metal batteries (LMBs) from a large virtual search space.

## Project Overview
The repository includes:
1. Labeled and unlabeled datasets used in the study.
2. Codes and notebooks to replicate main findings and figures in the main text of this study.
3. Trained model checkpoints used in the study to screen electrolytes.

## Directory Structure
```plaintext
.
├── README.md
├── environment.yml
├── datasets
│   ├── featurized
│   │   ├── CE
│   │   ├── conductivity
│   │   └── oxstab
│   ├── other
│   ├── predicted
│   │   ├── CE
│   │   ├── conductivity
│   │   └── oxstab
│   └── raw
│       ├── CE
│       ├── conductivity
│       └── oxstab
├── hyperparameters
│       ├── CE
│       ├── conductivity
│       └── oxstab
├── models
│   ├── Chemprop
│   └──SL
└── notebooks
    ├── Chemprop_BHO_training_prediction
    ├── SHAP_sensitivity_analysis
    ├── SL_BHO_training_prediction
    ├── creating-data-splits
    ├── eScore_calculations
    ├── featurization
    ├── manuscript-plots
    └── reduced_embeddings
```

## Datasets
The datasets are arranged in the following directories:

1. `datasets/raw`: Contain raw datasets without any features for each of the three properties (inside `conductivity`, `oxstab`, and `CE`). 
2. `datasets/featurized`: Contain featurized datasets for both shallow learning and Chemprop models for each of the three properties (inside `conductivity`, `oxstab`, and `CE`). 
3. `datasets/predicted`: Contain files with ML predictions for each of the three properties (inside `conductivity`, `oxstab`, and `CE`)
4. `datasets/other`: Other relevant files, e.g., t-SNE embeddings used in the present study.

## Notebooks
The repository includes the Jupyter notebooks for different purposes inside:
1. `notebooks/creating-data-splits`: For generating all data splits used in the present study.
2. `notebooks/featurization`: For generating all types of features used in the present study.
3. `notebooks/Chemprop_BHO_training_prediction`: For performing Bayesian hyerparameter optimization (BHO), training, and predicting Chemprop models
4. `notebooks/SL_BHO_training_prediction`: For performing Bayesian hyerparameter optimization (BHO), training, and predicting shallow learning models (LightGBM and PLSR).
5. `notebooks/SHAP_sensitivity_analysis`: For performing SHAP and sensitivity analyses on shallow learning models (LightGBM and PLSR).
6. `notebooks/eScore_calculations`: For calculating eScores.
7. `notebooks/reduced_embeddings`: For obtaining and plotting t-SNE reduced embeddings.
8. `notebooks/manuscript-plots`: For reproduing figures in the main text of this study.

## Model checkpoints
The trained model checkpoints for shallow learning (in `.sav` format) and Chemprop models are stored inside the directory `models` for each of the three properties (inside `conductivity`, `oxstab`, and `CE`).

## Hyperparameters
The exact hyperparameters obtained after BHO for for shallow learning and Chemprop models are also provided inside the directory `hyperparameters` for each of the three properties (inside `conductivity`, `oxstab`, and `CE`).

## How to Run
Follow these steps to run the notebooks:

1. Clone the repository:
   ```bash
   git clone https://github.com/AmanchukwuLab/electrolytomics
   cd electrolytomics
   ```

2. Create virutal environment, install the required dependencies, and activate the virtual environment:
   ```bash
   conda env create -f environment.yml
   conda activate electrolytomics
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

4. Open the notebooks from the `notebooks` directory and run them cell-by-cell.

## Dependencies
The following libraries are required (refer `environment.yml` file):
- Python 3.8+
- Jupyter Notebook
- Pandas
- NumPy
- Scipy
- Scikit Learn
- Pickle
- Matplotlib
- Seaborn
- Shap
- SALib
- LightGBM
- Chemprop
- RDKit
- Optuna
- OpenTSNE

## Citation
Please consider citing this work if you use our datasets or work:
```plaintext
@article{kumar2024electrolytomics,
  title={Electrolytomics: A unified big data approach for electrolyte design and discovery},
  author={Kumar, Ritesh and Vu, Minh Canh and Ma, Peiyuan and Amanchukwu, Chibueze},
  journal={ChemRxiv},
  year={2024},
  doi={10.26434/chemrxiv-2024-vqtc}
}
```
