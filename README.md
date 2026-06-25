# 🔬 The Scattering Law: A Physical Limit of Information Distribution in Semitic Morphology

## 🌌 The Discovery
For decades, the "failure" of Neural Language Models in processing Semitic languages was attributed to "data scarcity" or "tokenization issues." 

**We have proven that this is a misconception.**

Through a systematic study of root-and-pattern morphology, we discovered the **Scattering Law**: a fundamental linear decay in a model's ability to perceive morphological boundaries as the distance between root radicals increases. This is not a data problem; it is an **Information Distribution Limit**.

## 📐 The Mathematical Core
We define the **Scattering Degree ($S$)** as:
$$S = (\text{span of root radicals}) - (\text{number of radicals})$$

Our empirical evidence shows that the **Neural Lift** (the gain in boundary detection over random chance) follows a strict linear decay:
$$\text{Lift} = \beta_0 - \beta_1 \cdot S$$

Where $\beta_1$ represents the **"Blindness Coefficient"**. When $S$ exceeds a critical threshold (typically $\approx 3.7$), the model enters the **"Blind Zone"**, where its predictive power collapses.

## 🌍 Semitic Universality
The law is not language-specific. We validated the Scattering Law across the Semitic family:
- **Arabic**: Confirmed ($\beta_1 \approx 0.11$).
- **Hebrew**: Confirmed (Stronger correlation, $r = -0.81$).
- **Amharic**: Confirmed (Extreme correlation, $r = -0.91$).

## 🧠 The Transformer Paradox
A pivotal part of this research is the "Transformer Test." While Attention mechanisms improve general performance, they **do not eliminate the Scattering Law**. This proves that the blindness is an **Instrumental Limit** of sequence-to-sequence processing of scattered dependencies, rather than a failure of a specific layer type.

## 🛠️ Repository Structure
- `/docs`: Contains the full **Technical Report** and theoretical derivations.
- `/scripts`: Tools to calculate $S$ and reproduce the Scattering Law plots.
- `/data`: Sample datasets demonstrating the "Blind Zone" across different languages.

---
*This research is a cornerstone of the **Mir'aah Intelligence** ecosystem, leading to the development of the `semitic-router` and `hayy-correct`.*
