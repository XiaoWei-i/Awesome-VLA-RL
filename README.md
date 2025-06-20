# Awesome-VLA-RL

With significant advances in **Vision-Language-Action (VLA)🍔** models based on large-scale imitation learning, integrating VLA with **Reinforcement Learning (RL)🥤** has emerged as a promising paradigm. This paradigm leverages the benefits of trial-and-error interactions with environments or pre-collected sub-optimal data.

This repository summarizes recent advances in the **VLA🍔 + RL🥤** paradigm and provides a classification of relevant works (offline RL training(without env.), online RL training(with env.), test-time RL(during deployment), and RL alignment).

**Contributions are welcome! Please feel free to submit an issue or reach out via email to add papers!**

If you find this repository useful, please giving this list a star ⭐. Feel free to share it with others!

# **Offline RL**

The Offline RL pre-trained VLA models leverage both human demonstrations and autonomously collected data.

| Method | Title | Venue | Date | Code/Project | Key feature/finding |
| --- | --- | --- | --- | --- | --- |
| [Q-Transformer](https://arxiv.org/abs/2309.10150) | Q-Transformer: Scalable Offline Reinforcement Learning via Autoregressive Q-Functions | Arxiv | 18/9/2023 | [Github](https://github.com/lucidrains/q-transformer) | <details><summary>Details</summary>offline Q-learning with Transformer models: 1. Autoregressive Discrete Q-Learning; 2. Conservative Q-Learning; 3. Monte Carlo and n-step Returns</details> |
| [Perceiver-Actor-Critic](https://arxiv.org/abs/2402.05546) | Offline Actor-Critic Reinforcement Learning Scales to Large Models | ICML2024 | 8/2/2024 | [Project](https://sites.google.com/view/perceiver-actor-critic) | <details><summary>Details</summary>An offline actor-critic method that scales to large models of up to 1B parameters and learn a wide variety of 132 control and robotics tasks</details> |
| [GeRM](https://arxiv.org/abs/2403.13358) | GeRM: A Generalist Robotic Model with Mixture-of-experts for Quadruped Robot | IROS2024 | 20/3/2024 | [Github](https://github.com/Songwxuan/GeRM) | <details><summary>Details</summary>Mixtureof-Experts structure; Quadruped robot learning</details> |
| [ReinboT](https://arxiv.org/abs/2505.07395) | ReinboT: Amplifying Robot Visual-Language Manipulation with Reinforcement Learning | ICML2025 | 12/5/2025 |  | <details><summary>Details</summary>Max-Return Sequence Modeling as Reinformer; Reward Densification with heuristic methods</details> |
| [MoRE](https://arxiv.org/abs/2503.08007) | MoRE: Unlocking Scalability in Reinforcement Learning for Quadruped Vision-Language-Action Models | ICRA2025 | 11/3/2025 |  | <details><summary>Details</summary>Integrates multiple low-rank adaptation modules as distinct experts within a dense multi-modal large language model (MLLM), forming a sparse-activated mixture-of-experts model</details> |


# **Online RL**
With trial-and-error interactions in online environments, VLA models can be further optimized to improve their performance.

## **in Simulator**

| Method | Title | Venue | Date | Code/Project | Key feature/finding |
| --- | --- | --- | --- | --- | --- |
| [FLaRe](https://arxiv.org/abs/2409.16578) | FLaRe: Achieving Masterful and Adaptive Robot Policies with Large-Scale Reinforcement Learning Fine-Tuning | ICRA 2025 Best Paper Finalist | 30/9/2024 | [Code](https://github.com/JiahengHu/FLaRe) | <details><summary>Details</summary>For **large-scale fine-tuning in simulation**, it performs extensive domain randomization, extract visual features through DinoV2, and utilize the KV-cache technique during inference and a set of algorithmic choices to **ensure the stability of RL fine-tuning** </details> |
| [PA-RL](https://arxiv.org/abs/2412.06685) | Policy Agnostic RL: Offline RL and Online RL Fine-Tuning of Any Class and Backbone | Arxiv | 9/12/2024 | [Project](https://policyagnosticrl.github.io/) | <details><summary>Details</summary>a single method that fine-tunes multiple policy classes, with varying architectures and sizes. It enables sample-efficient improvement of diffusion and transformer-based autoregressive policies. PA-RL sets a new state of the art for offline to online RL, and **it makes it possible, for the first time, to improve OpenVLA** </details> |
| [iRe-VLA](https://arxiv.org/abs/2501.16664) | Improving Vision-Language-Action Model with Online Reinforcement Learning | RAL2025 | 28/1/2025 |  | <details><summary>Details</summary>Adopt SFT & RL two-stage iterative optimization to **Stabilizing Training Process** and **Managing the Model Training Burden**.</details> |
| [RIPT-VLA](https://arxiv.org/abs/2505.17016) | Interactive Post-Training for Vision-Language-Action Models | Arxiv | 22/5/2025 | [Github](https://github.com/Ariostgx/ript-vla) | <details><summary>Details</summary>A critic-free optimization framework called Leave-One-Out Proximal Policy Optimization (LOOP); Dynamic rollout sampling</details> |
| [VLA-RL](https://arxiv.org/abs/2505.18719) | VLA-RL: Towards Masterful and General Robotic Manipulation with Scalable Reinforcement Learning | Arxiv | 24/5/2025 | [Github](https://github.com/GuanxingLu/vlarl) | <details><summary>Details</summary>Robotic process reward model and the VLA-RL System with (1) Curriculum Selection Strategy (2) Critic Warmup (3) GPU-balanced Vectorized Environments (4) PPO infrastructure</details> |
| [RLVLA](https://arxiv.org/abs/2505.19789) | What Can RL Bring to VLA Generalization? An Empirical Study | Arxiv | 26/5/2025 | [Github](https://github.com/gen-robot/RL4VLA) |  <details><summary>Details</summary>PPO consistently outperforms GRPO and DPO; Shared actor-critic backbone; VLA warm-up</details> |
| [RFTF](https://arxiv.org/abs/2505.19767) | RFTF: Reinforcement Fine-tuning for Embodied Agents with Temporal Feedback | Arxiv | 26/5/2025 |  |  <details><summary>Details</summary>For the sparse reward problem, RFTF leverages **a value model trained using temporal information** to generate dense rewards</details> |
| SimpleVLA-RL |  | Github | 5/2025 | [Github](https://github.com/PRIME-RL/SimpleVLA-RL) |  |
| [TGRPO](https://arxiv.org/abs/2506.08440) | TGRPO: Fine-tuning Vision-Language-Action Model via Trajectory-wise Group Relative Policy Optimization | Arxiv | 10/6/2025 | [Github](https://github.com/hahans/TGRPO) | From **GRPO in LLM** to **TGRPO in VLA**  |


## **in Real-World**

| Method | Title | Venue | Date | Code/Project | Key feature/finding |
| --- | --- | --- | --- | --- | --- |
| [RLDG](https://arxiv.org/abs/2412.09858) | RLDG: Robotic Generalist Policy Distillation via Reinforcement Learning | RSS2025 | 12/2024 | [Project](https://generalist-distillation.github.io/) | <details><summary>Details</summary>Pretrain task-specific RL policies with HIL-SERL; Distill RL policies into VLA for Knowledge Transfer.</details> |
| [PA-RL](https://arxiv.org/abs/2412.06685) | Policy Agnostic RL: Offline RL and Online RL Fine-Tuning of Any Class and Backbone | Arxiv | 9/12/2024 | [Project](https://policyagnosticrl.github.io/) | <details><summary>Details</summary>a single method that fine-tunes multiple policy classes, with varying architectures and sizes. It enables sample-efficient improvement of diffusion and transformer-based autoregressive policies. PA-RL sets a new state of the art for offline to online RL, and **it makes it possible, for the first time, to improve OpenVLA** </details> |
| [iRe-VLA](https://arxiv.org/abs/2501.16664) | Improving Vision-Language-Action Model with Online Reinforcement Learning | RAL2025 | 28/1/2025 |  | <details><summary>Details</summary>Adopt SFT & RL two-stage iterative optimization to **Stabilizing Training Process** and **Managing the Model Training Burden**.</details> |
| [ConRFT](https://arxiv.org/abs/2502.05450) | ConRFT: A Reinforced Fine-tuning Method for VLA Models via Consistency Policy | RSS2025 | 14/4/2025 | [Github](https://github.com/cccedric/conrft) | <details><summary>Details</summary>Offline fine-tuning(Cal-QL+PA-RL) and online fine-tuning(CPQL+HIL-SERL+PA-RL) </details> |
| DYNA-1 | Dynamism v1 (DYNA-1) Model: A Breakthrough in Performance and Production-Ready Embodied AI |  | 5/2025 | [Project](https://www.dyna.co/research) | |

# Test-Time RL
Leverage a value function pre-trained via offline RL.

| Method | Title | Venue | Date | Code/Project | Key feature/finding |
| --- | --- | --- | --- | --- | --- |
| [Bellman-Guided Retrials](https://arxiv.org/abs/2406.15917) | To Err is Robotic: Rapid Value-Based Trial-and-Error during Deployment | Arxiv | 22/6/2024 | [Github](https://github.com/nakamotoo/V-GPS) | <details><summary>Details</summary>Pre-train a value function to estimate task completion, recover the robot and sample a new strategy if failed</details> |
| [V-GPS](https://arxiv.org/abs/2410.13816) | Steering Your Generalists: Improving Robotic Foundation Models via Value Guidance | CoRL2024 | 17/10/2024 | [Project](https://sites.google.com/view/to-err-robotic/home) | <details><summary>Details</summary>Re-ranking multiple action proposals from a generalist policy using a value function at test-time</details> |
| [Hume](https://arxiv.org/abs/2505.21432) | Hume: Introducing System-2 Thinking in Visual-Language-Action Model | Arxiv | 2/6/2025 | [Github](https://github.com/hume-vla/hume) | <details><summary>Details</summary> Pre-train a value function, perform best-of-N selection of candidate action chunks with state-action value estimation</details> |



# RL Alignment

| Method | Title | Venue | Date | Code/Project | Key feature/finding |
| --- | --- | --- | --- | --- | --- |
| [GRAPE](https://openreview.net/pdf?id=XnwyFD1Fvw) | GRAPE: Generalizing Robot Policy via Preference Alignment | ICLR2025 workshop | 4/2/2025 | [Github](https://github.com/aiming-lab/grape) | <details><summary>Details</summary>Trajectory-wise Preference Optimization aligns VLA policies on a trajectory level</details> |
| [SafeVLA](https://arxiv.org/abs/2503.03480) | SafeVLA: Towards Safety Alignment of Vision-Language-Action Model via Constrained Learning | Arxiv | 31/5/2025 | [Project](https://pku-safevla.github.io/) | <details><summary>Details</summary>Constraining VLA policies via safe reinforcement learning</details> |

# Unclassified

| Method | Title | Venue | Date | Code/Project | Key feature/finding |
| --- | --- | --- | --- | --- | --- |
| [RPD](https://arxiv.org/abs/2503.05833) | Refined Policy Distillation: From VLA Generalists to RL Experts | Arxiv | 6/3/2025 |  | <details><summary>Details</summary>Leverage VLA model as policy prior to improve sample-efficiency of RL, as Jump-Start RL</details> |