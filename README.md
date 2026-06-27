# 🔬 The Scattering Law — Exploratory Research on Information Distribution in Semitic Morphology

> An independent research project exploring how root-scatter affects neural language model performance in Semitic languages (Arabic, Hebrew, Amharic).

---

## 🌌 Overview

For decades, the difficulty of Neural Language Models in processing Semitic languages has been commonly attributed to "data scarcity" or "tokenization issues."

**This project investigates an alternative hypothesis**: that the difficulty stems, at least in part, from a structural property of root-and-pattern morphology — specifically, the spatial scatter of root radicals within a word.

Through a systematic empirical study, we observed a pattern we call the **Scattering Law**: a roughly linear decay in a model's ability to perceive morphological boundaries as the distance between root radicals increases. This is treated here as an exploratory finding, not a finalized scientific claim.

---

## 📐 The Mathematical Formulation

We define the **Scattering Degree (S)** as:

$$S = (\text{span of root radicals}) - (\text{number of radicals})$$

Our preliminary empirical observations suggest that the **Neural Lift** (the gain in boundary detection over random chance) follows an approximately linear decay:

$$\text{Lift} \approx \beta_0 - \beta_1 \cdot S$$

Where $\beta_1$ is what we informally call the **"Blindness Coefficient"**. When $S$ exceeds a critical threshold (empirically observed around $\approx 3.7$ in our experiments), the model's predictive power appears to drop sharply — a region we refer to as the **"Blind Zone"**.

> ⚠️ **Important caveat**: The constants above ($\beta_0$, $\beta_1$, the 3.7 threshold) are empirical observations from our experiments, not universal constants. Independent replication is encouraged.

---

## 🌍 Cross-Language Observations

We tested the Scattering Law hypothesis across three Semitic languages in our experiments:

| Language | Observation | Correlation |
|---|---|---|
| Arabic | Pattern confirmed | $\beta_1 \approx 0.11$ |
| Hebrew | Pattern confirmed | $r = -0.81$ |
| Amharic | Pattern confirmed | $r = -0.91$ |

These results are promising but preliminary. They have **not** been peer-reviewed yet, and the sample sizes vary across languages. We share them in the spirit of open research.

---

## 🧠 The Transformer Observation

A secondary observation from this research: while Attention mechanisms (Transformers) improve general performance, they **do not appear to eliminate** the Scattering Law pattern in our experiments. This suggests — but does not prove — that the difficulty may be an instrumental property of sequence-to-sequence processing of scattered dependencies, rather than a failure of a specific layer type.

More rigorous experiments are needed to confirm this.

---

## 🛠️ Repository Structure

```
semitic-scattering-law/
├── README.md              ← this file
├── docs/                  ← technical notes and theoretical derivations
└── scripts/
    └── reproduce_law.py   ← script to reproduce the empirical plots
```

### Quick Start

```bash
git clone https://github.com/faresrafat3/semitic-scattering-law.git
cd semitic-scattering-law
pip install numpy matplotlib
python scripts/reproduce_law.py
```

This will generate a plot at `plots/scattering_law_comparison.png` showing the empirical Neural Lift vs. Scattering Degree for both RNN and Transformer models.

---

## 📊 Status

- **Phase**: Exploratory research (pre-publication)
- **Peer review**: Not yet submitted
- **Replication**: Welcome — please open an issue if you replicate or contradict
- **Sample size**: Limited; results are preliminary

---

## 🤝 Related Projects

This research is part of a broader exploration of Semitic NLP tooling. Related repos:

- [`semitic-router`](https://github.com/faresrafat3/semitic-router) — A routing module that uses the Scattering Degree to decide between neural and symbolic correction paths.
- [`hayy-correct`](https://github.com/faresrafat3/hayy-correct) — A length-aware seq2seq model for Arabic text correction (work in progress).

---

## 📜 License

MIT — see [LICENSE](LICENSE).

---

## 📫 Contact

- GitHub: [@faresrafat3](https://github.com/faresrafat3)
- Issues: Please use the [Issues tab](https://github.com/faresrafat3/semitic-scattering-law/issues) for questions, replications, or critiques.

---

## 🙏 Acknowledgments

This is an independent research project. We welcome feedback, corrections, and replication attempts from the NLP community.
