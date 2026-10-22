# Raha Reproduction

This repository contains a reproduction of experiments using **Raha**, a data error detection system.

The project uses **uv** for Python environment and dependency management to make the experimental setup easier to reproduce.

## 1. Requirements

Before running the experiments, make sure you have:

- Python (the version specified in `pyproject.toml`)
- [uv](https://docs.astral.sh/uv/getting-started/installation/)
- Sufficient memory and processing capacity for the selected datasets

## 2. Installation

Clone the repository and navigate to the project directory:

```bash
git clone <repository-url>
cd <repository-directory>
```

Install the project dependencies using uv:

```bash
uv sync
```

This creates a virtual environment (`.venv`) and installs the dependencies specified in the project configuration and lockfile.

To verify that the environment is working:

```bash
uv run python --version
```

**Note:** Use `uv run` when executing Python scripts or commands to ensure that the correct project environment is used. There is no need to activate the virtual environment manually.

## 3. Running the Experiments

Run the relevant Python script using:

```bash
uv run python <script-name>.py
```

For Jupyter notebooks, select the Python interpreter from the project's `.venv` environment.

## 4. Excluded Datasets

Some datasets from the original experimental setup have been excluded from the experiments due to their size and computational requirements.

These datasets are stored separately in the following directory:

```text
removed_datasets/
```

The excluded datasets were not included in the experimental runs because processing them would require more computing resources than were available.

Consequently, the experiments cover only a subset of the original datasets. This should be considered when comparing the results with those reported in the original research.

## 5. Reduced Number of Iterations

The number of experimental iterations has deliberately been kept low to reduce execution time and computational costs.

Running the experiments with more iterations would require substantially more processing time, particularly for larger datasets.

As a result:

- The reported results may show greater variability.
- The results may be less statistically reliable than those obtained with a larger number of iterations.
- The experiments should be interpreted as a limited reproduction rather than a complete replication of the original experimental evaluation.

## 6. Reproducibility and Limitations

The repository provides the project configuration and dependencies needed to reproduce the included experiments.

However, the reproduction has two main limitations:

1. **Dataset selection:** Some larger datasets have been excluded because of their computational requirements.
2. **Iteration count:** The number of iterations has been reduced to make the experiments feasible with the available hardware.

These limitations may affect the comparability and generalizability of the experimental results.

For a more complete reproduction, the excluded datasets can be reintroduced and the number of iterations increased, provided sufficient computational resources are available.
