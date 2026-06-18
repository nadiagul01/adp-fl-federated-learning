ADP-FL: Adaptive Differential Privacy for Fair, Robust Federated Learning

An adaptive differential privacy mechanism for federated learning that personalizes noise injection per client based on data heterogeneity.

Overview

Standard differentially private federated learning applies uniform noise to all clients, disproportionately harming those with small or imbalanced datasets under non-IID conditions. ADP-FL scales per-client noise based on dataset size, label entropy, and gradient variance, preserving both privacy and fairness.

Key Highlights


Designed a personalized noise-scaling function based on each client's dataset size, label entropy, and gradient variance.
Implemented the full pipeline: client-side heterogeneity profiling, gradient clipping, personalized Gaussian noise injection, and server aggregation, with Rényi Differential Privacy accounting.
Evaluated on CIFAR-10 (Dirichlet α=0.5, 20 clients): ADP-FL achieved 25.22% accuracy, matching the non-private FedAvg baseline (25.10%), versus 19.76% for fixed-noise DP.
Characterized the privacy-utility trade-off explicitly (ADP-FL ε=100.75 vs. Fixed DP ε=12.19 at δ=10⁻⁵).
Ablation study confirmed the full multi-metric formulation outperforms single-metric noise scaling.


Tech Stack

Python, PyTorch, Differential Privacy, Federated Learning

Advisor

Dr. Hina Ayaz — Department of Computer Science, FAST-NU

Author

Nadia Gul — MS Computer Science, FAST-NUCES
