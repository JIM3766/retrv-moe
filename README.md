# Retrv-MoE Evaluation Artifact

This repository provides the official evaluation/inference artifact for the KDD 2026 paper:

**Retrv-MoE: Scaling Unified Multimodal Retrieval with Sparse Mixture-of-Experts**

## Overview

Retrv-MoE is a unified multimodal retriever based on sparse Mixture-of-Experts. This minimal artifact release contains the evaluation entry point, model wrapper, dataset loader, data collator, and scripts needed to run evaluation with a prepared checkpoint.

Training code is not included in this minimal artifact release.

## Repository Structure

```text
.
├── checkpoints/
├── collators/
├── dataset/
├── eval/
├── models/
├── scripts/eval/
└── README.md
