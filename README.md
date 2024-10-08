# Awesome Mixture of Experts (MoE)
Awesome Mixture of Experts: A Curated List of Mixture of Experts (MoE) and Mixture of Multimodal Experts (MoME)

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/SuperBruceJia/Awesome-Mixture-of-Experts) 
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Made With Love](https://img.shields.io/badge/Made%20With-Love-red.svg)](https://github.com/SuperBruceJia/Awesome-Mixture-of-Experts)

This repository, called **Awesome Mixture of Experts**, contains a collection of resources and papers on **Mixture of Experts (MoE)** and **Mixture of Multimodal Experts (MoME)**.

*Welcome to share your papers, thoughts, and ideas by [submitting an issue](https://github.com/SuperBruceJia/Awesome-Mixture-of-Experts/issues/new)!* 

## Contents
- [Course](#Course)
- [Presentation](#Presentation)
- [Books](#Books)
- [Papers](#Papers)
  - [Survey](#Survey)
  - [Foundational Work](#Foundational-Work)
    - [Sparse-Gated Mixture of Experts in Transformer](#Sparse-Gated-Mixture-of-Experts-in-Transformer)
    - [Sparse-Gated Mixture of Experts in LSTM](#Sparse-Gated-Mixture-of-Experts-in-LSTM)
    - [Hierarchical Mixtures of Experts for the EM Algorithm](#Hierarchical-Mixtures-of-Experts-for-the-EM-Algorithm)
    - [Mixtures of Experts Architecture](#Mixtures-of-Experts-Architecture)
  - [Sparse Gating Mechanism](#Sparse-Gating-Mechanism)
    - [Parameter-efficient Fine-tuning](#Parameter-efficient-Fine-tuning)
    - [Auxiliary Load Balance Loss](#Auxiliary-Load-Balance-Loss)
      - [Load Balance Loss](#Load-Balance-Loss)
      - [z-loss](#z-loss)
      - [Mutual Information Loss](#Mutual-Information-Loss)
    - [Expert Capacity Limit](#Expert-Capacity-Limit)
    - [Non-trainable Gating Mechanism](#Non-trainable-Gating-Mechanism)
      - [Random Assignment](#Random-Assignment)
      - [Domain Mapping](#Domain-Mapping)
    - [Expert-choice Gating](#Expert-choice-Gating)
    - [From Dense to Sparse](#From-Dense-to-Sparse)
      - [Sparse Upcycling](#Sparse-Upcycling)
      - [Sparse Splitting](#Sparse-Splitting)
  - [Dense Gating Mechanism](#Dense-Gating-Mechanism)
  - [Soft Gating Mechanism](#Soft-Gating-Mechanism)
    - [Token Merging](#Token-Merging)
    - [Expert Merging](#Expert-Merging)
- [Acknowledgement](#Acknowledgement)

# Course
**CS324: Large Language Models - Selective Architectures**\
_Percy Liang, Tatsunori Hashimoto, Christopher Ré_\
Stanford University, [[Link](https://stanford-cs324.github.io/winter2022/lectures/selective-architectures/#mixture-of-experts)]\
Winter 2022

**CSC321: Introduction to Neural Networks and Machine Learning - Mixtures of Experts**\
_Geoffrey Hinton_\
University of Toronto, [[Link](https://www.cs.toronto.edu/~hinton/csc321/notes/lec15.pdf)]\
Winter 2014

**CS2750: Machine Learning - Ensamble Methods and Mixtures of Experts**\
_Milos Hauskrecht_\
University of Pittsburgh, [[Link](https://people.cs.pitt.edu/~milos/courses/cs2750-Spring04/lectures/class22.pdf)]\
Spring 2004

# Presentation
**Mixture-of-Experts in the Era of LLMs: A New Odyssey**\
_Tianlong Chen, Yu Cheng, Beidi Chen, Minjia Zhang, Mohit Bansal_\
ICML 2024, [[Link](https://moe-tutorial.github.io/)] [[Slides](https://icml.cc/media/icml-2024/Slides/35222_1r94S59.pdf#page=1.00)]\
2024

# Books
**The Path to Artificial General Intelligence: Insights from Adversarial LLM Dialogue**\
_Edward Y. Chang_\
Stanford University, [[Link](https://www.amazon.com/dp/1962463303)]\
March 2024

**Foundation Models for Natural Language Processing: Pre-trained Language Models Integrating Media**\
_Gerhard Paaß, Sven Giesselbach_\
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
TMLR, [[Paper](https://arxiv.org/abs/2401.15969)]\
18 Apr 2024

## Foundational Work
### Sparse-Gated Mixture of Experts in Transformer
**Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity**\
_William Fedus, Barret Zoph, Noam Shazeer_\
JMLR, [[Paper](https://arxiv.org/abs/2101.03961)]\
16 Jun 2022

### Sparse-Gated Mixture of Experts in LSTM
**Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer**\
_Noam Shazeer, Azalia Mirhoseini, Krzysztof Maziarz, Andy Davis, Quoc Le, Geoffrey Hinton, Jeff Dean_\
ICLR 2017, [[Paper](https://arxiv.org/abs/1701.06538)]\
23 Jan 2017

### Hierarchical Mixtures of Experts for the EM Algorithm
**Hierarchical Mixtures of Experts and the EM Algorithm**\
_Michael I. Jordan, Robert A. Jacobs_\
Neural Computation, [[Paper](https://www.cs.toronto.edu/~hinton/absps/hme.pdf)]\
1993

### Mixtures of Experts Architecture
**Adaptive Mixtures of Local Experts**\
_Robert A. Jacobs, Michael I. Jordan, Steven J. Nowlan, Geoffrey E. Hinton_\
Neural Computation, [[Paper](https://ieeexplore.ieee.org/abstract/document/6797059)]\
1991

## Sparse Gating Mechanism
**Uni-MoE: Scaling Unified Multimodal LLMs with Mixture of Experts**\
_Yunxin Li, Shenyuan Jiang, Baotian Hu, Longyue Wang, Wanqi Zhong, Wenhan Luo, Lin Ma, Min Zhang_\
arXiv, [[Paper](https://arxiv.org/abs/2405.11273)]\
18 May 2024

**_Fine-grained and Shared Experts_ - DeepSeekMoE: Towards Ultimate Expert Specialization in Mixture-of-Experts Language Models**\
_Damai Dai, Chengqi Deng, Chenggang Zhao, R.X. Xu, Huazuo Gao, Deli Chen, Jiashi Li, Wangding Zeng, Xingkai Yu, Y. Wu, Zhenda Xie, Y.K. Li, Panpan Huang, Fuli Luo, Chong Ruan, Zhifang Sui, Wenfeng Liang_\
arXiv, [[Paper](https://arxiv.org/abs/2401.06066)]\
11 Jan 2024

**_Mistral AI_ - Mixtral of Experts**\
_Albert Q. Jiang, Alexandre Sablayrolles, Antoine Roux, Arthur Mensch, Blanche Savary, Chris Bamford, Devendra Singh Chaplot, Diego de las Casas, Emma Bou Hanna, Florian Bressand, Gianna Lengyel, Guillaume Bour, Guillaume Lample, Lélio Renard Lavaud, Lucile Saulnier, Marie-Anne Lachaux, Pierre Stock, Sandeep Subramanian, Sophia Yang, Szymon Antoniak, Teven Le Scao, Théophile Gervet, Thibaut Lavril, Thomas Wang, Timothée Lacroix, William El Sayed_\
arXiv, [[Paper](https://arxiv.org/abs/2401.04088)]\
8 Jan 2024

**PaCE: Unified Multi-modal Dialogue Pre-training with Progressive and Compositional Experts**\
_Yunshui Li, Binyuan Hui, ZhiChao Yin, Min Yang, Fei Huang, Yongbin Li_\
ACL 2023, [[Paper](https://arxiv.org/abs/2305.14839)]\
13 Jun 2023

**Scaling Vision-Language Models with Sparse Mixture of Experts**\
_Sheng Shen, Zhewei Yao, Chunyuan Li, Trevor Darrell, Kurt Keutzer, Yuxiong He_\
arXiv, [[Paper](https://arxiv.org/abs/2303.07226)]\
13 Mar 2023

**_Mixture of Attention Heads (MoA)_ - Mixture of Attention Heads: Selecting Attention Heads Per Token**\
_Xiaofeng Zhang, Yikang Shen, Zeyu Huang, Jie Zhou, Wenge Rong, Zhang Xiong_\
EMNLP 2022, [[Paper](https://arxiv.org/abs/2210.05144)]\
11 Oct 2022

**Multimodal Contrastive Learning with LIMoE: the Language-Image Mixture of Experts**\
_Basil Mustafa, Carlos Riquelme, Joan Puigcerver, Rodolphe Jenatton, Neil Houlsby_\
arXiv, [[Paper](https://arxiv.org/abs/2206.02770)]\
6 Jun 2022

**_Pyramid Design of Experts_ - DeepSpeed-MoE: Advancing Mixture-of-Experts Inference and Training to Power Next-Generation AI Scale**\
_Samyam Rajbhandari, Conglong Li, Zhewei Yao, Minjia Zhang, Reza Yazdani Aminabadi, Ammar Ahmad Awan, Jeff Rasley, Yuxiong He_\
ICML 2022, [[Paper](https://arxiv.org/abs/2201.05596)]\
21 Jul 2022

**_k-group Top-1 Routing for Expert Prototyping_ - M6-T: Exploring Sparse Expert Models and Beyond**\
_An Yang, Junyang Lin, Rui Men, Chang Zhou, Le Jiang, Xianyan Jia, Ang Wang, Jie Zhang, Jiamang Wang, Yong Li, Di Zhang, Wei Lin, Lin Qu, Jingren Zhou, Hongxia Yang_\
arXiv, [[Paper](https://arxiv.org/abs/2105.15082)]\
9 Aug 2021

**Scaling Vision with Sparse Mixture of Experts**\
_Carlos Riquelme, Joan Puigcerver, Basil Mustafa, Maxim Neumann, Rodolphe Jenatton, André Susano Pinto, Daniel Keysers, Neil Houlsby_\
arXiv, [[Paper](https://arxiv.org/abs/2106.05974)]\
10 Jun 2021

**_Routing as a Linear Assignment Problem_ - BASE Layers: Simplifying Training of Large, Sparse Models**\
_Mike Lewis, Shruti Bhosale, Tim Dettmers, Naman Goyal, Luke Zettlemoyer_\
arXiv, [[Paper](https://arxiv.org/abs/2103.16716)]\
30 Mar 2021

### Parameter-efficient Fine-tuning
**_Shared FFN_ - MixLoRA: Enhancing Large Language Models Fine-Tuning with LoRA-based Mixture of Experts**\
_Dengchun Li, Yingzi Ma, Naizheng Wang, Zhengmao Ye, Zhiyuan Cheng, Yinghao Tang, Yan Zhang, Lei Duan, Jie Zuo, Cal Yang, Mingjie Tang_\
arXiv, [[Paper](https://arxiv.org/abs/2404.15159)]\
20 Jul 2024

**_FFN_ - MoE-LLaVA: Mixture of Experts for Large Vision-Language Models**\
_Bin Lin, Zhenyu Tang, Yang Ye, Jiaxi Cui, Bin Zhu, Peng Jin, Jinfa Huang, Junwu Zhang, Yatian Pang, Munan Ning, Li Yuan_\
arXiv, [[Paper](https://arxiv.org/abs/2401.15947)] [[Codes](https://github.com/PKU-YuanGroup/MoE-LLaVA)]\
6 Jul 2024

**_"q_proj", "v_proj" (InstructBLIP) and "up_proj", "down_proj" (LLaVA-1.5)_ - MoCLE: Mixture of Cluster-conditional LoRA Experts for Vision-language Instruction Tuning**\
_Yunhao Gou, Zhili Liu, Kai Chen, Lanqing Hong, Hang Xu, Aoxue Li, Dit-Yan Yeung, James T. Kwok, Yu Zhang_\
arXiv, [[Paper](https://arxiv.org/abs/2312.12379)]\
4 Jul 2024

**_All the Layers_ - Omni-SMoLA: Boosting Generalist Multimodal Models with Soft Mixture of Low-rank Experts**\
_Jialin Wu, Xia Hu, Yaqing Wang, Bo Pang, Radu Soricut_\
arXiv, [[Paper](https://arxiv.org/abs/2312.00968)]\
2 Apr 2024

**_FFN_ - LoRAMoE: Alleviate World Knowledge Forgetting in Large Language Models via MoE-Style Plugin**\
_Shihan Dou, Enyu Zhou, Yan Liu, Songyang Gao, Jun Zhao, Wei Shen, Yuhao Zhou, Zhiheng Xi, Xiao Wang, Xiaoran Fan, Shiliang Pu, Jiang Zhu, Rui Zheng, Tao Gui, Qi Zhang, Xuanjing Huang_\
arXiv, [[Paper](https://arxiv.org/abs/2312.09979)]\
8 Mar 2024

**_"q_proj", "p_proj"_ - MoELoRA: Contrastive Learning Guided Mixture of Experts on Parameter-Efficient Fine-Tuning for Large Language Models**\
_Tongxu Luo, Jiahe Lei, Fangyu Lei, Weihao Liu, Shizhu He, Jun Zhao, Kang Liu_\
arXiv, [[Paper](https://arxiv.org/abs/2402.12851)]\
20 Feb 2024

**_FFN_ - MoRAL: MoE Augmented LoRA for LLMs' Lifelong Learning**\
_Shu Yang, Muhammad Asif Ali, Cheng-Long Wang, Lijie Hu, Di Wang_\
arXiv, [[Paper](https://arxiv.org/abs/2402.11260)]
17 Feb 2024

**_All the Layers_ - MoLA: Higher Layers Need More LoRA Experts**\
_Chongyang Gao, Kezhen Chen, Jinmeng Rao, Baochen Sun, Ruibo Liu, Daiyi Peng, Yawen Zhang, Xiaoyuan Guo, Jie Yang, VS Subrahmanian_\
arXiv, [[Paper](https://arxiv.org/abs/2402.08562)]\
13 Feb 2024

**_FFN_ - LLaVA-MoLE: Sparse Mixture of LoRA Experts for Mitigating Data Conflicts in Instruction Finetuning MLLMs**\
_Shaoxiang Chen, Zequn Jie, Lin Ma_\
arXiv, [[Paper](https://arxiv.org/abs/2401.16160)]\
30 Jan 2024

**_Attention Projections_ - SiRA: Sparse Mixture of Low Rank Adaptation**\
_Yun Zhu, Nevan Wichers, Chu-Cheng Lin, Xinyi Wang, Tianlong Chen, Lei Shu, Han Lu, Canoee Liu, Liangchen Luo, Jindong Chen, Lei Meng_\
arXiv, [[Paper]([15 Nov 2023](https://arxiv.org/abs/2311.09179))]\
15 Nov 2023

**_Mixture of Vectors (MoV)_ & _Mixture of LORA (MoLORA)_ - Pushing Mixture of Experts to the Limit: Extremely Parameter Efficient MoE for Instruction Tuning**\
_Ted Zadouri, Ahmet Üstün, Arash Ahmadian, Beyza Ermiş, Acyr Locatelli, Sara Hooker_\
arXiv, [[Paper](https://arxiv.org/abs/2309.05444)]\
11 Sep 2023

**AdaMix: Mixture-of-Adaptations for Parameter-efficient Model Tuning**\
_Yaqing Wang, Sahaj Agarwal, Subhabrata Mukherjee, Xiaodong Liu, Jing Gao, Ahmed Hassan Awadallah, Jianfeng Gao_\
EMNLP 2022, [[Paper](https://arxiv.org/abs/2205.12410)]\
2 Nov 2022

### Auxiliary Load Balance Loss
#### Load Balance Loss
**_Load Balance Loss_ - MixLoRA: Enhancing Large Language Models Fine-Tuning with LoRA-based Mixture of Experts**\
_Dengchun Li, Yingzi Ma, Naizheng Wang, Zhengmao Ye, Zhiyuan Cheng, Yinghao Tang, Yan Zhang, Lei Duan, Jie Zuo, Cal Yang, Mingjie Tang_\
arXiv, [[Paper](https://arxiv.org/abs/2404.15159)]\
20 Jul 2024

**_Load Balance Loss_ - MoE-LLaVA: Mixture of Experts for Large Vision-Language Models**\
_Bin Lin, Zhenyu Tang, Yang Ye, Jiaxi Cui, Bin Zhu, Peng Jin, Jinfa Huang, Junwu Zhang, Yatian Pang, Munan Ning, Li Yuan_\
arXiv, [[Paper](https://arxiv.org/abs/2401.15947)] [[Codes](https://github.com/PKU-YuanGroup/MoE-LLaVA)]\
6 Jul 2024

**_Load Balance Loss and Router z-loss_ - JetMoE: Reaching Llama2 Performance with 0.1M Dollars**\
_Yikang Shen, Zhen Guo, Tianle Cai, Zengyi Qin_\
arXiv, [[Paper](https://arxiv.org/abs/2404.07413)]\
11 Apr 2024

**_Load Balance Loss and Router z-loss_ - OpenMoE: An Early Effort on Open Mixture-of-Experts Language Models**\
_Fuzhao Xue, Zian Zheng, Yao Fu, Jinjie Ni, Zangwei Zheng, Wangchunshu Zhou, Yang You_\
arXiv, [[Paper](https://arxiv.org/abs/2402.01739)]\
27 Mar 2024

**_Localized Balancing Constraint Loss_ - LoRAMoE: Alleviate World Knowledge Forgetting in Large Language Models via MoE-Style Plugin**\
_Shihan Dou, Enyu Zhou, Yan Liu, Songyang Gao, Jun Zhao, Wei Shen, Yuhao Zhou, Zhiheng Xi, Xiao Wang, Xiaoran Fan, Shiliang Pu, Jiang Zhu, Rui Zheng, Tao Gui, Qi Zhang, Xuanjing Huang_\
arXiv, [[Paper](https://arxiv.org/abs/2312.09979)]\
8 Mar 2024

**_Load Balance Loss and Contrastive Loss_ - MoELoRA: Contrastive Learning Guided Mixture of Experts on Parameter-Efficient Fine-Tuning for Large Language Models**\
_Tongxu Luo, Jiahe Lei, Fangyu Lei, Weihao Liu, Shizhu He, Jun Zhao, Kang Liu_\
arXiv, [[Paper](https://arxiv.org/abs/2402.12851)]\
20 Feb 2024

**_Load Balance Loss_ - SiRA: Sparse Mixture of Low Rank Adaptation**\
_Yun Zhu, Nevan Wichers, Chu-Cheng Lin, Xinyi Wang, Tianlong Chen, Lei Shu, Han Lu, Canoee Liu, Liangchen Luo, Jindong Chen, Lei Meng_\
arXiv, [[Paper]([15 Nov 2023](https://arxiv.org/abs/2311.09179))]\
15 Nov 2023

**_Top-1 Routing and Load Balance Loss_ & _Sparse-Gated Mixture of Experts in Transformer_ - Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity**\
_William Fedus, Barret Zoph, Noam Shazeer_\
JMLR, [[Paper](https://arxiv.org/abs/2101.03961)]\
16 Jun 2022

**_Top-2 Routing and Mean Gates Per Experts Loss_ - GShard: Scaling Giant Models with Conditional Computation and Automatic Sharding**\
_Dmitry Lepikhin, HyoukJoong Lee, Yuanzhong Xu, Dehao Chen, Orhan Firat, Yanping Huang, Maxim Krikun, Noam Shazeer, Zhifeng Chen_\
arXiv, [[arXiv](https://arxiv.org/abs/2006.16668)]\
30 Jun 2020

**_Top-k Routing and Importance/Load Balance Losses_ & _Sparse-Gated Mixture of Experts in LSTM_ - Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer**\
_Noam Shazeer, Azalia Mirhoseini, Krzysztof Maziarz, Andy Davis, Quoc Le, Geoffrey Hinton, Jeff Dean_\
ICLR 2017, [[Paper](https://arxiv.org/abs/1701.06538)]\
23 Jan 2017

#### z-loss
**_Load Balance Loss and Router z-loss_ - JetMoE: Reaching Llama2 Performance with 0.1M Dollars**\
_Yikang Shen, Zhen Guo, Tianle Cai, Zengyi Qin_\
arXiv, [[Paper](https://arxiv.org/abs/2404.07413)]\
11 Apr 2024

**_Load Balance Loss and Router z-loss_ - OpenMoE: An Early Effort on Open Mixture-of-Experts Language Models**\
_Fuzhao Xue, Zian Zheng, Yao Fu, Jinjie Ni, Zangwei Zheng, Wangchunshu Zhou, Yang You_\
arXiv, [[Paper](https://arxiv.org/abs/2402.01739)]\
27 Mar 2024

**_Router z-loss_ - ST-MoE: Designing Stable and Transferable Sparse Expert Models**\
_Barret Zoph, Irwan Bello, Sameer Kumar, Nan Du, Yanping Huang, Jeff Dean, Noam Shazeer, William Fedus_\
arXiv, [[Paper](https://arxiv.org/abs/2202.08906)]\
29 Apr 2022

### Mutual Information Loss
**_Mutual Information Loss and Mixture of Attention_ - Dense Training, Sparse Inference: Rethinking Training of Mixture-of-Experts Language Models**\
_Bowen Pan, Yikang Shen, Haokun Liu, Mayank Mishra, Gaoyuan Zhang, Aude Oliva, Colin Raffel, Rameswar Panda_\
arXiv, [[Paper](https://arxiv.org/abs/2404.05567)]\
8 Apr 2024

**_Mutual Information Loss_ - ModuleFormer: Modularity Emerges from Mixture-of-Experts**\
_Yikang Shen, Zheyu Zhang, Tianyou Cao, Shawn Tan, Zhenfang Chen, Chuang Gan_\
arXiv, [[Paper](https://arxiv.org/abs/2306.04640)]\
11 Sep 2023

**_Mutual Information Loss_ - Mod-Squad: Designing Mixture of Experts As Modular Multi-Task Learners**\
_Zitian Chen, Yikang Shen, Mingyu Ding, Zhenfang Chen, Hengshuang Zhao, Erik Learned-Miller, Chuang Gan_\
CVPR 2023, [[Paper](https://arxiv.org/abs/2212.08066)]\
15 Dec 2022

### Expert Capacity Limit
**Dynamic Mixture of Experts: An Auto-Tuning Approach for Efficient Transformer Models**\
_Yongxin Guo, Zhenglin Cheng, Xiaoying Tang, Tao Lin_\
arXiv, [[Paper](https://arxiv.org/abs/2405.14297)]\
23 May 2024

**_Expert capacity Threshold_ - GShard: Scaling Giant Models with Conditional Computation and Automatic Sharding**\
_Dmitry Lepikhin, HyoukJoong Lee, Yuanzhong Xu, Dehao Chen, Orhan Firat, Yanping Huang, Maxim Krikun, Noam Shazeer, Zhifeng Chen_\
arXiv, [[arXiv](https://arxiv.org/abs/2006.16668)]\
30 Jun 2020

### Non-trainable Gating Mechanism
#### Random Assignment
**_For Inference_ - Unchosen Experts Can Contribute Too: Unleashing MoE Models' Power by Self-Contrast**\
_Chufan Shi, Cheng Yang, Xinyu Zhu, Jiahao Wang, Taiqiang Wu, Siheng Li, Deng Cai, Yujiu Yang, Yu Meng_\
arXiv, [[Paper](https://arxiv.org/abs/2405.14507)]\
23 May 2024

**_Randomly Allocate 2 Experts_ - Taming Sparsely Activated Transformer with Stochastic Experts**\
_Simiao Zuo, Xiaodong Liu, Jian Jiao, Young Jin Kim, Hany Hassan, Ruofei Zhang, Tuo Zhao, Jianfeng Gao_\
ICLR 2022, [[Paper](https://arxiv.org/abs/2110.04260)]\
3 Feb 2022

**_Hash Routing_ - Hash Layers For Large Sparse Models**\
_Stephen Roller, Sainbayar Sukhbaatar, Arthur Szlam, Jason Weston_\
arXiv, [[Paper](https://arxiv.org/abs/2106.04426)]\
20 Jul 2021

#### Domain Mapping
**DEMix Layers: Disentangling Domains for Modular Language Modeling**\
_Suchin Gururangan, Mike Lewis, Ari Holtzman, Noah A. Smith, Luke Zettlemoyer_\
arXiv, [[Paper](https://arxiv.org/abs/2108.05036)]\
20 Aug 2021

### Expert-choice Gating
**_Expert Chooses Tokens_ - Mixture-of-Experts with Expert Choice Routing**\
_Yanqi Zhou, Tao Lei, Hanxiao Liu, Nan Du, Yanping Huang, Vincent Zhao, Andrew Dai, Zhifeng Chen, Quoc Le, James Laudon_\
NeurIPS 2022, [[Paper](https://arxiv.org/abs/2202.09368)]\
14 Oct 2022

### From Dense to Sparse
#### Sparse Upcycling 
**Sparse Upcycling: Training Mixture-of-Experts from Dense Checkpoints**\
_Aran Komatsuzaki, Joan Puigcerver, James Lee-Thorp, Carlos Riquelme Ruiz, Basil Mustafa, Joshua Ainslie, Yi Tay, Mostafa Dehghani, Neil Houlsby_\
ICLR 2023, [[Paper](https://arxiv.org/abs/2212.05055)]\
17 Feb 2023

#### Sparse Splitting
**_Neuron-Independent and Neuron-Sharing_ - LLaMA-MoE: Building Mixture-of-Experts from LLaMA with Continual Pre-training**\
_Tong Zhu, Xiaoye Qu, Daize Dong, Jiacheng Ruan, Jingqi Tong, Conghui He, Yu Cheng_\
arXiv, [[Paper](https://arxiv.org/abs/2406.16554)]\
24 Jun 2024

**_Evenly Splitting_ - Sparse MoE as the New Dropout: Scaling Dense and Self-Slimmable Transformers**\
_Tianlong Chen, Zhenyu Zhang, Ajay Jaiswal, Shiwei Liu, Zhangyang Wang_\
arXiv, [[Paper](https://arxiv.org/abs/2303.01610)]\
2 Mar 2023

**_Activation Diversity of Different Neurons_ - MoEfication: Transformer Feed-forward Layers are Mixtures of Experts**\
_Zhengyan Zhang, Yankai Lin, Zhiyuan Liu, Peng Li, Maosong Sun, Jie Zhou_\
ACL Findings 2022, [[Paper](https://arxiv.org/abs/2110.01786)]\
5 Apr 2022

## Dense Gating Mechanism
_**All the experts are activated.**_\
**_MoELoRA_ - MoELoRA: Contrastive Learning Guided Mixture of Experts on Parameter-Efficient Fine-Tuning for Large Language Models**\
_Tongxu Luo, Jiahe Lei, Fangyu Lei, Weihao Liu, Shizhu He, Jun Zhao, Kang Liu_\
arXiv, [[Paper](https://arxiv.org/abs/2402.12851)]\
20 Feb 2024

## Soft Gating Mechanism
_**Dense Gating Mechanism + Gating-weighted Merging of Input Tokens or Experts**_
### Token Merging
**From Sparse to Soft Mixtures of Experts**\
_Joan Puigcerver, Carlos Riquelme, Basil Mustafa, Neil Houlsby_\
ICLR 2024, [[Paper](https://arxiv.org/abs/2308.00951)]\
27 May 2024

### Expert Merging
**Soft Merging of Experts with Adaptive Routing**\
_Mohammed Muqeeth, Haokun Liu, Colin Raffel_\
TMLR, [[Paper](https://arxiv.org/abs/2306.03745)]\
13 May 2024

# Acknowledgement
This project is sponsored by the [PodGPT](https://podgpt.org/) group, Kolachalama Laboratory at Boston University.

<a href="https://podgpt.org/"> <img width="500" src="https://github.com/user-attachments/assets/84e28a61-d69b-47d3-a8db-d3605f4562e0"></a>
