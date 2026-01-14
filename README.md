# carbon-aware-parameter-reusing-architecture-search-for-GNN
Neural Architecture Search Implementation
This repository contains an implementation of neural architecture search (NAS) for automating the design of deep neural network architectures. The project defines a configurable search space, a pluggable search strategy, and an evaluation pipeline to explore candidate models efficiently under compute and accuracy constraints.
​

Features
Modular search space definition (operations, connectivity, and hyperparameters) so you can quickly adapt NAS to new datasets or tasks like classification or detection.
​

Pluggable search strategies (e.g., random search, reinforcement learning, or evolutionary search) for exploring architectures.
​

Re-usable training and evaluation loop with support for early stopping or low-fidelity training to speed up the search process.
​

Simple configuration-driven experiments via YAML/JSON configs for search, training, and evaluation settings.
​

Project Structure
search/: Search algorithms (controller, evolutionary loop, or other searchers).
​

models/: Search space definition and model-building utilities for candidate architectures.
​

trainer/ or train.py: Scripts for training and validating sampled architectures.
​

configs/: Example configuration files for different datasets and search settings.
​

scripts/: Helper scripts for running experiments and reproducing results.
​

Installation
Clone this repository and install the Python dependencies listed in requirements.txt using your preferred environment manager.
​

Ensure compatible versions of the deep learning framework (e.g., PyTorch) and CUDA are installed if using GPU acceleration.
​

Usage
Define or edit a configuration file in configs/ to set dataset paths, search space, and search strategy parameters.
​

Run the search script, e.g. python search.py --config configs/experiment.yaml, to start NAS and log candidate architectures and metrics.
​

Use the best discovered architecture ID or config to fully train the final model with train.py.
​

Reproducibility
All main experiments can be reproduced by running the provided configuration files and scripts in the order documented under the Usage section.
​

Random seeds and key hyperparameters are stored in configs and logged alongside results for easier replication and ablation studies.
