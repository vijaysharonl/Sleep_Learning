# 🧠 Sleep Training for Neural Networks

Can deep learning models benefit from something like sleep?

This project introduces **Artificial Sleep Cycles** into training deep neural networks — inspired by how biological sleep helps the brain consolidate memory, suppress noise, and generalize better.

---

## 📘 Concept: What is Sleep Training?

In neuroscience, sleep involves:

- **Memory consolidation**  
- **Synaptic pruning**  
- **Spontaneous activity (noise)**  

We translate this into deep learning via **Sleep Phases**:

| Phase         | Behavior                                       |
|---------------|------------------------------------------------|
| 🟦 Wake Phase | Standard training on clean (x, y)              |
| 🟫 Sleep Phase| Train on **noisy inputs** and **random labels**|

This alternation (like REM and non-REM cycles) encourages models to:

- Generalize better by escaping sharp minima  
- Drop spurious correlations  
- Develop more robust internal representations

---

## 🧪 Datasets Used

We evaluated Sleep Training across 3 public datasets of varying complexity:

- 🧬 **Breast Cancer** (binary classification, tabular)  
- 🔢 **Digits** (image classification, moderate noise)  
- 💉 **Diabetes** (noisy regression-style classification)

Each experiment used:

- 30 total epochs  
- Sleep every 5th epoch  
- 3 random seeds for robustness  
- Comparison with **Normal Training** and **Dropout**

---

## 📈 Results Overview

- Sleep training **recovers quickly** after each sleep phase  
- Accuracy often **rebounds stronger** post-sleep  
- Comparable or better final performance than Dropout  
- Most effective on **noisy data** (e.g., diabetes)



---

## 📊 Key Findings

- Sleep acts as a **phasic regularizer**  
- Helps models avoid overfitting and spurious features  
- **Architecture-agnostic**: No changes needed to model structure  
- Lightweight: ~1% training time overhead  

---

