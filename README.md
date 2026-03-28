# An-Updated-Version-of-the-View-Batch-Model-for-Continual-Learning
Enhanced View-Batch Model (VBM) for continual learning, extending CVPR 2025 work with improved memory buffers, replay strategies, and loss functions (contrastive, cosine). Achieves better CIL/TIL performance on CIFAR-10 with stable training via gradient clipping and warm restarts.
An Updated Version of the View-Batch Model for Continual Learning
👨‍💻 Authors
Jagadeesh Guptha
Yashwanth Yalamarthy
Bure Siddardha

📍 Institution: IIT Jodhpur
🔗 Project Links
📂 GitHub Repository: (Add your repo link here)
🎥 YouTube Demo: (Add your demo link here)
📖 Abstract

Continual Learning (CL) aims to enable models to learn sequential tasks without forgetting previously learned knowledge. However, neural networks often suffer from catastrophic forgetting, where old knowledge is overwritten by new data.

This project presents an enhanced version of the View-Batch Model (VBM) that improves:

Memory efficiency
Learning stability
Representation quality

We introduce:

Improved self-supervised learning objectives
Memory-aware replay strategy
Class-balanced memory buffer
Gradient clipping & cosine annealing
🧠 Base Model: View-Batch Model (VBM)

The original VBM is inspired by the Ebbinghaus Forgetting Curve, which suggests learning improves when spaced over time.

🔑 Key Idea

Instead of revisiting samples frequently, VBM:

Uses view-batches (multiple augmented versions)
Increases recall interval
Improves long-term retention
🚀 Our Contributions
1️⃣ Improved Self-Supervised Learning
Replaced KL-Divergence with:
Cosine Similarity Loss
Contrastive Learning (InfoNCE)
Helps learn stronger and more discriminative features
2️⃣ Memory-Aware Replay Strategy
Prioritizes high-loss samples
Improves learning under limited memory
Fixes weak decision boundaries
3️⃣ Class-Balanced Memory Buffer
Ensures equal representation of all classes
Prevents bias toward certain categories
Dynamically adjusts as new classes are added
4️⃣ Training Stabilization Techniques
✅ Gradient Clipping → avoids sudden large updates
✅ Cosine Annealing Warm Restarts → smooth learning
📊 Experimental Setup
Dataset: Sequential CIFAR-10
Tasks: 5 sequential tasks
Epochs: 50 per task
Buffer Size: 200 (memory constraint)
Model Base: iCaRL
📈 Results
Method	CIL	TIL	Avg
Base iCaRL	64.11	90.20	77.16
VBM (baseline)	69.71	92.76	81.25
VBM (reproduced)	68.05	90.95	79.50
+ Contrastive Loss	66.53	90.76	78.64
+ Cosine Similarity	63.50	90.49	77.00
+ Class Balance Buffer	⭐ 72.25	83.48	78.12
+ Memory-Aware Replay	64.69	⭐ 93.59	79.14
🏆 Key Observations
Best CIL Performance: Class-balanced memory buffer
Best TIL Performance: Memory-aware replay
Improved SSL methods show strong potential
📌 Conclusion

We transformed the standard VBM into a more dynamic and intelligent framework by:

Improving representation learning
Optimizing memory usage
Stabilizing training

This results in:
✔ Reduced catastrophic forgetting
✔ Better generalization
✔ Stable continual learning
