# Molecular Property Analyzer
*A simple Python tool for calculating basic molecular descriptors from SMILES strings.*

---

## 🔬 Overview
This project is a small cheminformatics tool I built independently as part of my early exploration into computational drug-design concepts. The program takes a list of SMILES strings and computes fundamental molecular descriptors such as:

- Molecular Weight  
- LogP  
- Number of Hydrogen Bond Acceptors (HBA)  
- Number of Hydrogen Bond Donors (HBD)

The tool is intended for educational purposes and demonstrates how computer science can be applied to early-stage molecular analysis.

---

## 🧪 Features
- Accepts any list of SMILES strings  
- Calculates commonly used descriptors  
- Prints results in a clean, readable format  
- Uses RDKit (open-source cheminformatics library)  

This program is not meant for real-world drug development or experimentation — it is purely computational and conceptual.

---

## 🧠 Why I Built This
I am a high school student interested in biology, computational chemistry, and AI-based molecular design. I wanted to understand how molecules can be analyzed using code, and how computational tools support scientific thinking.

This project helped me:
- Learn how cheminformatics software works  
- Practice Python for scientific computing  
- Explore the connection between CS and biomedical innovation  

---

## 📁 Example Code

```python
from rdkit import Chem
from rdkit.Chem import Descriptors

smiles = ["CCO", "c1ccccc1O", "CCN(CC)CC"]

for s in smiles:
    mol = Chem.MolFromSmiles(s)
    print("SMILES:", s)
    print("Molecular Weight:", Descriptors.MolWt(mol))
    print("LogP:", Descriptors.MolLogP(mol))
    print("HBA:", Descriptors.NumHAcceptors(mol))
    print("HBD:", Descriptors.NumHDonors(mol))
    print()
