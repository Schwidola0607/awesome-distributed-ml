# Awesome Distributed Machine Learning System

![Awesome](https://awesome.re/badge.svg)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/Schwidola0607/awesome-distributed-ml/pulls)

A curated list of awesome projects and papers for distributed training or inference **especially for large model**.

## Contents
- [Awesome Distributed Machine Learning System](#awesome-distributed-machine-learning-system)
  - [Contents](#contents)
  - [Open Source Projects](#open-source-projects)
  - [Papers](#papers)
    - [Survey](#survey)
    - [Pipeline Parallelism](#pipeline-parallelism)
    - [Sequence Parallelism](#sequence-parallelism)
    - [Mixture-of-Experts System](#mixture-of-experts-system)
    - [Graph Neural Networks System](#graph-neural-networks-system)
    - [Hybrid Parallelism & Framework](#hybrid-parallelism--framework)
    - [Memory Efficient Training](#memory-efficient-training)
    - [Tensor Movement](#tensor-movement)
    - [Auto Parallelization](#auto-parallelization)
    - [Communication Optimization](#communication-optimization)
    - [Fault-tolerant Training](#fault-tolerant-training)
    - [Inference and Serving](#inference-and-serving)
    - [Applications](#applications)
  - [Contribute](#contribute)

## Open Source Projects

- [Megatron-LM: Ongoing Research Training Transformer Models at Scale](https://github.com/NVIDIA/Megatron-LM)
- [DeepSpeed: A Deep Learning Optimization Library that Makes Distributed Training and Inference Easy, Efficient, and Effective.](https://www.deepspeed.ai/)
- [ColossalAI: A Unified Deep Learning System for Large-Scale Parallel Training](https://www.colossalai.org/)
- [OneFlow: A Performance-Centered and Open-Source Deep Learning Framework](www.oneflow.org)
- [Mesh TensorFlow: Model Parallelism Made Easier](https://github.com/tensorflow/mesh)
- [FlexFlow: A Distributed Deep Learning Framework that Supports Flexible Parallelization Strategies.](https://github.com/flexflow/FlexFlow)
- [Alpa: Auto Parallelization for Large-Scale Neural Networks](https://github.com/alpa-projects/alpa)
- [Easy Parallel Library: A General and Efficient Deep Learning Framework for Distributed Model Training](https://github.com/alibaba/EasyParallelLibrary)
- [FairScale: PyTorch Extensions for High Performance and Large Scale Training](https://github.com/facebookresearch/fairscale)
- [TePDist: an HLO-level automatic distributed system for DL models](https://github.com/alibaba/TePDist)
- [EasyDist: Automated Parallelization System and Infrastructure](https://github.com/alibaba/easydist)
- [Horovod: Distributed training framework](https://github.com/horovod/horovod)
- [Megatron-Deepspeed: Fork of Megatron with additional features](https://github.com/microsoft/Megatron-DeepSpeed)
- [VLLM: high-throughput and memory-efficient inference and serving engine](https://github.com/vllm-project/vllm)
- [TGI: Large Language Model Text Generation Inference](https://github.com/huggingface/text-generation-inference)
- [JetStream: throughput and memory optimized engine for LLM inference on XLA devices](https://github.com/google/JetStream)
## Papers

### Survey

- [Demystifying Parallel and Distributed Deep Learning: An In-Depth Concurrency Analysis](https://arxiv.org/abs/1802.09941) by Tal Ben-Nun et al., ACM Computing Surveys 2020
- [A Survey on Auto-Parallelism of Neural Networks Training](https://www.techrxiv.org/articles/preprint/A_Survey_on_Auto-Parallelism_of_Neural_Networks_Training/19522414) by Peng Liang., techrxiv 2022
- [Communication-Efficient Data Parallel Distributed Deep Learning: A Comprehensive Survey](https://arxiv.org/pdf/2003.06307.pdf) by Zhengheng Tang et al., CoRR 2020

### General Scaling

- [Scaling Laws for Neural Language Models](https://arxiv.org/pdf/2001.08361.pdf) by Jared Kaplan et al. arxiv 2020
- [Training Compute-Optimal Large Language Models](https://arxiv.org/pdf/2203.15556.pdf) by Jordan Hoffmann et al., arxiv 2022
- [Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity](https://arxiv.org/pdf/2101.03961.pdf) by William Fedus et al., JMLR 2022
- [Chinchilla Scaling: A replication attempt](https://arxiv.org/pdf/2404.10102.pdf) by Tamay Besiroglu et al. arxiv 2024

### Pipeline Parallelism

- [GPipe: Efficient Training of Giant Neural Networks using Pipeline Parallelism](https://proceedings.neurips.cc/paper/2019/file/093f65e080a295f8076b1c5722a46aa2-Paper.pdf) by Yanping Huang et al., NeurIPS 2019
- [PipeDream: generalized pipeline parallelism for DNN training](https://dl.acm.org/doi/10.1145/3341301.3359646) by Deepak Narayanan et al., SOSP 2019
- [Memory-Efficient Pipeline-Parallel DNN Training](https://arxiv.org/abs/2006.09503v3) by Deepak Narayanan et al., ICML 2021
- [DAPPLE: a pipelined data parallel approach for training large models](https://dl.acm.org/doi/10.1145/3437801.3441593) by Shiqing Fan et al. PPoPP 2021
- [Chimera: efficiently training large-scale neural networks with bidirectional pipelines](https://dl.acm.org/doi/abs/10.1145/3458817.3476145) by Shigang Li et al., SC 2021
- [Elastic Averaging for Efficient Pipelined DNN Training](https://dl.acm.org/doi/abs/10.1145/3572848.3577484) by Zihao Chen et al. PPoPP 2023
- [Mobius: Fine Tuning Large-Scale Models on Commodity GPU Servers](https://dl.acm.org/doi/abs/10.1145/3575693.3575703) by Yangyang Feng et al. ASPLOS 2023
- [Hanayo: Harnessing Wave-like Pipeline Parallelism for Enhanced Large Model Training Efficiency](https://dl.acm.org/doi/10.1145/3581784.3607073) by Ziming Liu et al. SC 2023
- [SDPipe: A Semi-Decentralized Framework for Heterogeneity-Aware Pipeline-parallel Training](https://www.vldb.org/pvldb/vol16/p2354-miao.pdf) by Xupeng Miao et al. VLDB 2023
- [XPipe: Efficient Pipeline Model Parallelism for Multi-GPU DNN Training](http://arxiv.org/abs/1911.04610) by Lei Guan et al.
- [TeraPipe: Token-Level Pipeline Parallelism for Training Large-Scale Language Models](https://arxiv.org/pdf/2102.07988.pdf) by Zhuohan Li et al., ICML 2021
- [Zero Bubble Pipeline Parallelism](https://arxiv.org/pdf/2401.10241) by Penghui Qi et al., ICLR 2024

### Sequence Parallelism

- [Long Sequence Training from System Perspective](https://aclanthology.org/2023.acl-long.134/) by Shenggui Li et al., ACL 2023
- [DeepSpeed Ulysses: System Optimizations for Enabling Training of Extreme Long Sequence Transformer Models](https://arxiv.org/abs/2309.14509) by Sam Ade Jacobs et al., arxiv 2023
- [Blockwise Parallel Transformer for Large Context Windows](https://arxiv.org/pdf/2305.19370.pdf) by Hao Liu et al., NeurIPS 2023 Spotlight
- [Ring Attention with Blockwise Transformers for Near-Infinite Context](https://arxiv.org/abs/2310.01889) by Hao Liu et al., NeurIPS 2023 Workshop

### Data Parallelism 

### Mixture-of-Experts System

- [GShard: Scaling Giant Models with Conditional Computation and Automatic Sharding](https://openreview.net/forum?id=qrwe7XHTmYb) by Dmitry Lepikhin et al., ICLR 2021
- [FasterMoE: modeling and optimizing training of large-scale dynamic pre-trained models](https://dl.acm.org/doi/abs/10.1145/3503221.3508418) by Jiaao He et al., PPoPP 2022
- [BaGuaLu: targeting brain scale pretrained models with over 37 million cores](https://dl.acm.org/doi/abs/10.1145/3503221.3508417) by Zixuan Ma et al., PPoPP 2022
- [DeepSpeed-MoE: Advancing Mixture-of-Experts Inference and Training to Power Next-Generation AI Scale](https://arxiv.org/abs/2201.05596) by Samyam Rajbhandari et al., ICML 2022
- [Tutel: Adaptive Mixture-of-Experts at Scale](https://arxiv.org/abs/2206.03382) by Changho Hwang et al., MLSys 2023
- [Accelerating Distributed MoE Training and Inference with Lina](https://arxiv.org/abs/2210.17223) by Jiamin Li et al., ATC 2023
- [SmartMoE: Efficiently Training Sparsely-Activated Models through Combining Static and Dynamic Parallelization](https://www.usenix.org/conference/atc23/presentation/zhai) by Mingshu Zhai et al., ATC 2023
- [MegaBlocks: Efficient Sparse Training with Mixture-of-Experts](https://proceedings.mlsys.org/paper_files/paper/2023/hash/f9f4f0db4894f77240a95bde9df818e0-Abstract-mlsys2023.html) by Trevor Gale et al., MLSys 2023
### Graph Neural Networks System

- [PiPAD: Pipelined and Parallel Dynamic GNN Training on GPUs](https://dl.acm.org/doi/10.1145/3572848.3577487) Chunyang Wang et al., PPoPP 2023
- [DSP: Efficient GNN Training with Multiple GPUs](https://dl.acm.org/doi/10.1145/3572848.3577528) Zhenkun Cai et al., PPoPP 2023
- [Accelerating Graph Neural Networks with Fine-grained intra-kernel Communication-Computation Pipelining on Multi-GPU Platforms](https://arxiv.org/abs/2209.06800) Yuke Wang et al., OSDI 2023
### Hybrid Parallelism & Framework

- [GSPMD: General and Scalable Parallelization for ML Computation Graphs](https://arxiv.org/abs/2105.04663) by Yuanzhong Xu et al., arxiv 2021
- [Efficient large-scale language model training on GPU clusters using megatron-LM](https://dl.acm.org/doi/10.1145/3458817.3476209) by Deepak Narayanan et al., SC 2021
- [GEMS: GPU-Enabled Memory-Aware Model-Parallelism System for Distributed DNN Training](https://ieeexplore.ieee.org/document/9355254) by Arpan Jain et al., SC 2020
- [Amazon SageMaker Model Parallelism: A General and Flexible Framework for Large Model Training](https://arxiv.org/abs/2111.05972) by Can Karakus et al., arxiv 2021
- [OneFlow: Redesign the Distributed Deep Learning Framework from Scratch](https://arxiv.org/abs/2110.15032) by Jinhui Yuan et al., arxiv 2021
- [Colossal-AI: A Unified Deep Learning System For Large-Scale Parallel Training](https://arxiv.org/abs/2110.14883) by Zhengda Bian., arxiv 2021
- [PyTorch FSDP: Experiences on Scaling Fully Sharded Data Parallel](https://arxiv.org/pdf/2304.11277.pdf) by Pytorch, arxiv
- [Litz: Elastic Framework for High-Performance Distributed Machine Learning](https://www.usenix.org/system/files/conference/atc18/atc18-qiao.pdf) by Aurick Qiao et al. ATC 2018
- [Beyond Data and Model Parallelism for Deep Neural Networks](https://arxiv.org/pdf/1807.05358.pdf) by Zhihao Jia et al., SysML 2019
- [TASO: Optimizing Deep Learning Computation with Automatic Generation of Graph Substitutions](https://dl.acm.org/doi/pdf/10.1145/3341301.3359630) by Zhihao Jia et al., SOSP 2019

### Memory Efficient Training

- [Mixed Precision Training](https://arxiv.org/pdf/1710.03740.pdf) by Sharan Narang et al., ICLR 2018
- [Training deep nets with sublinear memory cost](https://arxiv.org/abs/1604.06174) by Tianqi Chen et al., arxiv 2016
- [Gist: Efficient Data Encoding for Deep Neural Network Training](https://www.microsoft.com/en-us/research/uploads/prod/2018/04/fiddle-gist-isca18.pdf) by Animesh Jain et al., ISCA 2018
- [ZeRO: memory optimizations toward training trillion parameter models](https://dl.acm.org/doi/10.5555/3433701.3433727) by Samyam Rajbhandari et al., SC 2020
- [Checkmate: Breaking the Memory Wall with Optimal Tensor Rematerialization](https://proceedings.mlsys.org/paper/2020/hash/084b6fbb10729ed4da8c3d3f5a3ae7c9-Abstract.html) by Paras Jain et al., MLSys 2020
- [Dynamic Tensor Rematerialization](https://arxiv.org/abs/2006.09616) by Marisa Kirisame et al., ICLR 2021
- [ActNN: Reducing Training Memory Footprint via 2-Bit Activation Compressed Training](https://proceedings.mlr.press/v139/chen21z.html) by Jianfei Chen et al., ICML 2021
- [GACT: Activation Compressed Training for Generic Network Architectures](https://proceedings.mlr.press/v162/liu22v.html) by Xiaoxuan Liu et al., ICML 2022
- [Reducing Activation Recomputation in Large Transformer Models](https://arxiv.org/pdf/2205.05198.pdf) by Vijay Korthikanti et al., MLSys 2023
- [Training Deep Nets with Sublinear Memory Cost](https://arxiv.org/pdf/1604.06174.pdf) by Tianqi Chen et al., arxiv 2016
- [FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](https://arxiv.org/pdf/2205.14135.pdf) by Tri Dao et al., NeurIPS 2022
- [FlashAttention-2: Faster Attention with Better Parallelism and Work Partitioning](https://arxiv.org/pdf/2307.08691.pdf) by Tri Dao, ICLR 2024

### Tensor Movement

- [Superneurons: dynamic GPU memory management for training deep neural networks](https://dl.acm.org/doi/10.1145/3200691.3178491) by Linnan Wang et al., PPoPP 2018
- [Capuchin: Tensor-based GPU Memory Management for Deep Learning](https://dl.acm.org/doi/10.1145/3373376.3378505) by Xuan Peng et al., ASPLOS 2020
- [SwapAdvisor: Pushing Deep Learning Beyond the GPU Memory Limit via Smart Swapping](https://dl.acm.org/doi/10.1145/3373376.3378530) by Chien-Chin Huang et al., ASPLOS 2020
- [ZeRO-Offload: Democratizing Billion-Scale Model Training](https://www.usenix.org/conference/atc21/presentation/ren-jie) by Jie Ren et al., ATC 2021
- [ZeRO-infinity: breaking the GPU memory wall for extreme scale deep learning](https://dl.acm.org/doi/abs/10.1145/3458817.3476205) by Samyam Rajbhandari et al., SC 2021
- [PatrickStar: Parallel Training of Pre-trained Models via Chunk-based Memory Management](https://ieeexplore.ieee.org/abstract/document/9940581) by Jiarui Fang et al., TPDS 2023
- [MegTaiChi: dynamic tensor-based memory management optimization for DNN training](https://dl.acm.org/doi/10.1145/3524059.3532394) by Zhongzhe Hu et al., ICS 2022
- [Tensor Movement Orchestration In Multi-GPU Training Systems](https://www.computer.org/csdl/proceedings-article/hpca/2023/10071043/1LMbAKcbFKg) Shao-Fu Lin et al., HPCA 2023

### Auto Parallelization

- [Mesh-tensorflow: Deep learning for supercomputers](https://proceedings.neurips.cc/paper/2018/hash/3a37abdeefe1dab1b30f7c5c7e581b93-Abstract.html) by Noam Shazeer et al., NeurIPS 2018
- [Exploring Hidden Dimensions in Parallelizing Convolutional Neural Networks](https://arxiv.org/abs/1802.04924) by Zhihao Jia et al., ICML 2018
- [Beyond Data and Model Parallelism for Deep Neural Networks](https://proceedings.mlsys.org/paper/2019/hash/c74d97b01eae257e44aa9d5bade97baf-Abstract.html) by Zhihao Jia et al., MLSys 2019
- [Supporting Very Large Models using Automatic Dataflow Graph Partitioning](https://dl.acm.org/doi/abs/10.1145/3302424.3303953) by Minjie Wang et al., EuroSys 2019
- [Alpa: Automating Inter- and Intra-Operator Parallelism for Distributed Deep Learning](https://arxiv.org/abs/2201.12023) by Lianmin Zheng et al., OSDI 2022
- [Unity: Accelerating DNN Training Through Joint Optimization of Algebraic Transformations and Parallelization](https://www.usenix.org/conference/osdi22/presentation/unger) by Colin Unger, Zhihao Jia, et al., OSDI 2022
- [Galvatron: Efficient Transformer Training over Multiple GPUs Using Automatic Parallelism](https://arxiv.org/abs/2211.13878) by Xupeng Miao, et al., VLDB 2023
- [Auto-Parallelizing Large Models with Rhino: A Systematic Approach on Production AI Platform](https://arxiv.org/abs/2302.08141) by Shiwei Zhang, Lansong Diao, et al., arxiv 2023

### Communication Optimization

- [Blink: Fast and Generic Collectives for Distributed ML](https://proceedings.mlsys.org/paper/2020/hash/43ec517d68b6edd3015b3edc9a11367b-Abstract.html) by Guanhua Wang et al., MLSys 2020
- [Synthesizing optimal collective algorithms](https://dl.acm.org/doi/10.1145/3437801.3441620) by Zixian Cai et al., PPoPP 2021
- [Breaking the computation and communication abstraction barrier in distributed machine learning workloads](https://dl.acm.org/doi/10.1145/3503222.3507778) by Abhinav Jangda et al., ASPLOS 2022
- [MSCCLang: Microsoft Collective Communication Language](https://dl.acm.org/doi/abs/10.1145/3575693.3575724) by Meghan Cowan et al., ASPLOS 2023
- [Overlap Communication with Dependent Computation via Decomposition in Large Deep Learning Models](https://dl.acm.org/doi/abs/10.1145/3567955.3567959) by Shibo Wang et al., ASPLOS 2023
- [Logical/Physical Topology-Aware Collective Communication in Deep Learning Training](https://www.computer.org/csdl/proceedings-article/hpca/2023/10071117/1LMbHmoPq0M) Jo Sanghoon et al., HPCA 2023

### Fault-tolerant Training
- [Oobleck: Resilient Distributed Training of Large Models Using Pipeline Templates](https://dl.acm.org/doi/abs/10.1145/3600006.3613152) by Insu Jang et al., SOSP 2023
- [Bamboo: Making Preemptible Instances Resilient for Affordable Training of Large DNNs](https://www.usenix.org/conference/nsdi23/presentation/thorpe) by John Thorpe et al., NSDI 2023
- [Varuna: scalable, low-cost training of massive deep learning models](https://dl.acm.org/doi/abs/10.1145/3492321.3519584) by Sanjith Athlur et al., EuroSys 2022
- [Decentralized Training of Foundation Models in Heterogeneous Environments](https://arxiv.org/pdf/2206.01288.pdf) by Binhuang Yuan et al., NeurIPS 2022
- [GEMINI: Fast Failure Recovery in Distributed Training with In-Memory Checkpoints](https://assets.amazon.science/29/31/6523473f48e4af52252bac56ef51/gemini-fast-failure-recovery-in-distributed-training-with-in-memory-checkpoints.pdf) by Zhuang Wang et al., SOSP 2023

### Sparsity and Quantization
- [Hogwild!: A Lock-Free Approach to Parallelizing Stochastic Gradient Descent](https://arxiv.org/pdf/1106.5730.pdf) by Feng Niu et al., NeurIPS 2011
- [Sparse Communication for Distributed Gradient Descent](https://arxiv.org/pdf/1704.05021.pdf) by Alham Aji et al., EMNLP 2017
- [Efficient Sparse Collective Communication and its application to Accelerate Distributed Deep Learning](https://dl.acm.org/doi/pdf/10.1145/3452296.3472904) by Jiawei Fei et al., KAUST 2020
- [Natural Compression for Distributed Deep Learning](https://arxiv.org/pdf/1905.10988.pdf) by Samuel Horvath et al., MLR 2022
- [Deep Gradient Compression: Reducing the Communication Bandwidth for Distributed Training](https://arxiv.org/pdf/1712.01887.pdf) by Yujun Lin et al., ICLR 2018
- [SlowMo: Improving Communication-Efficient Distributed SGD with Slow Momentum](https://arxiv.org/pdf/1910.00643) by Jianyu Wang et al., ICLR 2020
- [Stochastic Gradient Push for Distributed Deep Learning](https://arxiv.org/pdf/1811.10792) by Mahmoud Assran et al., ICML 2019

### Inference and Serving
- [DeepSpeed Inference: Enabling Efficient Inference of Transformer Models at Unprecedented Scale](https://dl.acm.org/doi/abs/10.5555/3571885.3571946) by Reza Yazdani Aminabadi et al., SC 2022
- [EnergonAI: An Inference System for 10-100 Billion Parameter Transformer Models](https://arxiv.org/abs/2209.02341) by Jiangsu Du et al., arxiv 2022
- [Efficiently Scaling Transformer Inference](https://arxiv.org/abs/2211.05102) by Reiner Pope et al., MLSys 2022
- [Beta: Statistical Multiplexing with Model Parallelism for Deep Learning Serving](https://arxiv.org/abs/2302.11665) by Zhuohan Li et al., OSDI 2023
- [Fast inference from transformers via speculative decoding](https://arxiv.org/abs/2211.17192) by Yaniv Leviathan et al., ICML 2023
- [FlexGen: High-throughput Generative Inference of Large Language Models with a Single GPU](https://arxiv.org/abs/2303.06865) by Ying Sheng et al., ICML 2023
- [Liger: Interleaving Intra- and Inter-Operator Parallelism for Distributed Large Model Inference](https://dl.acm.org/doi/abs/10.1145/3627535.3638466) by Jiangsu Du et al., PPoPP 2024

### Compute Sharing and Scheduling
- [Orion: Interference-aware, Fine-grained GPU Sharing for ML Applications](https://anakli.inf.ethz.ch/papers/orion_eurosys24.pdf) by Foteini Strati et al., EuroSys 2024
- [Singularity: Planet-Scale, Preemptive and Elastic Scheduling of AI Workloads](https://arxiv.org/pdf/2202.07848.pdf) by Dharma Shukla et al., arxiv 2022
- [Pollux: Co-adaptive Cluster Scheduling for Goodput-Optimized Deep Learning](https://www.usenix.org/system/files/osdi21-qiao.pdf) by Aurick Qiao et al., OSDI 2021
- [Sia: Heterogeneity-aware, goodput-optimized ML-cluster scheduling](https://dl.acm.org/doi/pdf/10.1145/3600006.3613175) by Suhas Jayaram Subramanya et al., SOSP 2023

### Applications

- [NASPipe: High Performance and Reproducible Pipeline Parallel Supernet Training via Causal Synchronous Parallelism](https://dl.acm.org/doi/abs/10.1145/3503222.3507735) by Shixiong Zhao et al., ASPLOS 2022
- [AthenaRL: Distributed Reinforcement Learning with Dataflow Fragments](https://arxiv.org/abs/2210.00882) by Huanzhou Zhu et al., ATC 2023 
- [Hydro: Surrogate-Based Hyperparameter Tuning Service in the Datacenter](https://www.usenix.org/conference/osdi23/presentation/hu-qinghao) by Qinghao Hu et al., OSDI 2023
- [FastFold: Optimizing AlphaFold Training and Inference on GPU Clusters](https://dl.acm.org/doi/10.1145/3627535.3638465) by Shenggan Cheng et al., PPoPP 2024

## Contribute

All contributions to this repository are welcome. Open an [issue](https://github.com/Schwidola0607/awesome-distributed-ml/issues) or send a [pull request](https://github.com/Schwidola0607/awesome-distributed-ml/pulls).
