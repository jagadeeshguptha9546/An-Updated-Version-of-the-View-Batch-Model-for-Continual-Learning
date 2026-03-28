# 📘 An Updated Version of the View-Batch Model for Continual Learning

> Enhanced continual learning model to reduce catastrophic forgetting using improved memory strategies and self-supervised learning.

---

## 🚀 Features
- Improved Self-Supervised Learning (Contrastive + Cosine Similarity)
- Memory-Aware Replay Strategy
- Class-Balanced Memory Buffer
- Gradient Clipping & Cosine Annealing

---

## 📂 Project Structure
```bash
An-Updated-Version-of-the-View-Batch-Model/
│── src/              # Source code
│── models/           # Saved models
│── data/             # Dataset
│── notebooks/        # Jupyter notebooks
│── train.py          # Training script
│── requirements.txt  # Dependencies
│── README.md         # Documentation
```

---

## 🧠 Problem Statement
Continual Learning models suffer from **catastrophic forgetting**, where learning new tasks degrades performance on previously learned tasks. This project aims to solve this issue by improving memory replay and learning stability.

---

## 💡 Approach / Methodology
- Use **View-Batch Model (VBM)** to increase recall intervals
- Replace KL-Divergence with:
  - Contrastive Learning
  - Cosine Similarity Loss
- Implement **Memory-Aware Replay**
- Maintain **Class-Balanced Buffer**
- Apply **Gradient Clipping & Warm Restarts**

---

## 🛠️ Tech Stack
- Python
- PyTorch
- NumPy
- Matplotlib

---

## 📊 Results

| Method | CIL | TIL | Avg |
|------|------|------|------|
| Base iCaRL | 64.11 | 90.20 | 77.16 |
| VBM (baseline) | 69.71 | 92.76 | 81.25 |
| VBM (reproduced) | 68.05 | 90.95 | 79.50 |
| + Contrastive Loss | 66.53 | 90.76 | 78.64 |
| + Cosine Similarity | 63.50 | 90.49 | 77.00 |
| + Class Balance Buffer | **72.25** | 83.48 | 78.12 |
| + Memory-Aware Replay | 64.69 | **93.59** | 79.14 |

---

## ⚙️ Installation
```bash
git clone https://github.com/your-username/your-repo.git
cd An-Updated-Version-of-the-View-Batch-Model
pip install -r requirements.txt
```

---

## ▶️ Usage
```bash
python train.py
```

---

## 📸 Outputs
(Add your graphs, plots, or screenshots here)

---

## 🔗 Links
- 📂 GitHub: https://github.com/your-username/your-repo
- 🎥 Demo: Add your YouTube link here

---

## 👨‍💻 Contributors
- Jagadeesh Guptha  
- Yashwanth Yalamarthy  
- Bure Siddardha  

---
## 📬 Contact
For queries:
- GitHub: https://github.com/your-username
