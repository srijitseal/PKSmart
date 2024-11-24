PKSmart: Predicting Pharmacokinetic (PK) Properties from Chemical Structures
Overview
PKSmart is an open-source tool developed to predict human pharmacokinetic (PK) parameters, including steady-state volume of distribution (VDss), clearance (CL), half-life (t½), fraction unbound in plasma (fu), and mean residence time (MRT). By integrating structural fingerprints, physicochemical properties, and predicted animal PK data, PKSmart offers predictions with performance on par with industry-standard models. This tool is designed to streamline the early stages of drug development and is available for both web and local use.

Features
Predictive Models for Human PK Parameters: Models for VDss, CL, t½, fu, and MRT based on chemical structure and predicted animal PK data.
Integration of Animal PK Data: Predicts animal PK parameters (VDss, CL, fu) for rats, dogs, and monkeys, which are used to improve human PK predictions.
Accessible Web Application and Local Implementation: Available for use via a browser or can be run locally using the provided code.
Installation
Using PyPI
You can install PKSmart using pip:

bash
Copy code
pip install pksmart
Note: Please use Python <3.12, >=3.9.

Building from Source
Alternatively, build PKSmart from source using Python Poetry:

Clone the repository:
git clone https://github.com/srijitseal/PKSmart.git
Navigate to the project directory:
cd PKSmart/
Install dependencies:
poetry install
Activate the virtual environment:
poetry shell
Build the project:
poetry build
Usage
Running PKSmart as CLI
To get started with the command-line interface, use:

bash
Copy code
pksmart -h
Predicting PK Parameters for a Single Compound
Select from the sidebar to predict PK parameters for a single compound.

Running PKSmart as a Python Library
Here's an example of how to use PKSmart as a Python library:

python
Copy code
from pksmart import PKSmart

if __name__ == '__main__':
    pksmart = PKSmart()
    smiles = "CCCCCCCO"
    result = pksmart.predict(smiles)
    print(result)
Web Access
PKSmart Web Application (Recommended):
You can access PKSmart through the following link:
PKSmart Web Application

Alternative Web Access:
PKSmart Streamlit App

Repository Structure
data/: Contains datasets used in the project.
01_Predict_human_data_Mordred.ipynb: Notebook to predict human PK data using Mordred descriptors.
02_Predict_animal_data.ipynb: Notebook for animal PK predictions.
03_Analyse_Predictive_Performance.ipynb: Notebook to evaluate model performance.
PKSmart/: Contains the core Python code and models.
test_data.csv: Sample data used for testing predictions.
Citation
If you use PKSmart in your work, please cite the following paper:
Srijit Seal, Maria-Anna Trapotsi, Manas Mahale, Vigneshwari Subramanian, Nigel Greene, Ola Spjuth, Andreas Bender. "PKSmart: An Open-Source Computational Model to Predict in vivo Pharmacokinetics of Small Molecules," bioRxiv, 2024.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Acknowledgements
PKSmart is developed and maintained by Srijit Seal and contributors, with support from various research institutes and organizations.

Contact
For questions or issues, please open an issue on the GitHub repository:
PKSmart GitHub Repository

