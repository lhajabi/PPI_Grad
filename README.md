# Protein-Protein Interaction (PPI) Prediction with RNNs and GNNs

## Overview
Protein-protein interactions (PPIs) are fundamental to cellular functions, governing processes like metabolic pathways, signal transduction, and regulatory mechanisms. Dysregulation in PPIs is linked to diseases such as cancer, neurological disorders, and metabolic dysfunctions. Accurate PPI prediction is critical for advancing biomedical research and therapeutic development.  

This repository explores machine learning approaches for PPI prediction, leveraging **recurrent neural networks (RNNs)**—specifically **LSTM** and **GRU**—combined with **Graph Neural Networks (GNNs)** to model sequential and structural dependencies in protein data. The models are trained on curated datasets to improve prediction accuracy over traditional methods.

---

## Repository Structure
1. **Data Preparation**  
   - [`Dataset_Generator.ipynb`](Dataset_Generator.ipynb): Generates the raw PPI dataset from sources like UniProt/STRING, including protein sequences and interaction labels.  
   - [`Dataset_Prep.ipynb`](Dataset_Prep.ipynb): Preprocesses the raw data (e.g., tokenization, padding, graph construction) for model input.  

2. **Model Implementation & Results**  
   - [`GRU_PPI.ipynb`](GRU_PPI.ipynb): Implements a **Gated Recurrent Unit (GRU)**-based model for PPI prediction and evaluates performance.  
   - [`LSTM_PPI.ipynb`](LSTM_PPI.ipynb): Implements a **Long Short-Term Memory (LSTM)**-based model and compares results with the GRU approach.  

---

## Key Features
- **Hybrid Architecture**: Combines RNNs (for sequential protein data) and GNNs (for interaction networks).  
- **Data Integration**: Processes heterogeneous datasets (e.g., sequences from UniProt, interactions from STRING).  
- **Performance Focus**: Benchmarks LSTM/GRU models against baseline methods.  

---

## Usage
1. **Data Pipeline**:  
   - Run `Dataset_Generator.ipynb` to fetch/generate raw data.  
   - Use `Dataset_Prep.ipynb` to preprocess data into train/test splits.  

2. **Training Models**:  
   - Execute `GRU_PPI.ipynb` or `LSTM_PPI.ipynb` to train and evaluate the respective models.  

---

## Dependencies
- Python ≥ 3.8  
- Libraries: `TensorFlow/Keras`, `PyTorch` (for GNNs), `NetworkX`, `Pandas`, `NumPy`  

Install requirements:  
```bash
pip install -r requirements.txt  # (include a requirements.txt in your repo)
```

---

## Results
Both LSTM and GRU models achieve competitive accuracy in PPI prediction by capturing:  
- **Temporal dependencies** in protein sequences (via RNNs).  
- **Graph-structured interactions** (via GNNs).  

See notebooks for detailed metrics (e.g., precision, recall, F1-score).  

---

## Future Work
- Incorporate attention mechanisms (e.g., Transformers) for long-range sequence modeling.  
- Expand GNN integration to handle larger PPI networks.  

---

## References
- UniProt, STRING database  
- Related papers on PPI prediction with deep learning  

---

**License**: [MIT](LICENSE)  

---

This README provides a clear, modular breakdown of your project while highlighting its scientific relevance. Adjust hyperlinks/license as needed. Let me know if you’d like to emphasize any specific technical details!
