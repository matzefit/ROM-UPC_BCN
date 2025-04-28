# Reduced Order Model for Urban Climate Simulation

This project focuses on developing a Reduced Order Model (ROM) for predicting high-resolution urban climate variables using weather station data. The goal is to replace computationally expensive CFD-based multiphysics simulations with a faster, data-driven approach for estimating urban microclimate variables such as:
- Mean Radiant Temperature (MRT)
- Air Temperature (AT)
- Wind Speed Magnitude (MagVel)

The ROM leverages a combination of clustering techniques to select representative weather scenarios, and machine learning models trained on simulation data to approximate hourly climate conditions across an urban domain.

Link to Report: PENDING


Folder Structure: 
### Folder Structure:

```text
ROM_UPC/
│
├── data/
│   ├── X/                            # CSV files of 5 weather inputs per hour
│   ├── Y/                            # Corresponding 3 climate output images (MRT, AT, MagVel)
│   └── RawMeasurementData/           # Original weather station datasets
│
├── RawSimOutputData/                 # Raw simulation results (Animations, images, etc)
│
├── SimulationInputs/
│   ├── FinalSimulationInputs/        # Final weather input files for CFD simulations (with final modifications)
│   ├── PreprocessedSimulationInputs/ # Processed weather inputs for CFD simulation
│   └── SolarIrradCommands/           # Solar load command files for Fluent
│
├── src/
│   ├── BaselineModel.ipynb           # Training and evaluation of the ROM models
│   ├── ClusterRefStation.ipynb       # Clustering of weather station data to select representative days for CFD Simulation
│   ├── PrepRefStationData.ipynb      # Preprocessing of weather station data
│   ├── TrainingDataPrep.ipynb        # Preparation of training datasets from CFD simulation outputs
│
├── .gitignore                        # Git ignore files
└── Readme.md                         # This file
