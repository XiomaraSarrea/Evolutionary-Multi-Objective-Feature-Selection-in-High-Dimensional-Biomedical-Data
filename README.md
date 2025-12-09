# Evolutionary Multi-Objective Feature Selection in High-Dimensional Biomedical Data

## Project Overview
This repository contains the implementation and results of a Master's project focused on feature selection in High-Dimension, Small-Sample (HDLSS) biomedical regimes. The study approaches biomarker discovery as a Multi-Objective Optimization Problem (MOOP), simultaneously minimizing prediction error and model complexity.

Non-dominated Sorting Genetic Algorithm II (NSGA-II) was implemented to navigate the intractable search space of a high-dimensional EEG dataset ($D=642$). The approach successfully identified a robust Pareto Front, achieving a feature reduction of 99.4% while maintaining high generalization performance on external validation sets.

## Repository Structure

- **code/**: Contains the Python implementation of the optimization framework.
    - `main_optimization.ipynb`: Jupyter notebook with the NSGA-II algorithm, custom operators, and validation loops.
- **report/**: Contains the final scientific report.
    - `PROJ_OPT.pdf`: Full text describing methodology, mathematical formulation, and biological interpretation of results.
- **requirements.txt**: List of Python dependencies required to run the code.

## Key Results

The optimization identified a stable feature subset (Knee Point) that outperforms traditional univariate filter methods:

| Metric | Value |
| :--- | :--- |
| **Original Feature Dimension** | 642 |
| **Selected Feature Dimension** | 4 |
| **Dimensionality Reduction** | 99.4% |
| **External Validation (XGBoost AUC)** | 0.97 |

## Dependencies

To run the provided code, the following Python libraries are required:
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- pymoo
- xgboost
- shap

## Usage

1. Clone the repository.
2. Install the requirements: `pip install -r requirements.txt`
3. Open `code/main_optimization.ipynb` in Jupyter Notebook or JupyterLab to view the implementation and reproduce the analysis.

*Note: The raw EEG dataset is not included due to data privacy restrictions. The code assumes input data follows standard tabular formats.*
