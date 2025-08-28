# Contextual Bias Training with Causality Compensated Attention

This repository contains experiments and results from my work on **causality and contextual bias in visual recognition**, inspired by the paper *Causality Compensated Attention for Contextual Biased Visual Recognition* (Ruyang Liu, Jingjia Huang, Thomas H. Li, Ge Li, 2023).

The main notebook demonstrates how causal interventions can improve attention mechanisms, reduce contextual bias, and enhance model robustness in classification and object detection tasks.

---

## 📌 Overview

- **Why Causality Matters**: Attention mechanisms help models focus on features, but they often misinterpret context (e.g., predicting *spoon* because of *dining table*).  
- **Causal View**: Context acts as a confounder, leading to false associations.  
- **Solution**: Intervention Dual Attention (IDA) — a new attention module that uses multi-sampling and reweighting to cut spurious correlations:contentReference[oaicite:1]{index=1}.  

---

## 🎯 Aim and Objectives
- **Aim**: Improve attention mechanisms by reducing contextual bias in vision tasks.  
- **Objectives**:
  - Understand how current models are affected by contextual bias.  
  - Develop and apply the **IDA module**.  
  - Evaluate performance on benchmarks like MS-COCO and Pascal VOC:contentReference[oaicite:2]{index=2}.  

---

## 🛠️ Methodology (IDA)
- **Baseline**: Spatial Class-Aware Attention (SCA).  
- **Multi-Sampling (MS-SCA)**: Generates diverse feature views to simulate intervention.  
- **Dual Attention**: A second attention layer (Dot-Product or Transformer) reweights features, ensuring causal focus:contentReference[oaicite:3]{index=3}.  

**Training Setup**:
- Epochs: 80  
- Batch Size: 32  
- Learning Rate: 0.0001  
- Optimizer: Adam:contentReference[oaicite:4]{index=4}  

---

## 📊 Results
- **Multi-label classification (MS-COCO)**: Achieved mAP of **48.6%**.  
- **Evaluation**: IDA improved predictions across categories like *person, cat, dog, car,* and *bicycle*.  
- **Interpretation**: By cutting contextual influence, IDA produced more accurate predictions and attention maps:contentReference[oaicite:5]{index=5}.  

---

## ✅ Conclusion
- IDA addresses contextual bias using causal inference.  
- Reduces predictions influenced by irrelevant context, leading to **robust and accurate recognition**.  
- Future extensions: applying IDA to video recognition and other high-dimensional tasks:contentReference[oaicite:6]{index=6}.  

---

## 📖 References
- He, K., Zhang, X., Ren, S., & Sun, J. (2016). *Deep residual learning for image recognition*. CVPR.  
- Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, Ł., & Polosukhin, I. (2017). *Attention is all you need*. NeurIPS.  
- Pearl, J. (2009). *Causality: Models, reasoning, and inference*. Cambridge University Press.  
- Lin, T.-Y., Maire, M., Belongie, S., et al. (2014). *Microsoft COCO: Common objects in context*. ECCV:contentReference[oaicite:7]{index=7}.  

---

## 👤 Author
**Olaluwoye Olalekan**  
African Masters in Machine Intelligence (AMMI), AIMS Senegal  
GitHub: [olaluwoye9](https://github.com/olaluwoye9)

---

