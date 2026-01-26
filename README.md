# Development and Validation of a A Dual-Level AI Framework for Quantitative Histological Assessment of Ex-Situ Perfused Rat Livers

This repository contains the source code and methodology associated with the thesis project: *"A Dual-Level AI Framework for Quantitative Histological Assessment of Ex-Situ Perfused Rat Livers"*.

## 📄 Project Description
**Ex-situ sub-normothermic machine perfusion (SNMP)** is a promising strategy to increase the availability of viable liver grafts for transplantation. However, current methods for assessing graft viability rely heavily on subjective semi-quantitative scoring systems, lacking the precision required for optimal clinical decision-making.

This project proposes an **Artificial Intelligence (Deep Learning)** system capable of identifying and quantifying subtle histological patterns that differentiate a liver before ("Pre") and after ("Post") undergoing machine perfusion, aiming to provide an objective tool for graft assessment.

## 🔬 Methodology
The study employs a **dual-level** approach based on Convolutional Neural Networks (CNNs) to analyze rat liver histological samples:

1. **Data:** H&E stained rat liver sections (Pre-perfusion vs. Post-perfusion).
2. **Models:**
    * **Hepatocyte CNN:** Trained on **8,390** single hepatocyte images.
    * **Tissue CNN:** Trained on **6,960** histological patches.
3. **Validation:** Explainable AI (Grad-CAM) and Radiomics (Random Forest) to ensure biological relevance.
4. **Deployment:** Interactive **Streamlit** web application for whole-slide scoring.


## 📊 Visualization & Explainability
The codebase implements algorithms to generate **average saliency maps** to answer: *What histological features does the model focus on for each class?*

* **Pre-perfusion Map:** Visualization of baseline tissue characteristics and normal architecture.
* **Post-perfusion Map:** Identification of specific morphological changes (e.g., edema) induced by the perfusion process.
* **Difference Map:** Mathematical subtraction (`Post - Pre`) to highlight the intensity and localization of histological alterations detected by the AI.

## 💻 Requirements
The project is developed in Python and requires the following main libraries (based on the visualization scripts):

* Deep Learning Framework: `tensorflow` (Keras)
* Data Manipulation: `numpy`
* Image Processing:`Pillow` (PIL), `scikit-image`
* Machine Learning Utils: `scikit-learn`
* Visualization: `matplotlib`, `seaborn`

## 📂 Project Resources (OneDrive)

Due to file size constraints, the complete codebase and trained models are hosted on **OneDrive** in the folder named **`Liver_ML_Models_UC-UV`**.

### 🔗 [https://postgradouvcl-my.sharepoint.com/:f:/g/personal/nicolas_diazv_postgrado_uv_cl/IgAjd-_zhNKjQKpwIPaibLgCAS-qiFSub4_M75NGS5efHyo?e=4Qc8Ft]

**Folder Contents:**
* **`Hepatocyte_CNN`**: Notebook containing the training pipeline, validation metrics, and saliency maps for the single-cell classifier.
* **`Tissue_CNN`**: Notebook containing the training pipeline, validation metrics, and saliency maps for the tissue-level classifier.
* **`cell.h5`**: Pre-trained model weights for the hepatocyte classifier.
* **`tissue.h5`**: Pre-trained model weights for the tissue classifier.
  
## 📝 Project Status
* **Manuscript:** Finalized.
* **Validation:** Concluded. Saliency map analysis has been validated, confirming the model's ability to identify relevant morphological patterns associated with perfusion injury.

## 🤝 Acknowledgments & Affiliations

This project is a collaborative effort involving:

* **Universidad de Valparaíso (UV):** Research developed at the **Centro Interdisciplinario de Investigación Biomédica e Ingeniería para la Salud (MEDING)**.
* **Pontificia Universidad Católica de Chile (UC):** Research originating from the **Instituto de Ingeniería Biológica y Médica (IIBM)**, associated with the supporting **FONDECYT** project.

---
**Author:** [Your Name]
**Institutions:** Universidad de Valparaíso & Pontificia Universidad Católica de Chile
