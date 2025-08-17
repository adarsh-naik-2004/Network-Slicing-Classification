# 5G Network Slicing Classification

This project implements a machine learning pipeline to classify **5G network slices** into three categories:

* **eMBB (Enhanced Mobile Broadband)**
* **URLLC (Ultra-Reliable Low Latency Communication)**
* **mMTC (Massive Machine Type Communication)**

The system leverages a KNN classifier with optimized hyperparameters to achieve high accuracy on real-world network slicing datasets.

---

## Features

* **Preprocessing & Optimization**: Reduced dataset memory usage by **86%** using efficient data types
* **KNN Classification**: Achieved **93% accuracy** with `n_neighbors=3`
* **Evaluation Metrics**: Accuracy, Precision, Recall, F1-score, Confusion Matrix
* **Hyperparameter Tuning**: Tested different values of *k (2–8)* and analyzed trade-offs in accuracy and runtime
* **Visualization**: Plotted confusion matrices and accuracy trends for clear model insights

---

## Dataset

* **Size**: \~31,000 rows
* **Columns**: Use Case, LTE/5G Category, Technology Supported, Day, Time, GBR, Packet Loss Rate, Packet Delay, Slice Type
* **Target Variable**: `Slice Type` → {`eMBB`, `URLLC`, `mMTC`}

---

## Tech Stack

* **Python**
* **Scikit-learn** – Model building & evaluation
* **Pandas, NumPy** – Data preprocessing
* **Matplotlib** – Performance visualization

---

## Results

* **Best Model**: KNN with `n_neighbors=3`
* **Accuracy**: 93%
* **Confusion Matrix**: Demonstrated strong performance across all slice types
* **Execution Time Analysis**: Balanced accuracy vs runtime for different `k` values

---

## Example Outputs

* Confusion Matrix for KNN classification
* Accuracy vs `k` plot
* Tabular predictions on test data

---

## Future Improvements

* Experiment with advanced classifiers (Random Forest, XGBoost, Neural Networks)
* Deploy real-time classification with streaming data
* Extend dataset with more diverse 5G slicing scenarios

---

## How to Run

```bash
# Clone repository
git clone https://github.com/yourusername/5g-network-slicing.git
cd 5g-network-slicing

# Install dependencies
pip install -r requirements.txt

# Run training
python train.py

# Run evaluation
python evaluate.py
```

---

