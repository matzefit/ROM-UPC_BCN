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
```

Model Performance: 
![image](https://github.com/user-attachments/assets/38194ebf-2a48-4382-a395-bfa5dc33e5c0)

Example Prediction:

Given 5 Values: 

- Hour:               14
- Windspeed [m/s]:    5.69
- Wind Dir [deg]:     83
- Solar Irrad [W/m²]: 841
- Air Temp [K]:       298.65

![image](https://github.com/user-attachments/assets/8bc1d8d1-50f0-439a-a5fa-63640e07abe7)
