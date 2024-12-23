# Molecular Solubility Prediction Web App

This web application predicts the **Solubility (LogS)** values of molecules based on their molecular structure. The app uses molecular descriptors to estimate the aqueous solubility of compounds, utilizing a trained machine learning model for prediction.

## Data Source
The model is based on data from the John S. Delaney paper:  
**"ESOL:  Estimating Aqueous Solubility Directly from Molecular Structure"**  
Published in *J. Chem. Inf. Comput. Sci.*, 2004, 44, 3, 1000-1005.  
Link: [ESOL Paper](https://pubs.acs.org/doi/10.1021/ci034243x)

## Features
- **SMILES Input**: Enter the SMILES notation of a molecule, and the app will compute molecular descriptors such as LogP, Molecular Weight, Rotatable Bonds, and Aromatic Proportion.
- **Prediction**: Using these descriptors, the app predicts the solubility value (LogS) for the molecule.
- **Molecular Descriptors**: The app calculates descriptors including:
  - **MolLogP**: The logarithm of the partition coefficient.
  - **MolWt**: Molecular weight.
  - **NumRotatableBonds**: Number of rotatable bonds in the molecule.
  - **AromaticProportion**: The proportion of aromatic atoms in the molecule.

## How to Use
1. **Enter SMILES Notation**: In the left sidebar, enter the SMILES string of your molecule.
2. **View Computed Descriptors**: The app automatically computes and displays the molecular descriptors for the entered molecule.
3. **Predict Solubility (LogS)**: After computing the descriptors, the app will use a pre-trained machine learning model to predict the molecule's solubility in water (LogS).
4. **See Results**: The predicted LogS value will be displayed on the app.

## Requirements
To run this app locally, you will need the following Python packages:
- **streamlit**: For building the web app.
- **numpy**: For numerical computations.
- **pandas**: For data manipulation.
- **rdkit**: For calculating molecular descriptors.
- **pickle**: For loading the pre-trained model.
- **Pillow**: For displaying images.

You can install the necessary libraries by running the following command:
```bash
   pip install -r requirements.text
```
## Running the App Locally

1. Clone this repository to your local machine.
2. Ensure that you have the required dependencies installed.
3. Run the following command to start the app:

    ```bash
    streamlit run app.py
    ```

## Live Version
The live version of the app can be accessed here:  
**[Molecular Solubility Prediction Web App](https://abdouyami-molecular-solubility-prediction-solubility-app-fm8idf.streamlit.app/)**

## Model Details
The machine learning model used for prediction is based on molecular descriptors and was trained using the ESOL dataset. The model is saved using pickle and is loaded within the app to make predictions.

## 📄 License
This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
