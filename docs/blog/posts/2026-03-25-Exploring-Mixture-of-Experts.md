---
title: 'AI Wednesday 06 : Exploring Mixture-of-Experts (MoE)'
date: 2026-03-25
authors: [sebin]
slug: ai-wednesday-06
description: >
  A session on how Mixture-of-Experts architectures work, DeepSeek's implementation, and related approaches like Chain of Experts and Gemma's effective parameters.
---

## Overview

This week's AI Wednesday focused on Mixture-of-Experts (MoE) — a sparse architecture that scales model capacity without proportionally scaling compute. We explored how routing and expert specialization work, looked at DeepSeek's MoE design, and compared it with other recent approaches including Chain of Experts and how Gemma models report effective parameters.

## Topics

* How MoE architectures route tokens to specialized expert networks
* DeepSeekMoE: fine-grained expert segmentation and shared expert isolation
* Chain of Experts — sequential communication between experts within a layer
* Gemma and the idea of effective vs. total parameters in sparse models
* Why MoE matters for building large models at lower inference cost

## Resources

* [DeepSeekMoE: Towards Ultimate Expert Specialization in Mixture-of-Experts Language Models](https://arxiv.org/abs/2401.06066)
* [Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity](https://arxiv.org/abs/2101.03961)
* [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://arxiv.org/abs/1701.06538)
* [Chain-of-Experts: Unlocking the Communication Power of Mixture-of-Experts Models](https://arxiv.org/abs/2506.18945)

## Highlights

* MoE lets models carry far more parameters than are active per token — understanding routing and expert specialization is key to reading modern LLM architecture papers.

## Next Week

- Topic: TITANS — Mamba, Titans, and the MIRAS Framework
- Host: [Sebin Thomas](https://tinkerhub.org/@sebin)
