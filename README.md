<h1 align="center">
  <img src="assets/title-icon.png" width="52" align="absmiddle" style="vertical-align: -0.2em;" alt="Project icon">
  Vision-Language-Action Models for Diverse Application Scenarios: A Survey of Input Modalities
</h1>

<p align="center">
  <strong>A companion repository for a survey on input modalities in Vision-Language-Action models.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/arXiv-coming%20soon-b31b1b.svg?logo=arxiv" alt="arXiv coming soon">
  <a href="https://mpil-lab.github.io/lab-webpage/index.html"><img src="https://img.shields.io/badge/Lab-MPIL--Lab-blue.svg" alt="Lab: MPIL Lab"></a>
  <img src="https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-coming%20soon-FFD21E" alt="Hugging Face coming soon">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-CC%20BY%204.0-black.svg" alt="License: CC BY 4.0"></a>
</p>

🔥 This repository accompanies our survey on input modalities for Vision-Language-Action (VLA) models. We are currently organizing the full paper list, taxonomy, and supplementary resources.

- We maintain a curated resource list for VLA input modalities across embodied agents, robotic manipulation, navigation, and related physical decision-making tasks.
- The repository follows the paper structure: vision-language modalities, VLAs with a single additional modality, and VLAs with multiple additional modalities.
- If you find missing papers, incorrect metadata, broken links, or taxonomy issues, please open an issue or submit a pull request.

## Table of Contents

- [🤖 Overview](#overview)
- [🔍 Input Modalities in VLAs](#input-modalities-in-vlas)
- [ Vision-Language Modalities in VLAs](#vision-language-modalities-in-vlas)
  - [Language Modality](#language-modality)
  - [Vision Modality](#vision-modality)
  - [Vision-Language to Action Modeling](#vision-language-to-action-modeling)
- [ VLAs with Single Additional Modality](#vlas-with-single-additional-modality)
  - [Depth Modality](#depth-modality)
  - [Point Cloud Modality](#point-cloud-modality)
  - [Tactile Modality](#tactile-modality)
  - [Force Modality](#force-modality)
  - [Audio Modality](#audio-modality)
  - [Gaze Modality](#gaze-modality)
  - [Other Emerging Modalities](#other-emerging-modalities)
- [ VLAs with Multiple Additional Modalities](#vlas-with-multiple-additional-modalities)
  - [Depth and Point Cloud Modalities (3D Geometry)](#depth-and-point-cloud-modalities-3d-geometry)
  - [Tactile and Force Modalities](#tactile-and-force-modalities)
  - [Other Multiple Additional Modalities](#other-multiple-additional-modalities)
- [🤝 Acknowledgements](#acknowledgements)
- [📖 Citation](#citation)
- [📄 License](#license)

## Overview

Vision-Language-Action models increasingly rely on diverse input signals beyond standard RGB observations. This survey studies how different modalities contribute to perception, grounding, planning, control, and human-agent interaction in VLA systems.


## Input Modalities in VLAs

| Modality | Representative VLA Application Scenarios | Task-Relevant Information |
| --- | --- | --- |
| 🖼️ RGB Image | General object-centric manipulation and scene understanding | Object appearance, scene context, and visual state observations |
| 🎞️ Video | Long-horizon, dynamic, or temporally dependent manipulation | Motion history, temporal context, and action-relevant dynamics |
| 💬 Language | Instruction-conditioned manipulation and goal specification | Task goals, constraints, and semantic instructions |
| 📏 Depth | Precision manipulation, obstacle avoidance, and spatial alignment | Metric distance, depth ordering, and image-aligned spatial structure |
| ☁️ Point Cloud | Complex 3D manipulation and pose-aware interaction | 3D geometry, object shape, and point-level spatial structure |
| ✋ Tactile | Contact-rich manipulation, insertion, grasping, and slip handling | Local contact state, deformation, and tactile feedback |
| 🧲 Force | Force-aware contact manipulation and compliant control | Interaction force, torque, and contact intensity |
| 🔊 Audio | Sound-producing manipulation and interactive tasks | Contact sounds, speech cues, and intent-related acoustic signals |
| ⚡ Event Stream | Low-light, high-speed, or motion-blurred manipulation | Asynchronous motion cues and brightness-change events |
| 🌡️ Thermal Image | Low-light, reflective, or temperature-sensitive operation | Heat distribution, material state, and non-visible environmental cues |
| 👁️ Gaze | Ambiguous or human-in-the-loop interaction | Human attention, target preference, and intent cues |
| 🧠 Brain Signal | Assistive control and human-guided intervention | Neural intention signals and intervention commands |
| 📡 Radar | Occluded-object or hidden-state manipulation | Radar reflections, through-occlusion cues, and hidden-object responses |

## Vision-Language Modalities in VLAs

This section covers VLA methods that keep the standard vision-language input interface while focusing on how the two modalities are specified, represented, fused, and converted into actions.

### Language Modality

> These works use the canonical vision-language input interface and focus on how language specifies tasks, goals, reasoning contexts, and instruction variants for VLA policies.

- **LIBERO-Para** - *LIBERO-Para: A Diagnostic Benchmark and Metrics for Paraphrase Robustness in VLA Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.28301-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.28301)

- **IGAR** - *Restoring Linguistic Grounding in VLA Models via Train-Free Attention Recalibration*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.06001-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.06001)

- **LangGap** - *LangGap: Diagnosing and Closing the Language Gap in Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.00592-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.00592)

- **CAG** - *When Vision Overrides Language: Evaluating and Mitigating Counterfactual Failures in VLAs*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.17659-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.17659) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://vla-va.github.io/)

- **LangForce** - *LangForce: Bayesian Decomposition of Vision Language Action Models via Latent Action Queries*  
  [![arXiv](https://img.shields.io/badge/arXiv-2601.15197-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2601.15197)

- **RSS** - *Stable Language Guidance for Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2601.04052-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2601.04052)

- **BayesVLA** - *Seeing to Act, Prompting to Specify: A Bayesian Factorization of Vision Language Action Policy*  
  [![arXiv](https://img.shields.io/badge/arXiv-2512.11218-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2512.11218) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://xukechun.github.io/papers/BayesVLA)

- **MG-Select** - *Verifier-free Test-Time Sampling for Vision Language Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.05681-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.05681)

- **VLA-Reasoner** - *VLA-Reasoner: Empowering Vision-Language-Action Models with Reasoning via Online Monte Carlo Tree Search*  
  [![arXiv](https://img.shields.io/badge/arXiv-2509.22643-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2509.22643) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://vla-reasoner.github.io/)

- **RICL** - *RICL: Adding In-Context Adaptability to Pre-Trained Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2508.02062-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2508.02062) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://ricl-vla.github.io)

- **InstructVLA** - *InstructVLA: Vision-Language-Action Instruction Tuning from Understanding to Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2507.17520-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2507.17520)

- **RoboMonkey** - *RoboMonkey: Scaling Test-Time Sampling and Verification for Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2506.17811-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2506.17811)

- **FSD** - *From Seeing to Doing: Bridging Reasoning and Decision for Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2505.08548-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2505.08548) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://embodied-fsd.github.io/)

- **CoA-VLA** - *CoA-VLA: Improving Vision-Language-Action Models via Visual-Textual Chain-of-Affordance*  
  [![arXiv](https://img.shields.io/badge/arXiv-2412.20451-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2412.20451) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://chain-of-affordance.github.io)

- **ECoT** - *Robotic Control via Embodied Chain-of-Thought Reasoning*  
  [![arXiv](https://img.shields.io/badge/arXiv-2407.08693-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2407.08693) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://embodied-cot.github.io)

- **RT-2** - *RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control*  
  [![arXiv](https://img.shields.io/badge/arXiv-2307.15818-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2307.15818) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://robotics-transformer.github.io/)

- **PaLM-E** - *PaLM-E: An Embodied Multimodal Language Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2303.03378-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2303.03378) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://palm-e.github.io/)

- **SayCan** - *Do As I Can, Not As I Say: Grounding Language in Robotic Affordances*  
  [![arXiv](https://img.shields.io/badge/arXiv-2204.01691-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2204.01691) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://say-can.github.io/)


### Vision Modality

> These works also remain within the vision-language input setting, but focus on the visual side: viewpoints, temporal context, object-centric cues, pixel-level grounding, and visual prompting.

- **Sentinel-VLA** - *Sentinel-VLA: A Metacognitive VLA Model with Active Status Monitoring for Dynamic Reasoning and Error Recovery*  
  [![arXiv](https://img.shields.io/badge/arXiv-2605.01191-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2605.01191)

- **VP-VLA** - *VP-VLA: Visual Prompting as an Interface for Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.22003-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.22003) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://visualprompt-vla.github.io/)

- **ReMem-VLA** - *ReMem-VLA: Empowering Vision-Language-Action Model with Memory via Dual-Level Recurrent Queries*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.12942-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.12942)

- **AnyCamVLA** - *AnyCamVLA: Zero-Shot Camera Adaptation for Viewpoint Robust Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.05868-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.05868) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://heo0224.github.io/AnyCamVLA/)

- **JALA** - *Joint-Aligned Latent Action: Towards Scalable VLA Pretraining in the Wild*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.21736-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.21736)

- **BFA++** - *BFA++: Hierarchical Best-Feature-Aware Token Prune for Multi-View Vision Language Action Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.20566-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.20566)

- **Selective Perception** - *Selective Perception for Robot: Task-Aware Attention in Multimodal VLA*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.15543-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.15543)

- **Dream4manip** - *Say, Dream, and Act: Learning Video World Models for Instruction-Driven Robot Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.10717-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.10717)

- **DySta** - *Efficient Long-Horizon Vision-Language-Action Models via Static-Dynamic Disentanglement*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.03983-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.03983)

- **MVP-LAM** - *MVP-LAM: Learning Action-Centric Latent Action via Cross-Viewpoint Reconstruction*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.03668-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.03668)

- **Point-VLA** - *Point What You Mean: Visually Grounded Instruction Policy*  
  [![arXiv](https://img.shields.io/badge/arXiv-2512.18933-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2512.18933)

- **VideoVLA** - *VideoVLA: Video Generators Can Be Generalizable Robot Manipulators*  
  [![arXiv](https://img.shields.io/badge/arXiv-2512.06963-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2512.06963) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://videovla-nips2025.github.io)

- **PixelVLA** - *PixelVLA: Advancing Pixel-level Understanding in Vision-Language-Action Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2511.01571-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2511.01571)

- **ContextVLA** - *ContextVLA: Vision-Language-Action Model with Amortized Multi-Frame Context*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.04246-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.04246) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://huiwon-jang.github.io/contextvla)

- **RS-CL** - *Contrastive Representation Regularization for Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.01711-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.01711)

- **HAMLET** - *HAMLET: Switch your Vision-Language-Action Model into a History-Aware Policy*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.00695-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.00695) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://myungkyukoo.github.io/hamlet/)

- **VLA-LPAF** - *VLA-LPAF: Lightweight Perspective-Adaptive Fusion for Vision-Language-Action to Enable More Unconstrained Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2509.18183-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2509.18183)

- **FlowVLA** - *FlowVLA: Visual Chain of Thought-based Motion Reasoning for Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2508.18269-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2508.18269) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://irpn-lab.github.io/FlowVLA/)

- **OC-VLA** - *Grounding Actions in Camera Space: Observation-Centric Vision-Language-Action Policy*  
  [![arXiv](https://img.shields.io/badge/arXiv-2508.13103-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2508.13103)

- **ReconVLA** - *ReconVLA: Reconstructive Vision-Language-Action Model as Effective Robot Perceiver*  
  [![arXiv](https://img.shields.io/badge/arXiv-2508.10333-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2508.10333) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://zionchow.github.io/ReconVLA/)

- **EgoVLA** - *EgoVLA: Learning Vision-Language-Action Models from Egocentric Human Videos*  
  [![arXiv](https://img.shields.io/badge/arXiv-2507.12440-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2507.12440) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://rchalyang.github.io/EgoVLA)

- **CrayonRobo** - *CrayonRobo: Object-Centric Prompt-Driven Vision-Language-Action Model for Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2505.02166-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2505.02166)

- **UP-VLA** - *UP-VLA: A Unified Understanding and Prediction Model for Embodied Agent*  
  [![arXiv](https://img.shields.io/badge/arXiv-2501.18867-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2501.18867)

- **EF-VLA** - *Early Fusion Helps Vision Language Action Models Generalize Better*  
  [![OpenReview](https://img.shields.io/badge/OpenReview-yj1yHnLxEg-8c1b13.svg)](https://openreview.net/forum?id=yj1yHnLxEg)

- **RoboVLMs** - *What Matters in Building Vision-Language-Action Models for Generalist Robots*  
  [![arXiv](https://img.shields.io/badge/arXiv-2412.14058-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2412.14058)

- **TraceVLA** - *TraceVLA: Visual Trace Prompting Enhances Spatial-Temporal Awareness for Generalist Robotic Policies*  
  [![arXiv](https://img.shields.io/badge/arXiv-2412.10345-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2412.10345)

- **Moto** - *Moto: Latent Motion Token as the Bridging Language for Learning Robot Manipulation from Videos*  
  [![arXiv](https://img.shields.io/badge/arXiv-2412.04445-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2412.04445) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://chenyi99.github.io/moto/)

- **GR-2** - *GR-2: A Generative Video-Language-Action Model with Web-Scale Knowledge for Robot Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2410.06158-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2410.06158) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://gr2-manipulation.github.io)

- **GR-MG** - *GR-MG: Leveraging Partially Annotated Data via Multi-Modal Goal-Conditioned Policy*  
  [![arXiv](https://img.shields.io/badge/arXiv-2408.14368-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2408.14368) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://gr-mg.github.io/)

- **Octo** - *Octo: An Open-Source Generalist Robot Policy*  
  [![arXiv](https://img.shields.io/badge/arXiv-2405.12213-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2405.12213) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://octo-models.github.io)

- **GR-1** - *Unleashing Large-Scale Video Generative Pre-training for Visual Robot Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2312.13139-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2312.13139) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://GR1-Manipulation.github.io)

- **RT-Trajectory** - *RT-Trajectory: Robotic Task Generalization via Hindsight Trajectory Sketches*  
  [![arXiv](https://img.shields.io/badge/arXiv-2311.01977-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2311.01977) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://rt-trajectory.github.io/)

- **RoboFlamingo** - *Vision-Language Foundation Models as Effective Robot Imitators*  
  [![arXiv](https://img.shields.io/badge/arXiv-2311.01378-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2311.01378) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://roboflamingo.github.io)

- **SuSIE** - *Zero-Shot Robotic Manipulation with Pretrained Image-Editing Diffusion Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2310.10639-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2310.10639) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](http://rail-berkeley.github.io/susie)

- **RT-1** - *RT-1: Robotics Transformer for Real-World Control at Scale*  
  [![arXiv](https://img.shields.io/badge/arXiv-2212.06817-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2212.06817) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://robotics-transformer1.github.io/)


### Vision-Language to Action Modeling

> These works use vision-language inputs while focusing on architecture and action modeling, including action tokenization, diffusion/flow action heads, reinforcement learning, robustness, and efficient inference.

- **STRONG-VLA** - *STRONG-VLA: Decoupled Robustness Learning for Vision-Language-Action Models under Multimodal Perturbations*  
  [![arXiv](https://img.shields.io/badge/arXiv-2604.10055-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2604.10055)

- **MMaDA-VLA** - *MMaDA-VLA: Large Diffusion Vision-Language-Action Model with Unified Multi-Modal Instruction and Generation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.25406-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.25406)

- **OptimusVLA** - *Global Prior Meets Local Consistency: Dual-Memory Augmented Vision-Language-Action Model for Efficient Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.20200-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.20200)

- **VLA-Pruner** - *Bridging the Semantic-Action Gap in Visual Token Pruning for Efficient VLA Inference*  
  [![arXiv](https://img.shields.io/badge/arXiv-2511.16449-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2511.16449)

- **pi_RL** - *$\pi_{\texttt{RL}}$: Online RL Fine-tuning for Flow-based Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.25889-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.25889)

- **dVLA** - *dVLA: Diffusion Vision-Language-Action Model with Multimodal Chain-of-Thought*  
  [![arXiv](https://img.shields.io/badge/arXiv-2509.25681-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2509.25681)

- **SimpleVLA-RL** - *SimpleVLA-RL: Scaling VLA Training via Reinforcement Learning*  
  [![arXiv](https://img.shields.io/badge/arXiv-2509.09674-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2509.09674)

- **RIPT-VLA** - *Interactive Post-Training for Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2505.17016-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2505.17016) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://ariostgx.github.io/ript_vla/)

- **GR00T N1** - *GR00T N1: An Open Foundation Model for Generalist Humanoid Robots*  
  [![arXiv](https://img.shields.io/badge/arXiv-2503.14734-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2503.14734) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://developer.nvidia.com/isaac/gr00t)

- **HybridVLA** - *HybridVLA: Collaborative Diffusion and Autoregression in a Unified Vision-Language-Action Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2503.10631-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2503.10631)

- **OTTER** - *OTTER: A Vision-Language-Action Model with Text-Aware Visual Feature Extraction*  
  [![arXiv](https://img.shields.io/badge/arXiv-2503.03734-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2503.03734) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://ottervla.github.io/)

- **VLA-Cache** - *VLA-Cache: Efficient Vision-Language-Action Manipulation via Adaptive Token Caching*  
  [![arXiv](https://img.shields.io/badge/arXiv-2502.02175-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2502.02175) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://vla-cache.github.io)

- **iRe-VLA** - *Improving Vision-Language-Action Model with Online Reinforcement Learning*  
  [![arXiv](https://img.shields.io/badge/arXiv-2501.16664-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2501.16664)

- **pi_0** - *$\pi_0$: A Vision-Language-Action Flow Model for General Robot Control*  
  [![arXiv](https://img.shields.io/badge/arXiv-2410.24164-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2410.24164) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://physicalintelligence.company/blog/pi0)

- **OpenVLA** - *OpenVLA: An Open-Source Vision-Language-Action Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2406.09246-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2406.09246) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://openvla.github.io/)


## VLAs with Single Additional Modality

This section covers VLA methods that add one extra input channel to address scenario-specific information needs beyond RGB observations and language instructions.

### Depth Modality

> Depth mainly provides metric distance and image-aligned spatial-layout cues for localization, obstacle awareness, and action constraints.

- **SOMA** - *Spatial Memory for Out-of-Vision Manipulation in Vision-Language-Action*  
  [![arXiv](https://img.shields.io/badge/arXiv-2605.22283-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2605.22283)

- **Evo-Depth** - *Evo-Depth: A Lightweight Depth-Enhanced Vision-Language-Action Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2605.14950-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2605.14950)

- **GST-VLA** - *GST-VLA: Structured Gaussian Spatial Tokens for 3D Depth-Aware Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.09079-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.09079)

- **UniLACT** - *UniLACT: Depth-Aware RGB Latent Action Learning for Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.20231-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.20231) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://manishgovind.github.io/unilact-vla/)

- **AutoFly** - *AutoFly: Vision-Language-Action Model for UAV Autonomous Navigation in the Wild*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.09657-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.09657)

- **PEAfowl** - *PEAfowl: Perception-Enhanced Multi-View Vision-Language-Action for Bimanual Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2601.17885-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2601.17885) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://peafowlvla.github.io/)

- **ActiveVLA** - *ActiveVLA: Injecting Active Perception into Vision-Language-Action Models for Precise 3D Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2601.08325-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2601.08325)

- **GeoPredict** - *GeoPredict: Leveraging Predictive Kinematics and 3D Gaussian Geometry for Precise VLA Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2512.16811-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2512.16811)

- **VIPA-VLA** - *Spatial-Aware VLA Pretraining through Visual-Physical Alignment from Human Videos*  
  [![arXiv](https://img.shields.io/badge/arXiv-2512.13080-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2512.13080)

- **FALCON** - *From Spatial to Actions: Grounding Vision-Language-Action Model in Spatial Foundation Priors*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.17439-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.17439) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://falcon-vla.github.io/)

- **DepthVLA** - *DepthVLA: Enhancing Vision-Language-Action Models with Depth-Aware Spatial Reasoning*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.13375-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.13375)

- **Spatial Forcing** - *Spatial Forcing: Implicit Spatial Representation Alignment for Vision-language-action Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.12276-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.12276) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://spatial-forcing.github.io/)


### Point Cloud Modality

> Point clouds provide explicit 3D spatial structure beyond image-plane observations, supporting object shape, reachability, and workspace-aware action reasoning.

- **PointACT** - *PointACT: Vision-Language-Action Models with Multi-Scale Point-Action Interaction*  
  [![arXiv](https://img.shields.io/badge/arXiv-2605.21414-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2605.21414) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://cshizhe.github.io/projects/pointact.html)

- **LaMP** - *LaMP: Learning Vision-Language-Action Policies with 3D Scene Flow as Latent Motion Prior*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.25399-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.25399) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://summerwxk.github.io/lamp-project-page/)

- **UniDex** - *UniDex: A Robot Foundation Suite for Universal Dexterous Hand Control from Egocentric Human Videos*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.22264-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.22264)

- **Avi** - *Avi: Action from Volumetric Inference*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.21746-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.21746) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://avi-3drobot.github.io/)

- **GeoVLA** - *GeoVLA: Empowering 3D Representations in Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2508.09071-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2508.09071) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://linsun449.github.io/GeoVLA/)

- **BridgeVLA** - *BridgeVLA: Input-Output Alignment for Efficient 3D Manipulation Learning with Vision-Language Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2506.07961-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2506.07961) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://bridgevla.github.io/)

- **OG-VLA** - *OG-VLA: Orthographic Image Generation for 3D-Aware Vision-Language Action Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2506.01196-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2506.01196) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://og-vla.github.io/)

- **PointVLA** - *PointVLA: Injecting the 3D World into Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2503.07511-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2503.07511)

- **3D-VLA** - *3D-VLA: A 3D Vision-Language-Action Generative World Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2403.09631-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2403.09631)


### Tactile Modality

> Tactile inputs provide local contact observations such as deformation, slip, and contact state, making them useful for insertion, grasping, and other contact-rich manipulation tasks.

- **T-Rex** - *T-Rex: Tactile-Reactive Dexterous Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2606.17055-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2606.17055) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://tactile-rex.github.io/)

- **TacCoRL** - *TacCoRL: Integrating Tactile Feedback into VLA via Simulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2606.11743-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2606.11743) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://tac-corl.github.io/)

- **AT-VLA** - *AT-VLA: Adaptive Tactile Injection for Enhanced Feedback Reaction in Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2605.07308-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2605.07308) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://sites.google.com/view/at-vla)

- **TacFiLM** - *Tactile Modality Fusion for Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.14604-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.14604)

- **TacVLA** - *TacVLA: Contact-Aware Tactile Fusion for Robust Vision-Language-Action Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.12665-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.12665) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://sites.google.com/view/tacvla)

- **FG-CLTP** - *FG-CLTP: Fine-Grained Contrastive Language Tactile Pretraining for Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.10871-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.10871)

- **DreamTacVLA** - *Learning to Feel the Future: DreamTacVLA for Contact-Rich Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2512.23864-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2512.23864)

- **VLA-Touch** - *VLA-Touch: Enhancing Vision-Language-Action Models with Dual-Level Tactile Feedback*  
  [![arXiv](https://img.shields.io/badge/arXiv-2507.17294-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2507.17294)

- **VTLA** - *VTLA: Vision-Tactile-Language-Action Model with Preference Learning for Insertion Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2505.09577-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2505.09577) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://sites.google.com/view/vtla)

- **TLA** - *TLA: Tactile-Language-Action Model for Contact-Rich Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2503.08548-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2503.08548) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://sites.google.com/view/tactile-language-action/)

- **BiTLA** - *BiTLA: A Bimanual Tactile-Language-Action Model for Contact-Rich Robotic Manipulation*  
  [![DOI](https://img.shields.io/badge/DOI-10.1145%2F3728485.3759237-007ec6.svg)](https://doi.org/10.1145/3728485.3759237)


### Force Modality

> Force-aware VLAs use force or torque feedback to model interaction intensity and support hybrid force-position control, gentle manipulation, and contact correction.

- **ForceVLA2** - *ForceVLA2: Unleashing Hybrid Force-Position Control with Force Awareness for Contact-Rich Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.15169-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.15169) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://sites.google.com/view/force-vla2/home)

- **FAVLA** - *FAVLA: A Force-Adaptive Fast-Slow VLA model for Contact-Rich Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.23648-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.23648)

- **CRAFT** - *CRAFT: Adapting VLA Models to Contact-rich Manipulation via Force-aware Curriculum Fine-tuning*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.12532-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.12532)

- **FD-VLA** - *FD-VLA: Force-Distilled Vision-Language-Action Model for Contact-Rich Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.02142-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.02142)

- **NeuroVLA** - *A Brain-inspired Embodied Intelligence for Fluid and Fast Reflexive Robotics Control*  
  [![arXiv](https://img.shields.io/badge/arXiv-2601.14628-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2601.14628)

- **TA-VLA** - *TA-VLA: Elucidating the Design Space of Torque-aware Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2509.07962-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2509.07962) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://zzongzheng0918.github.io/Torque-Aware-VLA.github.io/)

- **ForceVLA** - *ForceVLA: Enhancing VLA Models with a Force-aware MoE for Contact-rich Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2505.22159-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2505.22159) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://sites.google.com/view/forcevla2025)


### Audio Modality

> Audio expands the VLA interface with speech instructions, contact sounds, and environmental acoustic cues that may be unavailable from vision alone.

- **HEAR** - *Towards the Vision-Sound-Language-Action Paradigm: The HEAR Framework for Sound-Centric Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.16086-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.16086)

- **Audio-VLA** - *Audio-VLA: Adding Contact Audio Perception to Vision-Language-Action Model for Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2511.09958-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2511.09958)

- **RoboOmni** - *RoboOmni: Proactive Robot Manipulation in Omni-modal Context*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.23763-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.23763)

- **VITA-E** - *VITA-E: Natural Embodied Interaction with Concurrent Seeing, Hearing, Speaking, and Acting*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.21817-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.21817) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://lxysl.github.io/VITA-E/)

- **ELLSA** - *End-to-end Listen, Look, Speak and Act*  
  [![arXiv](https://img.shields.io/badge/arXiv-2510.16756-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2510.16756)

- **RoboEgo** - *RoboEgo System Card: An Omnimodal Model with Native Full Duplexity*  
  [![arXiv](https://img.shields.io/badge/arXiv-2506.01934-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2506.01934)

- **VLAS** - *VLAS: Vision-Language-Action Model With Speech Instructions For Customized Robot Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2502.13508-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2502.13508)

- **SVA** - *SVA: Towards Speech-Enabled Vision-Language-Action Model*  
  [![ScienceDirect](https://img.shields.io/badge/ScienceDirect-S003132032501578X-f26b21.svg)](https://www.sciencedirect.com/science/article/abs/pii/S003132032501578X)

- **RoboNurse-VLA** - *RoboNurse-VLA: Robotic Scrub Nurse System based on Vision-Language-Action Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2409.19590-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2409.19590) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://robonurse-vla.github.io)


### Gaze Modality

> Gaze-conditioned VLAs use human attention as an intent cue, helping robots infer targets, preferences, or interaction focus in human-centered manipulation.

- **Gaze2Act** - *Gaze2Act: Gaze-Conditioned Vision-Language-Action Policies for Interactive Robot Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2605.30282-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2605.30282) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://zuo-kuangji.github.io/Gaze2Act/)

- **GazeVLA** - *GazeVLA: Learning Human Intention for Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2604.22615-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2604.22615) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://gazevla.github.io)

- **Gaze-Regularized VLA** - *Gaze-Regularized Vision-Language-Action Models for Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.23202-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.23202)

- **DAA** - *Multi-task real-robot data with gaze attention for dual-arm fine manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2401.07603-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2401.07603) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://sites.google.com/view/multi-task-fine)


### Other Emerging Modalities

> This section collects newer input channels such as gesture, thermal, event, and other specialized signals that expand VLA perception beyond standard vision-language inputs.

- **GIVE** - *GIVE: Grounding Human Gestures in Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2606.13435-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2606.13435) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://luis-cloud-sg.github.io/GIVE-project/)

- **GesVLA** - *GesVLA: Gesture-Aware Vision-Language-Action Model Embedded Representations*  
  [![arXiv](https://img.shields.io/badge/arXiv-2605.22812-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2605.22812) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://gwxuan.github.io/GesVLA/)

- **E-VLA** - *E-VLA: Event-Augmented Vision-Language-Action Model for Dark and Blurred Scenes*  
  [![arXiv](https://img.shields.io/badge/arXiv-2604.04834-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2604.04834)

- **ThermoAct** - *ThermoAct: Thermal-Aware Vision-Language-Action Models for Robotic Perception and Decision-Making*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.25044-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.25044)

- **Safe-Night VLA** - *Safe-Night VLA: Seeing the Unseen via Thermal-Perceptive Vision-Language-Action Models for Safety-Critical Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.05754-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.05754)

- **SignVLA** - *SignVLA: A Gloss-Free Vision-Language-Action Framework for Real-Time Sign Language-Guided Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.22514-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.22514)

- **Expert-VLA** - *VLA Model-Expert Collaboration for Bi-directional Manipulation Learning*  
  [![arXiv](https://img.shields.io/badge/arXiv-2503.04163-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2503.04163) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://aoqunjin.github.io/Expert-VLA/)


## VLAs with Multiple Additional Modalities

This section covers VLA methods that combine multiple additional modalities for tasks where geometry, contact, and environmental signals jointly affect action generation.

### Depth and Point Cloud Modalities (3D Geometry)

> This 3D geometry branch combines depth cues and point-level structure, moving from distance estimation toward action-relevant spatial modeling.

- **GEAR-VLA** - *GEAR-VLA: Learning Geometry-Aware Action Representations for Generalizable Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2606.08530-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2606.08530)

- **MotionVLA** - *MotionVLA: Injecting Geometric Motion into Vision-Language-Action Model*  
  [![arXiv](https://img.shields.io/badge/arXiv-2606.08288-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2606.08288)

- **DiffRender-VLA** - *Localizing, Structuring, and Rendering: Bridging 3D and 2D Vision-Language-Action Models for Robotic Manipulation*  
  [![CVPR](https://img.shields.io/badge/CVPR-poster_39208-005bbb.svg)](https://cvpr.thecvf.com/virtual/2026/poster/39208)

- **StemVLA** - *StemVLA: An Open-Source Vision-Language-Action Model with Future 3D Spatial Geometry Knowledge and 4D Historical Representation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.23721-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.23721)

- **AugVLA-3D** - *AugVLA-3D: Depth-Driven Feature Augmentation for Vision-Language-Action Models*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.10698-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.10698)

- **Any3D-VLA** - *Any3D-VLA: Enhancing VLA Robustness via Diverse Point Clouds*  
  [![arXiv](https://img.shields.io/badge/arXiv-2602.00807-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2602.00807) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://xianzhefan.github.io/Any3D-VLA.github.io)

- **4D-VLA** - *4D-VLA: Spatiotemporal Vision-Language-Action Pretraining with Cross-Scene Calibration*  
  [![arXiv](https://img.shields.io/badge/arXiv-2506.22242-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2506.22242)

- **3D-CAVLA** - *3D CAVLA: Leveraging Depth and 3D Context to Generalize Vision Language Action Models for Unseen Tasks*  
  [![arXiv](https://img.shields.io/badge/arXiv-2505.05800-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2505.05800) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://3d-cavla.github.io)

- **RoboFlamingo-Plus** - *RoboFlamingo-Plus: Fusion of Depth and RGB Perception with Vision-Language Models for Enhanced Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2503.19510-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2503.19510)

- **RoboMM** - *RoboTron-Mani: All-in-One Multimodal Large Model for Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2412.07215-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2412.07215)


### Tactile and Force Modalities

> These methods combine local touch and mechanical feedback, allowing VLAs to perceive contact state while regulating interaction force during execution.

- **TORL-VLA** - *TORL-VLA: Tactile Guided Online Reinforcement Learning for Contact-Rich Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2606.09337-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2606.09337) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://torl-vla.github.io/)

- **Tabero** - *Tabero: Learning Gentle Manipulation with Closed-Loop Force Feedback from Vision, Touch, and Language*  
  [![arXiv](https://img.shields.io/badge/arXiv-2605.27886-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2605.27886)

- **HapticVLA** - *HapticVLA: Contact-Rich Manipulation via Vision-Language-Action Model without Inference-Time Tactile Sensing*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.15257-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.15257)

- **MoDE-VLA** - *Towards Human-Like Manipulation through RL-Augmented Teleoperation and Mixture-of-Dexterous-Experts VLA*  
  [![arXiv](https://img.shields.io/badge/arXiv-2603.08122-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2603.08122) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://sites.google.com/view/mode-vla)

- **TaF-VLA** - *TaF-VLA: Tactile-Force Alignment in Vision-Language-Action Models for Force-aware Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2601.20321-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2601.20321)

- **Cui et al.** - *End-to-End Dexterous Arm-Hand VLA Policies via Shared Autonomy: VR Teleoperation Augmented by Autonomous Hand VLA Policy for Efficient Data Collection*  
  [![arXiv](https://img.shields.io/badge/arXiv-2511.00139-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2511.00139)

- **Tactile-VLA** - *Tactile-VLA: Unlocking Vision-Language-Action Model's Physical Knowledge for Tactile Generalization*  
  [![arXiv](https://img.shields.io/badge/arXiv-2507.09160-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2507.09160)


### Other Multiple Additional Modalities

> These works explore task-specific multisensory mixtures where several physical signals are needed to handle complex or long-tail scenarios.

- **OmniVLA** - *OmniVLA: Physically-Grounded Multimodal VLA with Unified Multi-Sensor Perception for Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2511.01210-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2511.01210)

- **MLA** - *MLA: A Multisensory Language-Action Model for Multimodal Understanding and Forecasting in Robotic Manipulation*  
  [![arXiv](https://img.shields.io/badge/arXiv-2509.26642-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2509.26642) [![Project](https://img.shields.io/badge/Project-page-blue.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNiAxNiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJ3aGl0ZSIgc3Ryb2tlLXdpZHRoPSIxLjYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPGNpcmNsZSBjeD0iOCIgY3k9IjgiIHI9IjYuMiIvPjxwYXRoIGQ9Ik0xLjggOGgxMi40Ii8%2BPHBhdGggZD0iTTggMS44YzEuOCAxLjY1IDIuNzUgMy44IDIuNzUgNi4yUzkuOCAxMi41NSA4IDE0LjIiLz48cGF0aCBkPSJNOCAxLjhDNi4yIDMuNDUgNS4yNSA1LjYgNS4yNSA4UzYuMiAxMi41NSA4IDE0LjIiLz48L3N2Zz4%3D&logoWidth=14)](https://robotic-mla.github.io/)

- **Zhang et al.** - *A Unified Perception-Language-Action Framework for Adaptive Autonomous Driving*  
  [![arXiv](https://img.shields.io/badge/arXiv-2507.23540-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2507.23540)

- **FuSe** - *Beyond Sight: Finetuning Generalist Robot Policies with Heterogeneous Sensors via Language Grounding*  
  [![arXiv](https://img.shields.io/badge/arXiv-2501.04693-b31b1b.svg?logo=arxiv)](https://arxiv.org/abs/2501.04693)


## Acknowledgements

> This repository is inspired by the open curation style of community survey repositories, including [Awesome World Models for Robotic Policy Learning](https://github.com/NTUMARS/Awesome-World-Model-for-Robotics-Policy) and [Large VLM-based VLA for Robotic Manipulation](https://github.com/JiuTian-VL/Large-VLM-based-VLA-for-Robotic-Manipulation). We thank their maintainers for making these resources public.

## Citation

> The citation entry will be added after the preprint is publicly available.

## License

> This repository is released under the [Creative Commons Attribution 4.0 International License](LICENSE).
