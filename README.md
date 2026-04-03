<div align="center">
  <h1>Don’t Waste Bits!<br>Adaptive KV-Cache Quantization for Lightweight On-Device LLMs</h1>

[![arXiv](https://img.shields.io/badge/arXiv-2602.20205-b31b1b.svg)](https://scholar.google.com/citations?user=RL_CijgAAAAJ&hl=en&oi=ao)
[![Paper](https://img.shields.io/badge/Paper-CVPR%202026-8A2BE2)](https://cvpr.thecvf.com/)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

</div>


<p align="justify">
<b>Don’t Waste Bits!</b> introduces a <b>data-driven adaptive KV-cache quantization framework</b> for efficient <b>on-device Large Language Model (LLM) inference</b>. This work addresses the critical memory and latency bottlenecks of KV-cache storage by dynamically allocating precision at the token level using a lightweight controller guided by entropy, rarity, and attention-based signals. By assigning higher precision to informative tokens and compressing less important ones, the proposed method achieves a superior <b>accuracy–latency–memory trade-off</b> compared to static and heuristic quantization approaches. This work has been accepted to the <b>IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR) 2026</b>.
</p>

## 🔍 Overview
<p align="justify">
We introduce a data-driven controller for adaptive KV-cache quantization to address the KV-cache memory bottleneck in on-device LLM inference, where static quantization often degrades reasoning quality. Our method extracts lightweight token-level signals (e.g., token frequency, attention variance, and entropy-based uncertainty) and uses a learned MLP controller to assign per-token KV precision (2/4/8-bit or FP16) during decoding. This adaptive precision policy reduces KV memory footprint and latency while preserving (or improving) accuracy compared to static KV quantization, rule-based baselines, and FP16 inference.

<div align="center">
  <img src="Overview.jpg" width="90%"/>
</div>
