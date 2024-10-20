# Automated-PDB-AlphaFold-Structure-Retriever
Automated Python script to retrieve protein structures from PDB and AlphaFold databases from UniProt IDs and gene names

# Protein Structure Retrieval

## Overview

The **Protein Structure Retrieval** script is a Python-based designed to automate the process of retrieving structural information for proteins from the Protein Data Bank (PDB) and AlphaFold databases. 

## Key Features

- **CSV Input**: 
  - The script reads a user-provided CSV file that contains gene names and corresponding UniProt IDs. 
  - It expects the CSV file to have specific column headers: **Gene** and **UniProt ID**.

- **PDB Structure Retrieval**: 
  - For each UniProt ID, the script queries the UniProt database to identify the best available PDB structure. 
  - The selection is based on the resolution of the structure and its length, ensuring that only high-quality structures are considered (specifically, those with a resolution better than 2.0 Å).
  - Successfully retrieved PDB files are saved in a dedicated directory.

- **AlphaFold Integration**: 
  - If no suitable PDB structure is found, the script attempts to download the corresponding AlphaFold structure from the European Bioinformatics Institute (EBI).

- **Logging**: 
  - The results of the retrieval process are logged into three separate CSV files for easy tracking and review:
    - **PDB-Structure-Results.csv**: Contains details about successfully retrieved PDB structures.
    - **Unavailable-Structures.csv**: Logs any structures that were not available for retrieval.
    - **Retrieved-Structure-Details.csv**: Contains the status of each structure retrieval attempt, including PDB and AlphaFold structures.

##   Prerequisites

To run this script, you will need:
- **Python**: Ensure that you have Python installed on your system. You can download it from [python.org](https://www.python.org/).
- **Requests library**: This script uses the `requests` library to make HTTP requests. You can install it using pip:
  pip install requests
- **csv file**: containing at least two columns "[Genes, UniProt ID]"

##  License
This project is licensed under the MIT License.

