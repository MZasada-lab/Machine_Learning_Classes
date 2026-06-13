# SoftMoE: Soft Differentiable Routing for Mixture-of-Experts in LLMs

This repository contains the paper:

**SoftMoE: Soft Differentiable Routing for Mixture-of-Experts in LLMs**  
Mikołaj Zasada, Łukasz Struski, Jacek Tabor, Marcin Kurdziel  
Accepted at the **Forty-third International Conference on Machine Learning (ICML 2026)**.

[Read the paper](./SoftMoE.pdf) | [OpenReview](https://openreview.net/forum?id=vGTFOp3jLO) | [Source code](https://github.com/dlcuda/SoftMoE)

> Note: Until the conference date on 4 July 2026, OpenReview link, may not be publicly accessible.

## Overview

Sparse Mixture-of-Experts models scale language model capacity while keeping per-token inference cost low, but standard hard top-k routing is non-differentiable and fixes the number of active experts in advance.

SoftMoE replaces discrete routing with a differentiable soft top-k relaxation based on LapSum. The method allows expert routing to be optimized with gradients and introduces a globally constrained learnable expert budget, so the model can adapt how many experts are used across layers. In experiments on language modeling and downstream tasks, SoftMoE matches or improves sparse MoE performance while activating fewer experts on average.

## Paper

The PDF is available in this repository:

- [SoftMoE.pdf](./SoftMoE.pdf)