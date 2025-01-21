Context: This project classifies DNA regions into “accessible” (1) and “inaccessible” (0) using 1D Convolutional Neural Network models (AlexNet and NiN).
Goals:
Generate labeled datasets from the outputs of Project-1 (positive/negative files).
Convert DNA sequences to one-hot encodings.
Implement custom PyTorch DataLoader classes.
Train and evaluate two CNN architectures (AlexNet & NiN) on genomic data.
Compare different hyperparameters and visualize the performance (accuracy plots, confusion matrices).

Data Preparation
Input Files

Project-1 Output: At least 10 positive (accessible) and 10 negative (inaccessible) DNA sequence files, OR two large files labeled accordingly.
Labels: 1 for accessible, 0 for inaccessible.
Steps

Combine & Label: Merge your positive/negative files into a single CSV or two separate files. Ensure each sequence has a label column (e.g., 1 or 0).
One-Hot Encoding: Convert the nucleotide sequences (A, T, G, C) into numeric arrays.
Train/Test Split: Randomly shuffle and split the dataset into 80% for training and 20% for testing, ensuring shuffle=True.

Usage
Preprocessing: This script handles labeling, one-hot encoding, and generating final .npy or .pt files.

Create DataLoader
This script (or module) defines a PyTorch Dataset and DataLoader for the prepared data.

Train & Evaluate
Model can be alexnet or nin.

Hyperparameters loaded from JSON/YAML to easily switch between configurations (e.g., hidden layers = 256, learning rates, batch size, etc.).
Repeat the training with different hyperparameters for each model, for a total of four runs:

AlexNet + Hyperparameter Set 1
AlexNet + Hyperparameter Set 2
NiN + Hyperparameter Set 1
NiN + Hyperparameter Set 2

Results
Accuracy vs. Epoch
Plots stored in results/accuracy_plots/.
Compare the four experiments in one graph.
Confusion Matrix
Stored in results/confusion_matrices/.
Display for each experiment (e.g., AlexNet #1, AlexNet #2, NiN #1, NiN #2).

Further Development
Extended Models: Experiment with deeper architectures or LSTM/Transformer-based approaches for sequence data.
Hyperparameter Tuning: Automate the search for optimal learning rates, batch sizes, or dropout.
Interpretability: Explore feature importance or saliency maps to understand model decisions.
