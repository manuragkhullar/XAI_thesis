📚 XAI Thesis Code Repository
This repository contains the official code and experiments for the Master's Thesis:

Title: Improving Explainability of Transformer Models

🛠️ Overview
This thesis proposes two novel methods to improve the faithfulness and interpretability of Transformer attention mechanisms:

**Selective Attention Rollout**

  Selectively composes attention matrices across layers based on their dissimilarity, reducing noise amplification during Attention Rollout.
  
  Improves Spearman correlation with input gradients by 6.5× for BERT-base and 3.1× for BERT-large.

**Network Diffusion for Attention Smoothing**

  Applies a diffusion process to the attention matrices, based on singular value transformation.
  
  Enhances the clarity of attention maps by propagating meaningful signals and suppressing noise.

The experiments include evaluation on SST-2 (GLUE benchmark) for text classification and ImageNet samples for Vision Mamba models.

📂 **Repository Contents**
**4_01_experiments.py:** Main script for running Selective Attention Rollout experiments on BERT-base and BERT-large using SST-2 data.

**Network Diffusion_Attention Visualisation.ipynb**: Jupyter Notebook demonstrating Network Diffusion for smoothing attention maps (Vision Mamba examples).

🧪 **Key Experiments**
**Selective Attention Rollout:**

Calculate Spearman rank correlation between attention scores and input gradient saliency.

Compare standard Attention Rollout vs. selective layer composition based on Frobenius norm distance.

**Network Diffusion:**

Apply singular value-based diffusion to attention matrices.

Visualize before-and-after attention heatmaps for vision models.

🚀 Getting Started
Clone the repository:

bash
Copy
Edit
git clone https://github.com/manuragkhullar/XAI_thesis.git
cd XAI_thesis
Install required Python packages:

nginx
Copy
Edit
pip install -r requirements.txt
Run experiments:

For BERT Selective Rollout: run 4_01_experiments.py

For Vision Diffusion: open Network Diffusion_Attention Visualisation.ipynb

## Acknowledgments

This repository builds upon and adapts code from the following open-source projects:

- [Attention Rollout](https://github.com/samiraabnar/attention_flow) by Samira Abnar and Willem Zuidema (ACL 2020): "Quantifying Attention Flow in Transformers."

- [The Hidden Attention of Mamba](https://github.com/microsoft/hidden-state-mamba) by Ameen Ali, Itamar Zimerman, and Lior Wolf (Tel Aviv University, 2024): Official PyTorch implementation.
