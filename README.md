# Development and Validation of a A Dual-Level AI Framework for Quantitative Histological Assessment of Ex-Situ Perfused Rat Livers

This repository contains the source code and methodology associated with the thesis project: *"A Dual-Level AI Framework for Quantitative Histological Assessment of Ex-Situ Perfused Rat Livers"*.

## 📄 Project Description
Chronic liver failure (CLF) and the critical disparity between patients on the waiting list and available donors drive the search for novel organ preservation strategies. **Ex-situ machine perfusion** has emerged as a promising alternative to extend organ viability.

This project proposes an **Artificial Intelligence (Deep Learning)** system capable of identifying and quantifying subtle histological patterns that differentiate a liver before ("Pre") and after ("Post") undergoing machine perfusion, aiming to provide an objective tool for graft assessment.

## 🔬 Methodology
The study employs a **dual-level** approach based on Convolutional Neural Networks (CNNs) to analyze rat liver histological samples:

1.  **Tissue Level:** Classification of tissue patches to assess general architecture and structural integrity.
2.  **Cellular Level:** Analysis focused on specific nuclear and cellular morphological features.
3.  **Interpretability (XAI):** Implementation of **Saliency Maps** to visualize which specific image regions (e.g., sinusoids, cytoplasm, nuclei) the model utilizes to make its decisions.

## 📊 Visualization & Explainability
The codebase includes algorithms to generate average attention maps to answer: *What features does the model focus on for each class?*

* **Pre-perfusion Map:** Visualization of baseline tissue characteristics.
* **Post-perfusion Map:** Identification of morphological changes induced by the perfusion process.
* **Difference Map:** Mathematical subtraction (`Post - Pre`) to highlight specific histological alterations detected by the AI.

## 💻 Requirements
The project is developed in Python and requires the following main libraries (based on the visualization scripts):

* `numpy` (Matrix processing)
* `matplotlib` (Plotting and heatmaps generation)
* `tensorflow` / `keras` (Model loading and gradient calculation)
* `opencv-python` (Image processing)

## 📂 Repository Structure
* `src/models/`: Definition of CNN architectures (Tissue Level and Cellular Level).
* `src/saliency_maps.py`: Script for gradient calculation and heatmap generation (Pre vs Post).
* `data/`: (Not included in repo) Digitized rat liver histological samples.

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
