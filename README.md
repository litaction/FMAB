Robust Federated Multi-Armed Bandits Under Byzantine Attacks
This repository contains the source code and report for our project: Enhanced Federated Multi-Armed Bandits (FMAB), developed as part of our coursework at IIIT Allahabad.

🚀 Overview
Federated Multi-Armed Bandits (FMAB) combine the power of federated learning and multi-armed bandits to enable decentralized, privacy-preserving decision making. However, these systems are highly vulnerable to Byzantine attacks where malicious clients can degrade performance.

Our work enhances the baseline Fed-MoM-UCB algorithm by introducing two key techniques to improve robustness and reliability:

✅ Trust-Based Weighting (TBW): Dynamically penalizes clients whose updates consistently deviate from consensus.
✂️ Median-of-Trimmed-Means (MTM): Combines trimmed mean and median-of-means to eliminate the effect of outlier or adversarial updates.
🧠 Key Contributions
Robust Aggregation Strategy: Aggregates local updates by discarding extreme values and weighing client contributions based on trust.
Trust Score Mechanism: Assigns trust weights to each client, reducing the influence of historically unreliable (Byzantine) participants.
Sublinear Regret: Our algorithm achieves low regret even with 10–49% Byzantine clients in the system.
Empirical Evaluation: Demonstrates superior performance over Fed2-UCB and Plain MoM-UCB in terms of cumulative regret, stability, and convergence.
📊 Results
Our enhanced Robust MoM-UCB algorithm:

Shows lower cumulative regret (both with and without communication cost).
Stabilizes arm selection faster and more accurately.
Successfully isolates Byzantine clients through trust decay.
Outperforms baseline methods across all metrics.
Plots include:

Cumulative Regret
Remaining Arms over Time
Trust Score Evolution
🧪 Experimental Setup
Parameter	Value
Number of Arms	40
Clients	100
Byzantine Ratio	10%
Trimming Ratio	10%
Reward Noise (σ²)	2
Client Noise (σc²)	0.022
Phases	15
Trust Decay Factor	0.9
Synthetic data is used to simulate heterogeneous clients and adversarial conditions.

📁 Project Structure
.
├── src/                      # Source code for simulation and algorithms
├── plots/                    # Generated performance plots
├── report_FMAB.pdf           # Full project report with theoretical and empirical analysis
├── README.md                 # You're here
