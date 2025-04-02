# ICML_Rebuttal

## Revised Ablation Study
![Alt text](https://github.com/yixuehenshang/ICML_Rebuttal/blob/main/ablation_plot_rebuttal.png)

Figure 2. Ablation study of the PSV-PPO framework across two molecular optimization tasks (Osimertinib MPO and Fexofenadine MPO). Each row corresponds to a task, and columns represent four evaluation metrics: (1) Score — average optimization objective; (2) Valid Rate — proportion of syntactically valid SMILES; (3) Duplicated in Generation — number of duplicate molecules among generated samples (lower is better); (4) Computation Time — wall-clock time per epoch. We compare the full PSV-PPO model with ablated variants removing Partial SMILES Validation (WO_PSV), Global Pattern Suppression (WO_GPS), Token Probability Control (WO_TPC), and Length Penalty (WO_PL). REINFORCE serves as a baseline. Removing PSV leads to rapid validity collapse and training failure, while ablations of GPS or TPC result in increased mode collapse. The full PSV-PPO maintains high validity, diverse generations, and strong optimization performance with moderate computational cost. For clarity of visualization, the Duplicated in Generation and Computation Time metrics are capped at 100 and 50, respectively.

---

## PSV Exploration
![Alt text](https://github.com/yixuehenshang/ICML_Rebuttal/blob/main/Exploration.png)

Figure 1: Comparison between conventional reinforcement learning (RL) exploration (a) and PSV-guided RL exploration (b) in SMILES molecule generation. In (a), the model sequentially generates tokens without guidance, which can lead to invalid SMILES (red node: IV), halting the generation and yielding invalid outputs. In contrast, (b) illustrates our PSV-guided approach, where at each generation step, all possible next-token options are evaluated using partial SMILES validation (light green nodes: PV). This allows the model to perform a "what-if" analysis before committing to a token, reducing the risk of generating invalid sequences and improving exploration efficiency within the valid chemical space (dark green node: V).

---

