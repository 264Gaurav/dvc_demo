# dvc tool - data versioning and data pipeline

Data Versioning Control - Demonstrating the use of DVC tool with Git for efficient data and model management.

### Prerequisites

Python,
Git installed,
DVC installed (pip install dvc)

## Overview

This project showcases how DVC integrates with Git to manage datasets, machine learning models, and pipelines. It follows the principles of the ML lifecycle, including data preparation, featurization, model training and evaluation.

## ML Lifecycle and Data Pipeline

### ML Lifecycle

1. **Data Preparation**: Version control for raw and processed datasets.
2. **Feature Engineering**: Extract meaningful features from data.
3. **Model Training**: Track experiments and model versions.
4. **Evaluation**: Compare metrics across different model iterations.
5. **Deployment**: Ensure reproducibility of models and pipelines.

### Data Pipeline / Pipeline Workflow

1. **Prepare Stage**: Prepares the raw data (data/data.xml) into a processed format (data/prepared).
2. **Featurize Stage**: Extracts features from the prepared data (data/prepared) and outputs feature data (data/features).
3. **Train Stage**: Trains a machine learning model using the features (data/features) and outputs the model file (model.pkl).

The data pipeline is defined in the `dvc.yaml` file, which specifies the stages of the pipeline, their dependencies, outputs, and parameters.

### Installation / Project setup

1- Clone the repository:
git clone repo-url ,
cd dvc_demo

2- Install dependencies:
pip install -r src/requirements.txt

## Usage

1- Intiatlize DVC:
dvc init

2- Add data files for versioning:
dvc add <data-file>

3- Commit changes to Git:
git add data-file .dvc .gitignore ,
git commit -m "Track data file with DVC"

4- Push data to remote storage:
dvc remote add -d remote-name remote-url ,
dvc push

## Commands to Work with the Pipeline

1. Visualize the pipeline:
   dvc dag

2. Reproduce the pipeline:
   dvc repro

3. Push pipeline outputs to remote storage:
   dvc push

## Resources

- [DVC Documentation](https://dvc.org/doc)
- [Data Pipelines Guide](https://dvc.org/doc/start/data-pipelines/data-pipelines)
- [Git Documentation](https://git-scm.com/doc)
