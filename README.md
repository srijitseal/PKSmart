# PKSmart Repository Structure

## Overview
PKSmart is a repository dedicated to predicting pharmacokinetic (PK) properties, including parameters like clearance (CL), volume of distribution (VdSS), and the fraction unbound (fup), based on chemical structures. The project integrates machine learning and chemical informatics to model PK properties for various compounds, including human, dog, rat, and monkey data.

## Using local implementation
Download essential files from https://doi.org/10.5281/zenodo.10611606 and run locally!

## Run Online on Server v3.0.0 
If you prefer to use the predictor online via Uppsala University SciLifeLab Serve:[https://pk-predictor.serve.scilifelab.se/](https://pk-predictor.serve.scilifelab.se/)

## Data Files
- **`data/`**: Contains datasets used in training and testing PKSmart models. Includes curated datasets for human and animal pharmacokinetic (PK) parameters.

## Jupyter Notebooks
These notebooks provide data processing, model training, evaluation, and analysis workflows.

### Data Exploration and Preprocessing
1. **`00_check_data_pka.ipynb`**: Examines and preprocesses PK data, ensuring data quality and consistency.
2. **`00b_animal_human_lmplot_CL.ipynb`**: Creates linear regression plots comparing clearance (CL) between human and animal datasets.
3. **`00c_animal_human_lmplot_VdSS.ipynb`**: Generates regression plots comparing volume of distribution (VDss) between humans and animals.
4. **`00d_animal_human_lmplot_fup.ipynb`**: Visualizes relationships for fraction unbound in plasma (fu) between human and animal datasets.

### Human PK Prediction
5. **`01_Predict_human_data_Mordred.ipynb`**: Predicts human PK parameters using Mordred descriptors.
6. **`01_Predict_human_data_Morgan.ipynb`**: Predicts human PK parameters using Morgan fingerprints.
7. **`01_Predict_human_data_Morgan_Mordred.ipynb`**: Combines Morgan fingerprints and Mordred descriptors for human PK predictions.

### Animal PK Prediction
8. **`02_Predict_rat_data.ipynb`**: Predicts PK parameters for rats.
9. **`02_Predict_dog_data.ipynb`**: Predicts PK parameters for dogs.
10. **`02_Predict_monkey_data.ipynb`**: Predicts PK parameters for monkeys.
11. **`02b_Analyse_animal_models.ipynb`**: Analyzes and compares the performance of animal PK models.

### Advanced Model Training
12. **`03_Predict_human_data_with_artificial_real_animal_data_only.ipynb`**: Uses real animal data where available and artificial animal data for human PK predictions.
13.**`03_MedianMordredCalculator_artificial_animal_data_mfp_mrd.ipynb`**: Calculates median Mordred descriptors and integrates animal data for enhanced PK predictions.
14.**`03_Predict_human_data_mean_predictor.ipynb`**: Implements a mean predictor model as a baseline for comparisons.
15.**`03_Predict_human_data_with_artificial_animal_data_mfp.ipynb`**: Uses artificial animal data and Morgan fingerprints
16.**`03_Predict_human_data_with_artificial_animal_data_mrd.ipynb`**: Uses artificial animal data and Mordred descriptors
17.**`03_Predict_human_data_with_artificial_animal_data_mfp_mrd.ipynb`**: Uses artificial animal data with Morgan fingerprints and Mordred descriptors.
18.**`03_Predict_human_data_artificial_real_animal_data_mfp_mrd.ipynb`**: Uses artificial and real animal data with Morgan fingerprints and Mordred descriptors



### Chemical Space and Model Analysis
19. **`07_Analyse-Chemical_space_human_dataset_animal_dataset.ipynb`**: Explores and visualizes chemical space for human and animal datasets.
20. **`07_Analyse-Chemical_space_nested_cross_val.ipynb`**: Evaluates chemical space coverage across nested cross-validation splits.
21. **`08_Analyse_Performance_NCV_Wo_Outputs.ipynb`**: Assesses model performance in nested cross-validation (NCV)
22. **`09_Distribution and Drug Space.ipynb`**: Analyzes the distribution of PK parameters and drug chemical space.
23. **`09b_Figures_Cross_Val_Fold_errors.ipynb`**: Generates figures to evaluate cross-validation fold errors.
24. **`10_Evaluate_with_fold_errors.ipynb`**: Final evaluation of model predictions with calculated fold errors.

## Additional Files
- **`External_Test_ALL_Lombardo_FDA_CL_fu_V2`**: External test dataset for evaluating model performance against independent data sources.

## Installation

### Using PyPI 
You can install the DILI Predictor using pip: `pip install pksmart`. ***Please use Python <3.12, >=3.9*** 
For details see https://pypi.org/project/pksmart/

## Cite

If you use PKSmart in your work, please cite:

> PKSmart: An Open-Source Computational Model to Predict in vivo Pharmacokinetics of Small Molecules
> Srijit Seal, Maria-Anna Trapotsi, Manas Mahale, Vigneshwari Subramanian, Ola Spjuth, Nigel Greene, Andreas Bender
> bioRxiv 2024.02.02.578658; doi: https://doi.org/10.1101/2024.02.02.578658


## Acknowledgements
Developed and maintained by Srijit Seal and contributors.

## Contact
For any questions or issues, please open an issue on the GitHub repository.
