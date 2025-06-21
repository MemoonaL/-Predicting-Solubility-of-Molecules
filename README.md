# Predicting Solubility of Molecules
This project applies cheminformatics and linear regression to predict the aqueous solubility of molecules based on their SMILES representation — a practical reimplementation of John S. Delaney's paper
> This is an end-to-end **data science + chemistry** project that bridges machine learning and molecular property prediction.

---

## 🌐 Project Origin

📘 Based on a tutorial by [Chanin Nantasenamat – Data Professor](https://youtube.com/dataprofessor)  
📚 Reproduces the modeling approach from: [Delaney (2004), J. Chem. Inf. Comput. Sci.](https://pubs.acs.org/doi/10.1021/ci034243x)

---

## 🔬 Objective

The goal is to predict the **log solubility (logS)** of organic compounds using features derived from molecular structure.

---

## 📚 Dataset: ESOL (Delaney)

- 🧪 1128 molecules with experimentally measured solubility values (logS)
- 🔗 Downloaded directly from the Delaney paper
- Format includes:
  - `SMILES` (molecular string)
  - `logS` (experimental solubility)
  - Additional columns: ID, molecular weight, logP, etc.

---

## ⚙️ Tech Stack

| Tool | Use |
|------|-----|
| Python | Programming language |
| RDKit | Molecular parsing & descriptor calculation |
| Pandas | Data wrangling |
| scikit-learn | Linear regression model |
| Matplotlib / Seaborn | Visualization |

---

## 📈 Key Steps

### 1. **RDKit Featurization**
Used RDKit to extract molecular descriptors from SMILES:
- Molecular weight
- LogP (lipophilicity)
- Number of rotatable bonds
- Aromatic proportion
- H-bond donors/acceptors
- TPSA

### 2. **Modeling**
- Model: **Linear Regression**
- Target: `logS` (aqueous solubility)
- Features: Selected molecular descriptors

### 3. **Evaluation**
- RMSE and R² score
- Visualized predicted vs. actual solubility

---

