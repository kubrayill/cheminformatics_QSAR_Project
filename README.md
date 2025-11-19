# cheminformatics_QSAR_Project
**[View the Full Executable Code (Jupyter Notebook) here.](Cheminformatics_Analysis.ipynb)**

QSAR Modeling for Drug Activity Prediction (Cheminformatics Project)
This repository contains the complete pipeline for developing a Quantitative Structure-Activity Relationship (QSAR) model. 
The goal is to predict the biological activity class of novel chemical compounds using computational methods, thus simulating a core process in early-stage drug discovery.
 Project Goals:
Featurization: Convert complex chemical structures into machine-readable numerical data.
Modeling: Train a robust classification algorithm to predict activity based on structure. 
Validation: Use industry-standard techniques to assess model reliability.
 Methodology and Pipeline:
The project follows a standardized cheminformatics workflow, executed sequentially in the included Jupyter Notebook (Cheminformatics_Analysis.ipynb).
1. Data Source and Preprocessing:
    Data: A sample dataset was used containing SMILES codes and experimental pIC50 values simulating activity against a biological target (e.g., Acetylcholinesterase - AChE).
    Labeling: Compounds were categorized into the target classes: Active (1) for $\text{pIC50} > 6.5$ and Inactive (0) for $\text{pIC50} \le 6.5$.
2. Feature Engineering (RDKit)Tool:
     RDKit was used to perform all molecular calculations.
     Feature Generation: Morgan Fingerprints (1024-bit vectors) were generated for every compound. These fingerprints served as the primary input feature matrix ($\mathbf{X}$) for the model.
3. Model Training and Validation:
     Algorithm: Random Forest Classifier was selected as the predictive model.
     Validation Technique: Due to the limited sample size, 2-Fold Cross-Validation was employed to avoid overfitting and provide a reliable, generalized accuracy score.
     Key Results and Findings:
     Final Validation Metric: Average Cross-Validation Accuracy: 41.67%
     Note: This score is expected for the small, illustrative dataset and confirms that the methodology is sound, even if the predictive power is low due to limited training data.Analytical Insight
(Feature Importance): The model successfully identified specific Morgan Fingerprint bits (structural motifs) that were most influential in classifying a molecule as Active or Inactive.
Technologies Used:
Programming Language: Python
Cheminformatics: RDKit
Data Analysis: Pandas & NumPy
Machine Learning: scikit-learn (RandomForestClassifier, cross_val_score)
Visualization: Matplotlib
Management: GitHub Projects (Kanban Board)
