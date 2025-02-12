# Electrolytomics

This repository contains codes, datasets, and model checkpoints for the article "Electrolytomics: A unified big data approach for rational design and discovery of liquid electrolytes". The main objective of this work is to utilize machine learning models to screen efficient electrolytes for next-generation batteries, e.g., lithium metal batteries (LMBs) from a large virtual search space.

## Project Overview
The repository includes:
1. All labeled and unlabeled datasets used in the study.
2. All codes and notebooks to replicate main findings and figures in the main text of this study.
3. Trained model checkpoints used in the study to screen electrolytes.

## Directory Structure
```plaintext
.
├── README.md
├── datasets
│   ├── labeled_data.csv
│   ├── unlabeled_data.csv
│   └── virtual_search_space.csv
├── models
|   ├── Chemprop
│   |   ├── model_1.pkl
│   ├── SL
│   |   ├── model_3.pkl
│   └── model_4.pkl
└── notebooks
    ├── data_preprocessing.ipynb
    ├── model_training.ipynb
    └── model_evaluation.ipynb
```

## Datasets
The following datasets are used in this project:

1. **Labeled dataset**
   - File `labeled_data.csv` inside the directory `datasets`: this is the labeled dataset used for training machine learning models. The Jupyter notebook contains description for columns of features and target variable.

2. **Unlabeled dataset**
   - File `unlabeled_data.csv` inside the directory `datasets`: this is the unlabeled dataset used for predictions by the trained models.

3. **Virtual chemical search space**
   - File `virtual_search_space.csv` inside the directory `datasets`: this is the virtual search space containing potential electrolyte candidates.

## Notebooks
The repository includes the Jupyter notebooks with file names `data_preprocessing.ipynb`, `model_training.ipynb`, and `model_evaluation.ipynb`. Run the notebooks to reproduce the results of the study.

## Model checkpoints
All trained model checkpoints are stored inside the directory `models` containing files named `model_1.pkl`, `model_2.pkl`, `model_3.pkl`, and `model_4.pkl` for each of the models used in this study.

## How to Run
Follow these steps to run the notebooks:

1. Clone the repository:
   ```bash
   git clone https://github.com/AmanchukwuLab/electrolytomics
   cd electrolytomics
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

4. Open the notebooks from the `notebooks` directory and run them cell-by-cell.

## Dependencies
The following libraries are required:
- Python 3.8+
- Jupyter Notebook
- Pandas
- NumPy
- Scipy
- Scikit Learn
- Pickle
- Matplotlib

Install the required libraries using the provided `requirements.txt` file.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.
