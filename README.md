# Mingyu Sung
**AI Research Engineer — Efficient GenAI Inference (Quantization · Caching · Acceleration)**
Nota AI, Platform Team (Quantizer) · South Korea · mingyu.sung@nota.ai
[github](https://github.com/Bluear7878) · [homepage](https://bluear7878.github.io) · [scholar](https://scholar.google.co.kr/citations?user=TZw2NQgAAAAJ) · [linkedin](https://www.linkedin.com/in/mingyu-sung-83040b192/)

AI Research Engineer at Nota AI (Platform Team, Quantizer part). Ph.D. in Artificial Intelligence (KNU, 2026). Works on efficient generative-model inference: model quantization, diffusion/LLM cache acceleration, CUDA kernel optimization, split computing, and training-free KV-cache compression. Core contributor to the Nunchaku CUDA acceleration engine (ICLR 2025 Spotlight); 15 merged PRs across Nunchaku, ComfyUI-nunchaku, ByteDance DreamO, and Hugging Face Transformers.

Citations 48 · h-index 4 · i10-index 1 (as of 2026-09-28)

## Experience
- **AI Research Engineer — Platform Team, Quantizer Part**, Nota AI (2026-02–present)
  - LLM/VLM quantization platform: GPTQ, AWQ, SmoothQuant, QuaRot/SpinQuant pipelines; NVFP4 and GGUF export paths; MoE all-expert calibration; KV-cache quantization (verifiable via merged internal PR record).
  - Model enablement & evaluation: EXAONE 4.0 / MoE, Qwen3 / 3.5(-VL), Phi-3 (LongRoPE), gpt-oss, embedding/reranker and video-diffusion (Wan, Cosmos) evaluation harnesses.
  - K-EXAONE 236B (MoE) optimization for FuriosaAI's data-center NPU, with LG AI Research — ~71% model-size reduction at ~99.2% accuracy retention (GPQA 79.80, IFBench 68.98, AIME25 88.57); announced 2026-06-30.

## Education
- **Ph.D.** in Artificial Intelligence, Kyungpook National University (KNU) (2021-08–2026-02)
- **M.S.** in Computer Science, Kyungpook National University (KNU) (2019-09–2021-08)
- **B.S.** in Computer Science, Kyungpook National University (KNU) (2013-03–2019-08)

## Research
- **StreamPRS** (2026): Single-context-prefill approximation of KVzip's reconstruction-based KV-cache eviction; contributions framed as Factorization / Method / System. (Scope-limited per claims ledger — do not overstate.)

## Open Source
- **Nunchaku** (`nunchux-ai/nunchaku`) — Core Contributor · 2025 – 2026-02 · 9 merged PRs
  *CUDA acceleration engine for 4-bit neural networks (ICLR 2025 Spotlight, 3.9k+ stars)*
  - Cache optimizations — V2 FBCaching (#621), double FB cache, TeaCache batch processing (#601) — for 2–5x additional speedup
  - IP-Adapter (XLabs flux-ip-adapter-v2) support (#418)
  - Fixes: LoRA key mismatch (#557), ControlNet (#360, #452), Sana (#380), offload segfault (#440)
  - Forward-pass tensor-op cleanup (#491)
- **ComfyUI-nunchaku** (`nunchux-ai/ComfyUI-nunchaku`) — Contributor · 2025 · 2 merged PRs
  *ComfyUI integration for the Nunchaku engine*
  - IP-Adapter support for ComfyUI (#305)
  - Cache-mechanism file separation (#474)
- **DreamO** (`bytedance/DreamO`) — Contributor · 2025 · 1 merged PRs
  *ByteDance's unified image-customization framework*
  - Dynamic FBCache / DoubleFBCache support for Nunchaku engine integration (#104)
- **Transformers** (`huggingface/transformers`) — Contributor · 2026 · 3 merged PRs
  *Hugging Face Transformers library*
  - Fixed float16 overflow in Gemma4 vision pooler (#46277)
  - Fixed Gemma `sliding_window` being halved on every config save/reload, a silent accuracy regression for EmbeddingGemma (#47940)
  - Fixed `_init_weights` reading a quantized child's `weight`, which broke loading CLIP-family quantized checkpoints (#47921)

## Publications
- H2-Cache: A Novel Hierarchical Dual-Stage Cache for High-Performance Acceleration of Generative Diffusion Models. *IEEE Open Journal of the Computer Society*, 2025.
- A Novel VLM-Guided Diffusion Model for Remote Sensing Image Super-Resolution. *IEEE Geoscience and Remote Sensing Letters*, 2025. (Best Paper Award, KNU-EE Research Congress)
- DeCo-MeSC: Deep Compression-Based Memory-Constrained Split Computing Framework for Cooperative Inference of Neural Network. *IEEE Transactions on Vehicular Technology*, 2025.
- Generative Diffusion Model-Based Deep Learning Framework for Remaining Useful Life Prediction. *IEEE Internet of Things Journal*, 2025. (Co-first author)
- Entropy-based sampling for efficient training of deep learning on CNC machining dataset. *Electronics Letters*, 2024.
- Probabilistic Classification Method of Spiking Neural Network Based on Multi-Labeling of Neurons. *Mathematics*, 2023.
- Training and Inference using Approximate Floating-Point Arithmetic for Energy Efficient Spiking Neural Network Processors. *ICEIC*, 2021.
- Training spiking neural networks with an adaptive leaky integrate-and-fire neuron. *IEEE ICCE-Asia*, 2020.

## Preprints
- GLYPH-SR: Can We Achieve Both High-Quality Image Super-Resolution and High-Fidelity Text Recovery via VLM-guided Latent Diffusion Model?. [arXiv:2510.26339](https://arxiv.org/abs/2510.26339), 2025.
- Memory- and Latency-Constrained Inference of Large Language Models via Adaptive Split Computing. [arXiv:2511.04002](https://arxiv.org/abs/2511.04002), 2025.
- No Pose Estimation? No Problem: Pose-Agnostic and Instance-Aware Test-Time Adaptation for Monocular Depth Estimation. [arXiv:2511.05055](https://arxiv.org/abs/2511.05055), 2025.
- Why Should the Server Do It All?: A Scalable, Versatile, and Model-Agnostic Framework for Server-Light DNN Inference over Massively Distributed Clients via Training-Free Intermediate Feature Compression. [arXiv:2511.11608](https://arxiv.org/abs/2511.11608), 2025.
- Range Asymmetric Numeral Systems-Based Lightweight Intermediate Feature Compression for Split Computing of Deep Neural Networks. [arXiv:2511.11664](https://arxiv.org/abs/2511.11664), 2025.

## Projects
- **[K-EXAONE 236B MoE Optimization (Nota AI × LG AI Research × FuriosaAI)](https://blog.nota.ai/newsroom/k-exaone-moe-optimization)** (2026), Quantization Engineer — Optimized the 236B-parameter MoE model for FuriosaAI's data-center NPU via targeted precision analysis of degradation-prone sections — ~71% size reduction with ~99.2% accuracy retention (GPQA 79.80 / IFBench 68.98 / AIME25 88.57).
- **LLM Inference Optimization (Samsung Challenge)** (2024), Lead Developer — Optimized pipeline for Phi-3 using Torch-TensorRT conversion and memory-aware dynamic batching to accelerate LLM inference.
- **Advanced CNC Machine Tool Diagnosis & Prognosis (KERI)** (2023), Lead Developer — Deep learning models for tool wear classification, anomaly detection, and RUL prognosis.
- **AI-based Intelligent CCTV (ABB Project)** (2023), AI Optimization Engineer — Optimized an LSTR behavior-detection model for edge devices via Knowledge Distillation (TransKD) and Deep Compression — 25x model compression.
- **Global Basic Research Laboratory (NRF Project)** (2022), Participating Researcher — Deep learning-based channel estimation (CNN denoising, self-supervised learning) for IRS-aided communication systems.
- **ML-based Sensor Data Analysis (JS System Project)** (2022), Lead Developer — ML-based sensor feature-importance extraction and model performance optimization.

## Awards
- Best Paper Award, KNU-EE Research Congress (2025) — A Novel VLM-Guided Diffusion Model for Remote Sensing Image Super-Resolution

## Skills
- **Research**: model quantization, KV-cache compression, diffusion/LLM inference acceleration, split computing, super-resolution, long-context evaluation
- **Programming**: Python, C++, CUDA C, MATLAB
- **Frameworks & Tools**: PyTorch, HuggingFace Transformers, TensorRT, Triton, flash-attn, Docker, Git, LaTeX
- **Methodology**: preregistration, claims ledger, freeze discipline

## Languages
- Korean: native
- English: business fluent
