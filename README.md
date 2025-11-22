# CADD-COVID19
# 💻 CADD @ COVID-19: Biopython & RDKit for Bioinformatics Analysis

## 📝 Overview

This Jupyter Notebook serves as an introduction to **Computational-Aided Drug Discovery (CADD)** techniques using fundamental bioinformatics libraries, specifically **BioPython** and **RDKit**. The examples focus on handling common data types encountered in drug discovery related to targets like the SARS-CoV-2 protein (`7LC8`).

The notebook demonstrates essential tasks, including retrieving and inspecting protein structures and analyzing nucleic acid/protein sequences.

## 🚀 Analysis Demonstrations

The notebook contains two main examples showcasing basic bioinformatics and cheminformatics tasks:

### Example 1: Protein Structure Analysis (PDB)

* **Objective**: To fetch a protein structure from the Protein Data Bank (PDB) and inspect its composition.
* **PDB ID**: **7LC8** (Structure of SARS-CoV-2 main protease $\text{M}^{\text{pro}}$ with an inhibitor).
* **Steps**:
    1.  Uses `Bio.PDB.PDBList` to **download the structure** in `mmCIF` format (`7lc8.cif`).
    2.  Uses `Bio.PDB.MMCIFParser` to **parse the structure file**.
    3.  Prints the number of **Models** (14) and **Chains** (3) found in the structure.

### Example 2: Sequence Analysis (FASTA)

* **Objective**: To read a FASTA file containing genetic/protein sequences and compute the GC content.
* **Input File**: Assumes a FASTA file named **`rcsb_pdb_7LC8.fasta`** is available.
* **Steps**:
    1.  Uses `Bio.SeqIO.parse()` to read the sequence data.
    2.  Uses `Bio.SeqUtils.gc_fraction()` to calculate the **GC content** (Guanine-Cytosine ratio) of the sequence.
    3.  The calculated GC content (44.44% in the example output) is printed.

## 🛠️ Requirements and Setup

This notebook relies on several widely used Python libraries for bioinformatics and cheminformatics.

### Libraries

The following dependencies are installed within the notebook:

```bash
# Core bioinformatics library
!pip install biopython

# Cheminformatics library (used for CADD tasks)
!pip install rdkit
