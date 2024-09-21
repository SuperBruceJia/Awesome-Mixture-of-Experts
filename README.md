# Awesome Mixture of Experts (MoE)
Awesome Mixture of Experts (MoE): A Curated List of Mixture of Experts (MoE) and Mixture of Multimodal Experts (MoME)

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/SuperBruceJia/Awesome-Mixture-of-Experts) 
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Made With Love](https://img.shields.io/badge/Made%20With-Love-red.svg)](https://github.com/SuperBruceJia/Awesome-Mixture-of-Experts)

This repository, called **Mixture of Experts**, contains a collection of resources and papers on **Mixture of Experts (MoE)** and **Mixture of Multimodal Experts (MoME)**.

*Welcome to share your papers, thoughts, and ideas by [submitting an issue](https://github.com/SuperBruceJia/Awesome-Mixture-of-Experts/issues/new)!* 

## Contents
- [Course](#Course)
- [Presentations](#Presentations)
- [Books](#Books)
- [Papers](#Papers)
  - [Survey](#Survey)
  - [Foundation Work](#Foundational-Work)
  - [Sparse Gating Mechanism](#Sparse-Gating-Mechanism)
    - [Auxiliary Load Balancing Loss](#Auxiliary-Load-Balancing-Loss)
    - [Expert Capacity Limit](#Expert-Capacity-Limit)
    - [Non-trainable Gating Mechanism](#Non-trainable-Gating-Mechanism)
    - [Expert-choice Gating](#Expert-choice-Gating)
  - [Dense Gating Mechanism](#Dense-Gating-Mechanism)
  - [Soft Gating Mechanism](#Soft-Gating-Mechanism)
    - [Token Merging](#Token-Merging)
    - [Expert Merging](#Expert-Merging)
- [Acknowledgement](#Acknowledgement)

# Course
**Stanford CS324: Large Language Models**\
_Percy Liang, Tatsunori Hashimoto, Christopher Ré_\
[[Link](https://stanford-cs324.github.io/winter2022/lectures/selective-architectures/#mixture-of-experts)]\
Winter 2022

# Presentations

# Books
**The Path to Artificial General Intelligence: Insights from Adversarial LLM Dialogue**\
*Edward Y. Chang*\
SocraSynth.com, [[Link](https://www.amazon.com/dp/1962463303)]\
March 2024

**Foundation Models for Natural Language Processing: Pre-trained Language Models Integrating Media**\
*Gerhard Paaß, Sven Giesselbach*\
Artificial Intelligence: Foundations, Theory, and Algorithms (Springer Nature), [[Link](https://link.springer.com/book/10.1007/978-3-031-23190-2)]\
16 Feb 2023

# Papers
## Survey
**A Survey on Mixture of Experts**\
_Weilin Cai, Juyong Jiang, Fan Wang, Jing Tang, Sunghun Kim, Jiayi Huang_\
arXiv, [[Paper](https://arxiv.org/abs/2407.06204)] [[GitHub](https://github.com/withinmiaov/A-Survey-on-Mixture-of-Experts)]\
8 Aug 2024

**Routers in Vision Mixture of Experts: An Empirical Study**\
_Tianlin Liu, Mathieu Blondel, Carlos Riquelme, Joan Puigcerver_\
Transactions on Machine Learning Research (TMLR), [[Paper](https://arxiv.org/abs/2401.15969)]\
18 Apr 2024

## Foundation Work
**Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer**\
_Noam Shazeer, Azalia Mirhoseini, Krzysztof Maziarz, Andy Davis, Quoc Le, Geoffrey Hinton, Jeff Dean_\
ICLR 2017, [[Paper](https://arxiv.org/abs/1701.06538)]\
23 Jan 2017

**Adaptive Mixtures of Local Experts**\
_Robert A. Jacobs, Michael I. Jordan, Steven J. Nowlan, Geoffrey E. Hinton_\
Neural Computation, [[Paper](https://ieeexplore.ieee.org/abstract/document/6797059)]\
March 1991

## Sparse Gating Mechanism
_**A subset of experts is activated.**_
**MoE-LLaVA: Mixture of Experts for Large Vision-Language Models**\
_Bin Lin, Zhenyu Tang, Yang Ye, Jiaxi Cui, Bin Zhu, Peng Jin, Jinfa Huang, Junwu Zhang, Yatian Pang, Munan Ning, Li Yuan_\
arXiv, [[Paper](https://arxiv.org/abs/2401.15947)] [[Codes](https://github.com/PKU-YuanGroup/MoE-LLaVA)]\
6 Jul 2024

**Mixtral of Experts**\
_Albert Q. Jiang, Alexandre Sablayrolles, Antoine Roux, Arthur Mensch, Blanche Savary, Chris Bamford, Devendra Singh Chaplot, Diego de las Casas, Emma Bou Hanna, Florian Bressand, Gianna Lengyel, Guillaume Bour, Guillaume Lample, Lélio Renard Lavaud, Lucile Saulnier, Marie-Anne Lachaux, Pierre Stock, Sandeep Subramanian, Sophia Yang, Szymon Antoniak, Teven Le Scao, Théophile Gervet, Thibaut Lavril, Thomas Wang, Timothée Lacroix, William El Sayed_\
arXiv, [[Paper](https://arxiv.org/abs/2401.04088)]\
8 Jan 2024

**Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer**\
_Noam Shazeer, Azalia Mirhoseini, Krzysztof Maziarz, Andy Davis, Quoc Le, Geoffrey Hinton, Jeff Dean_\
ICLR 2017, [[Paper](https://arxiv.org/abs/1701.06538)]\
23 Jan 2017

**M6-T: Exploring Sparse Expert Models and Beyond**\
_An Yang, Junyang Lin, Rui Men, Chang Zhou, Le Jiang, Xianyan Jia, Ang Wang, Jie Zhang, Jiamang Wang, Yong Li, Di Zhang, Wei Lin, Lin Qu, Jingren Zhou, Hongxia Yang_\
arXiv, [[Paper](https://arxiv.org/abs/2105.15082)]\
9 Aug 2021

### Auxiliary Load Balancing Loss

### Expert Capacity Limit

### Non-trainable Gating Mechanism

### Expert-choice Gating

## Dense Gating Mechanism
_**All the experts are activated.**_

## Soft Gating Mechanism
_The fully differentiable approaches include input **Token Merging** and **Expert Merging**._

### Token Merging

### Expert Merging

# Acknowledgement
This project is sponsored by the [PodGPT](https://podgpt.org/) group, Kolachalama Laboratory at Boston University.

<a href="https://podgpt.org/"> <img width="500" src="https://github.com/user-attachments/assets/84e28a61-d69b-47d3-a8db-d3605f4562e0"></a>
