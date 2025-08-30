# Multimodal Validity System (MVS)  
**SAS Hackathon 2025 Project**  

---

## Overview
This project is being developed for the **2025 SAS Hackathon**.  
We are building the first **Multimodal Validity System (MVS)** to generate a novel composite validity index score by fusing predictions across multiple modalities (truthfulness, effort, consistency).  

The goal is to help clinicians quickly and reliably evaluate the validity of cognitive and psychological assessments, reducing waste, fraud, and diagnostic uncertainty.

---

## Datasets
We are leveraging three research datasets:  

- MU3D: Y variable: TruthProp (truth vs deception).  
- MOCAS: Y variable: effort/validity classification from public_subject_results.csv.  
- DepreSym: Y variable: depression severity (union of .trec transcript files).  

Each dataset represents one slice of the validity construct:  
- Truthfulness (MU3D)  
- Effort (MOCAS)  
- Consistency (DepreSym)  

---

## Workflow (in progress)
1. Preprocessing  
   - Clean and standardize datasets.  
   - Handle missing values and normalize labels.  
   - Feature extraction: TF-IDF for text, statistical features for physiological data, etc.  

2. Modeling (per dataset) 
   - Train separate models (Logistic Regression, Random Forest, XGBoost, and/or Neural Nets).  
   - Save metrics (accuracy, F1, ROC).  

3. Ensemble / Fusion 
   - Combine model outputs into an ensemble.  
   - Generate the novel validity index score as a standardized, single metric.  

4. Evaluation 
   - Compare individual dataset models vs. ensemble performance.  
   - Report results with confusion matrices, ROC curves, and validation metrics.  

---

## Repository Structure (in progress)
- /data/ # raw datasets
- /models/ # trained models and checkpoints
- /results/ # metrics, plots, confusion matrices
- /docs/ # workflow diagrams, additional documentation
- README.md # project overview

The Standard Dadivation Team:
- Johnathan Burpo
- Noah Duncan
- James Faulk
- Josh Simpson
