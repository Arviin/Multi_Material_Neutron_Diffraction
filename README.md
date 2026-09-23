# Multi_Material_Neutron_Diffraction
# Multi-Material Neutron Diffraction Classification

Synthetic neutron powder diffraction dataset generation and material
classification using McStas, NCrystal, and PyTorch.

## Project overview

The workflow consists of three main stages:

1. **Synthetic diffraction data generation**
   - McStas neutron transport simulations
   - NCrystal material definitions
   - Multiple crystalline materials
   - Wavelength (`lambda`) sweep
   - Wavelength bandwidth (`dlambda`) sweep
   - Direct-beam suppression using a beamstop
   - 2D diffraction patterns
   - Azimuthally integrated 1D diffraction profiles

2. **Material classification**
   - PyTorch 1D convolutional neural network
   - Train / validation / test splitting
   - Data augmentation
   - Dropout
   - AdamW optimization
   - Learning-rate scheduling
   - Early stopping
   - Confusion-matrix and classification-metric evaluation

3. **Evaluation on unseen diffraction conditions**
   - Generation of new McStas simulations
   - Previously unseen wavelength and bandwidth combinations
   - Material prediction using the trained classifier
   - External generalization assessment

## Repository structure

```text
Multi_Material_Neutron_Diffraction/
│
├── notebooks/
│   ├── 01_generate_diffraction_dataset.ipynb
│   ├── 02_DL_material_classifier.ipynb
│   └── 03_test_unseen_diffraction_data.ipynb
│
├── mcstas/
├── data/
├── figures/
├── README.md
└── .gitignore