<h1 align="center">
  <img src="assets/title-icon.png" width="52" align="absmiddle" style="vertical-align: 0.18em;" alt="Project icon">
  Vision-Language-Action Models for Diverse Application Scenarios: A Survey of Input Modalities
</h1>

<p align="center">
  <strong>A companion repository for a survey on input modalities in Vision-Language-Action models.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/arXiv-coming%20soon-b31b1b.svg?logo=arxiv" alt="arXiv coming soon">
  <a href="https://mpil-lab.github.io/lab-webpage/index.html"><img src="https://img.shields.io/badge/Lab-MPIL--Lab-blue.svg" alt="Lab: MPIL Lab"></a>
  <img src="https://img.shields.io/badge/HuggingFace-coming%20soon-ffcc4d.svg?logo=huggingface&logoColor=black" alt="Hugging Face coming soon">
  <img src="https://img.shields.io/badge/License-MIT-black.svg" alt="License: MIT">
</p>

This repository is being prepared as a public resource for tracking how VLA systems use different input modalities. The full paper list, taxonomy details, and supplementary materials are still being curated and checked for consistency.

## Current Status

We are currently organizing:

- the modality taxonomy;
- representative papers and model families;
- dataset and benchmark links;
- compact figures for the project page;
- contribution guidelines for future updates.

The initial release will focus on a clean, readable survey companion page before adding the full bibliography.

## Scope

The repository focuses on input signals used by Vision-Language-Action models for embodied agents, robotic manipulation, navigation, and related physical decision-making tasks.

<table>
  <thead>
    <tr>
      <th bgcolor="#ffffff">Area</th>
      <th bgcolor="#ffffff">Modalities</th>
      <th bgcolor="#ffffff">Role in VLA systems</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td bgcolor="#ffffff">👁️ Visual observation</td>
      <td bgcolor="#ffffff">RGB image, video, event stream</td>
      <td bgcolor="#ffffff">Scene understanding, object localization, temporal dynamics</td>
    </tr>
    <tr>
      <td bgcolor="#f8fafc">💬 Language instruction</td>
      <td bgcolor="#f8fafc">Text prompt, goal description, dialogue</td>
      <td bgcolor="#f8fafc">Task specification, human intent, constraints</td>
    </tr>
    <tr>
      <td bgcolor="#ffffff">📐 Geometry and state</td>
      <td bgcolor="#ffffff">Depth, point cloud, proprioception</td>
      <td bgcolor="#ffffff">Spatial layout, pose, contact-aware planning</td>
    </tr>
    <tr>
      <td bgcolor="#f8fafc">✋ Contact-rich sensing</td>
      <td bgcolor="#f8fafc">Tactile, force, torque</td>
      <td bgcolor="#f8fafc">Manipulation feedback, slip/contact detection</td>
    </tr>
    <tr>
      <td bgcolor="#ffffff">📡 Audio and signal cues</td>
      <td bgcolor="#ffffff">Audio, radar, thermal</td>
      <td bgcolor="#ffffff">Non-visual context, hidden state, environment feedback</td>
    </tr>
    <tr>
      <td bgcolor="#f8fafc">🧠 Human-centric cues</td>
      <td bgcolor="#f8fafc">Gaze, gesture, brain signal</td>
      <td bgcolor="#f8fafc">Attention, intention, assistive interaction</td>
    </tr>
  </tbody>
</table>

## Resource Roadmap

<table>
  <thead>
    <tr>
      <th bgcolor="#ffffff">Resource</th>
      <th bgcolor="#ffffff">Status</th>
      <th bgcolor="#ffffff">Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td bgcolor="#ffffff">Survey paper</td>
      <td bgcolor="#ffffff">Coming soon</td>
      <td bgcolor="#ffffff">Preprint link will be added after release.</td>
    </tr>
    <tr>
      <td bgcolor="#f8fafc">Paper list</td>
      <td bgcolor="#f8fafc">In progress</td>
      <td bgcolor="#f8fafc">We are checking categories, metadata, and citation consistency.</td>
    </tr>
    <tr>
      <td bgcolor="#ffffff">Modality taxonomy</td>
      <td bgcolor="#ffffff">In progress</td>
      <td bgcolor="#ffffff">The first version will prioritize clarity over exhaustive coverage.</td>
    </tr>
    <tr>
      <td bgcolor="#f8fafc">Figures</td>
      <td bgcolor="#f8fafc">In progress</td>
      <td bgcolor="#f8fafc">Compact diagrams and modality icons will be added here.</td>
    </tr>
    <tr>
      <td bgcolor="#ffffff">Citation</td>
      <td bgcolor="#ffffff">Coming soon</td>
      <td bgcolor="#ffffff">BibTeX will be added with the public preprint.</td>
    </tr>
  </tbody>
</table>

## Contribution

If you find missing papers, incorrect metadata, broken links, or taxonomy issues, please feel free to submit a pull request. Issues and suggestions for related surveys, datasets, and benchmarks are also welcome.

## Citation

The citation entry will be added after the preprint is publicly available.

## Maintainers

Maintained by the MPIL Lab.
