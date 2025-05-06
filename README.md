# Protein-Protein Interaction (PPI) Prediction with RNNs (LSTM & GRU)

## Overview
Protein-protein interactions (PPIs) govern critical cellular processes like metabolic pathways, signal transduction, and disease mechanisms (e.g., cancer, neurological disorders). Accurate PPI prediction enables breakthroughs in drug discovery and biomedical research.  

This repository implements **recurrent neural networks (RNNs)**—specifically **LSTM** and **GRU**—to model sequential patterns in protein sequences for PPI prediction. Models are trained on curated datasets to improve accuracy over traditional methods.

---

## Repository Structure
1. **Data Preparation**  
   - [`Dataset_Generator.ipynb`](Dataset_Generator.ipynb): Generates customized datasets (CD-hit, num_samples, ratio,confidence_score) for models input. 
   - [`Dataset_Prep.ipynb`](Dataset_Prep.ipynb): creates raw PPI datasets (e.g., from UniProt/STRING) with protein sequences and interaction labels.    

2. **Model Implementation & Results**  
   - [`GRU_PPI.ipynb`](GRU_PPI.ipynb): **GRU-based model** for PPI prediction with performance evaluation.  
   - [`LSTM_PPI.ipynb`](LSTM_PPI.ipynb): **LSTM-based model** with comparative analysis against GRU.  

---

## Key Features
- **Sequential Modeling**: LSTM/GRU architectures capture long-range dependencies in protein sequences.  
- **Data Integration**: Processes sequence data from standardized sources (e.g., UniProt).  
- **Benchmarking**: Compares RNN performance metrics (Precision and Recall,accuracy, F1-score,Confusion Matrix).  

---

## Usage
1. **Data Pipeline**:  
   - Run `Dataset_Prep.ipynb` to fetch raw data and create the full dataset.  
   - Run  `Dataset_Generator.ipynb`.  to generate custom dataset as required.

2. **Training Models**:  
   - Execute `GRU_PPI.ipynb` or `LSTM_PPI.ipynb` to train/evaluate models.  

---

## Dependencies
- Python ≥ 3.8  
- Libraries: `TensorFlow/Keras`, `Pandas`, `NumPy`, `Scikit-learn`  

Install requirements:  
```bash
pip install tensorflow pandas numpy scikit-learn
```

---

## Results
Both LSTM and GRU models leverage sequential protein data to predict PPIs, achieving competitive accuracy. See notebooks for detailed metrics.  

---

## Future Work
- Incorporate attention mechanisms (e.g., Transformers) for enhanced sequence modeling.  
- Expand to multi-task learning (e.g., predicting interaction types).  

---

## References
- UniProt, STRING database  
- Literature on RNNs for bioinformatics  

**License**: [MIT](LICENSE)  

---
