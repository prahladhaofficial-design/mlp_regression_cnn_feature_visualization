# MLP Regression and CNN Feature Visualization

A visual neural-network project combining noisy sinc regression, MLP training behavior, convolution kernels, stride/padding effects, pooling, and PyTorch CNN curves.

## Overview

Neural networks become easier to understand when their intermediate behavior is visible. This project focuses on visual outputs: regression surfaces, training curves, convolution feature maps, and pooling effects.
The repository connects function approximation with image feature extraction.

## Project Design

- Generate noisy nonlinear regression data.
- Train an MLP and visualize prediction behavior.
- Apply handcrafted convolution kernels to image data.
- Vary stride, padding, and pooling to inspect spatial effects.
- Track PyTorch CNN train-test loss and accuracy.

## Key Capabilities

- Noisy sinc-function dataset generation.
- MLP regression and loss visualization.
- Prediction-grid visualization.
- Edge, blur, and sharpen convolution feature maps.
- Stride, padding, and kernel-size comparisons.
- Max-pooling before/after comparison.
- Train-test loss and accuracy plots.

## Repository Structure

```text
notebooks/mlp_cnn_experiments.ipynb  Main notebook.
figures/                             Generated regression plots, feature maps, and training curves.
requirements.txt                     Python dependencies.
```

## Running Locally

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/mlp_cnn_experiments.ipynb
```

## Results and Artifacts

- Sinc function actual-vs-noisy visualization.
- MLP prediction-grid plot.
- Training and testing loss/accuracy curves.
- Feature maps for blur, edge detection, sharpen, stride, padding, and pooling settings.

## Reproducibility Notes

- Keep model hyperparameters and random seeds fixed when comparing regression surfaces.
- Regenerate feature-map plots after changing kernel size, stride, padding, or pooling settings.
- Run visualization cells after training cells so plots reflect the current model state.
- Use the saved figures as inspection artifacts, not as replacements for rerunning the notebook.

## Detailed Workflow

- Open the notebook and run the sinc regression section first.
- Inspect MLP prediction plots before moving into image feature maps.
- Run convolution-kernel sections to compare edge, blur, and sharpen filters.
- Run stride, padding, and pooling sections to inspect spatial transformation effects.
- Review PyTorch training curves to connect feature extraction with model training behavior.

## Implementation Details

- The regression section focuses on nonlinear function approximation.
- The convolution sections use visual kernels to make image transformations interpretable.
- Stride and padding experiments show how output dimensions and feature placement change.
- Pooling comparisons show how spatial information is compressed.
- Training curves provide a bridge between low-level feature operations and end-to-end learning.

## Data and Inputs

- The sinc task uses generated noisy data.
- Image experiments use local image data or notebook-prepared image tensors.
- Generated figures are stored under `figures/` for review outside the notebook.
- Changing kernel values or stride/padding settings will produce different feature maps.

## How To Interpret the Results

- The MLP prediction grid shows how the model approximates a nonlinear target function.
- Feature maps reveal the effect of individual convolution kernels.
- Pooling outputs should be read as compressed spatial summaries.
- Train-test curves help identify underfitting, overfitting, or unstable optimization.

## Limitations and Assumptions

- Handcrafted kernels are interpretability tools, not learned filters.
- Notebook execution order matters.
- The project mixes regression and CNN visualization, so sections should be reviewed independently.
- A script export pipeline would improve reproducibility for all figures.


## Review Guide

Use this checklist when reviewing the repository on GitHub:

- Start with the overview to understand the project objective before opening notebooks or source files.
- Read the repository structure section to identify the main entry point.
- Inspect generated outputs before rerunning experiments; they provide a quick view of the current project state.
- Review scripts and notebooks together when both are present, since notebooks often explain decisions while scripts preserve reusable execution paths.
- Check the limitations section before interpreting results too strongly.
- Use the possible extensions section to understand how the project can grow without changing its core purpose.

## Troubleshooting

Common issues and fixes:

- If imports fail, confirm that the virtual environment is activated and dependencies were installed from `requirements.txt`.
- If a notebook cell fails because a variable is missing, restart the kernel and run the notebook from the first cell.
- If a script cannot find a data file, run it from the repository root unless the README gives a different working directory.
- If plots are not regenerated, check that the output folder exists and that the script has write permission.
- If a package version causes errors, create a fresh environment and reinstall dependencies before debugging the source code.
- If GPU-related packages are unavailable, run CPU-compatible sections first and treat heavier deep-learning experiments separately.

## Development Notes

The repository is organized to be understandable before it is optimized. Most code favors clear structure, visible intermediate steps, and saved artifacts over highly compressed implementations. When extending the project, prefer small changes that keep the original experiment reproducible.

Recommended development practices:

- Keep new data files under `data/`, `datasets/`, or the existing local data folder for that project.
- Keep generated figures under `figures/`, `plots/`, `outputs/`, or `results/` depending on the existing convention.
- Add new experiments as separate scripts or clearly labeled notebook sections.
- Avoid overwriting existing outputs unless the experiment is intentionally being refreshed.
- Document any new dependency in `requirements.txt`.
- Prefer relative paths so the repository works after cloning on another machine.

## Project Status

This repository is prepared as a standalone GitHub project. The current version includes the core implementation, documentation, and available artifacts needed to understand the work. Future improvements can focus on stronger automation, more tests, richer visual summaries, and cleaner packaging where appropriate.

## Possible Extensions

- Add a script to export all notebook figures in one run.
- Compare multiple activation functions for the MLP regression task.
- Add learned CNN filters beside handcrafted kernels.
- Add a compact report summarizing visual observations.

## Tech Stack

Python, NumPy, Matplotlib, Pillow, PyTorch, torchvision, Jupyter Notebook.

## Author

Prahladha, IIT Hyderabad
