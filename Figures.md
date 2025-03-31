# ICML_Rebuttal

## PSV Novelty

Figure 1: Comparison between conventional reinforcement learning (RL) exploration (a) and PSV-guided RL exploration (b) in SMILES molecule generation. In (a), the model sequentially generates tokens without guidance, which can lead to invalid SMILES (red node: IV), halting the generation and yielding invalid outputs. In contrast, (b) illustrates our PSV-guided approach, where at each generation step, all possible next-token options are evaluated using partial SMILES validation (light green nodes: PV). This allows the model to perform a "what-if" analysis before committing to a token, reducing the risk of generating invalid sequences and improving exploration efficiency within the valid chemical space (dark green node: V).

### Explanation:
Figure 1 illustrates the core novelty of our method: integrating partial SMILES validation (PSV) directly into the training loop of reinforcement learning for molecular generation. In standard autoregressive generation, as shown in panel (a), the model makes sequential decisions without feedback on the validity of intermediate sequences. This blind sampling often leads to early invalid terminations, causing wasted computation and contributing to catastrophic forgetting.

Our method, shown in panel (b), introduces a PSV-guided exploratory framework. At each generation step, instead of choosing a single token, we simulate potential next-token candidates across the entire vocabulary and preemptively assess their validity using partial SMILES validation. This "what-if" branching strategy allows the model to identify invalid continuations before they are sampled and thus refine its policy using informative gradients. This process effectively turns SMILES validity from a post-hoc filtering problem into a differentiable training signal, enabling the model to proactively learn structural constraints while exploring diverse chemical paths.

This figure visually conveys how our approach differs from and improves upon traditional RL methods by encouraging validity-aware exploration, which not only mitigates catastrophic forgetting but also facilitates more reliable and efficient molecule generation.

---

## Revised Ablation Study


