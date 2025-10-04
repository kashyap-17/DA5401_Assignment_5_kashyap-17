### **Assignment: Dimensionality Reduction and Manifold Learning for Multi-Label Data**

**Student Information**

  * **Name:** Kashyap Shankar Iyer
  * **Roll Number:** DA25C012

-----

**Documentation**

This submission consists of a single Jupyter Notebook file containing all code, visualizations, and analysis for the assignment. Its purpose is to explore and compare non-linear dimensionality reduction techniques to understand the complex, high-dimensional structure of a multi-label biological dataset. This notebook applies t-Distributed Stochastic Neighbor Embedding (t-SNE) and Isomap to the Yeast dataset, analyzing the resulting visualizations to infer properties about the data's manifold and the separability of its functional classes.

-----

**Folder Structure**

```
.
└── Kashyap_DA25C012_Assignment_Manifold_Learning.ipynb
```

-----

**Dataset Information**

The analysis is based on the **Yeast** dataset, sourced from the **MULAN (MUlti-Label learNing) repository**. The dataset contains 2,417 genes, each described by 103 features derived from microarray expression data. The goal is to predict which of the 14 functional classes a gene belongs to, where each gene can belong to multiple classes simultaneously. [http://mulan.sourceforge.net/datasets-mlc.html]

-----

**Notebook Structure and Content**

The notebook is organized into the following sections to guide the reader through the analysis:

  * **Part A: Data Loading and Preprocessing**
    This section covers loading the `.arff` dataset, separating the 103 features from the 14 binary labels, and preparing the data for analysis. It includes applying **Standardization** to the feature matrix to ensure all features contribute equally to the distance-based algorithms.

  * **Part B: Visualization Strategy and Label Simplification**
    To create clear and interpretable visualizations, the complex 14-label system is simplified into a single categorical variable. This section details the process of identifying the most frequent **single-label classes** and the most frequent **multi-label combinations** to create a new 4-category target variable used exclusively for coloring the plots. I have explored two such classifications and used both for interprating the dimentionality reduction techniques.

  * **Part C: Dimensionality Reduction and Visualization**
    This is the core section where dimensionality reduction techniques are applied to the scaled feature matrix to project it into a 2D space. It involves:

    1.  **t-SNE (t-Distributed Stochastic Neighbor Embedding):** Applying t-SNE and experimenting with the `perplexity` hyperparameter (e.g., 5, 30, 50) to find the visualization that best reveals local cluster structures.
    2.  **Isomap (Isometric Mapping):** Applying Isomap to create a 2D embedding that preserves the global geodesic structure of the data manifold.

  * **Part D: Comparative Analysis and Interpretation**
    This section provides a detailed analysis of the resulting visualizations from both t-SNE and Isomap.