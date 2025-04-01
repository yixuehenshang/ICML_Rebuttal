# ICML_Rebuttal

## PSV Exploration
![Alt text](https://github.com/yixuehenshang/ICML_Rebuttal/blob/main/Exploration.png)

Figure 1: Comparison between conventional reinforcement learning (RL) exploration (a) and PSV-guided RL exploration (b) in SMILES molecule generation. In (a), the model sequentially generates tokens without guidance, which can lead to invalid SMILES (red node: IV), halting the generation and yielding invalid outputs. In contrast, (b) illustrates our PSV-guided approach, where at each generation step, all possible next-token options are evaluated using partial SMILES validation (light green nodes: PV). This allows the model to perform a "what-if" analysis before committing to a token, reducing the risk of generating invalid sequences and improving exploration efficiency within the valid chemical space (dark green node: V).

---

## Revised Ablation Study
![Alt text](https://github.com/yixuehenshang/ICML_Rebuttal/blob/main/ablation_plot_rebuttal.png)

