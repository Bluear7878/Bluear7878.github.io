# 성민규
**AI Research Engineer — 효율적 생성모델 추론 (양자화 · 캐싱 · 가속)**
Nota AI, Platform팀 (Quantizer) · 대한민국 · mingyu.sung@nota.ai
[github](https://github.com/Bluear7878) · [homepage](https://bluear7878.github.io) · [scholar](https://scholar.google.co.kr/citations?user=TZw2NQgAAAAJ) · [linkedin](https://www.linkedin.com/in/mingyu-sung-83040b192/)

Nota AI Platform팀 Quantizer 파트의 AI Research Engineer. 인공지능학 박사 (경북대, 2026). 효율적 생성모델 추론 연구: 모델 양자화, 디퓨전/LLM 캐시 가속, CUDA 커널 최적화, split computing, training-free KV-cache 압축. Nunchaku CUDA 가속 엔진 (ICLR 2025 Spotlight) 핵심 기여자; Nunchaku, ComfyUI-nunchaku, ByteDance DreamO, Hugging Face Transformers에 총 15개 PR 머지.

Citations 48 · h-index 4 · i10-index 1 (as of 2026-09-28)

## Experience
- **AI Research Engineer — Platform팀 Quantizer 파트**, Nota AI (2026-02–present)
  - LLM/VLM 양자화 플랫폼: GPTQ, AWQ, SmoothQuant, QuaRot/SpinQuant 파이프라인; NVFP4·GGUF export 경로; MoE all-expert calibration; KV-cache 양자화 (머지된 사내 PR 기록으로 검증 가능).
  - 모델 지원 및 평가: EXAONE 4.0 / MoE, Qwen3 / 3.5(-VL), Phi-3 (LongRoPE), gpt-oss, embedding/reranker 및 비디오 디퓨전 (Wan, Cosmos) 평가 하네스.
  - LG AI Research 협업, FuriosaAI 데이터센터 NPU용 K-EXAONE 236B (MoE) 최적화 — 모델 크기 약 71% 감축, 정확도 약 99.2% 유지 (GPQA 79.80, IFBench 68.98, AIME25 88.57); 2026-06-30 공개.

## Education
- **박사 (Ph.D.)** in 인공지능학과, 경북대학교 (KNU) (2021-08–2026-02)
- **석사 (M.S.)** in 컴퓨터학부, 경북대학교 (KNU) (2019-09–2021-08)
- **학사 (B.S.)** in 컴퓨터학부, 경북대학교 (KNU) (2013-03–2019-08)

## Research
- **StreamPRS** (2026): KVzip의 재구성 기반 KV-cache 축출을 단일-context-prefill로 근사; 기여는 Factorization / Method / System으로 규정. (claims ledger 기준 범위-한정 — 과장 금지.)

## Open Source
- **Nunchaku** (`nunchux-ai/nunchaku`) — Core Contributor · 2025 – 2026-02 · 9 merged PRs
  *4-bit 신경망용 CUDA 가속 엔진 (ICLR 2025 Spotlight, 3.9k+ stars)*
  - 캐시 최적화 설계·구현 — V2 FBCaching (#621), double FB cache, TeaCache 배치 처리 (#601) — 추가 2–5배 가속
  - IP-Adapter (XLabs flux-ip-adapter-v2) 지원 (#418)
  - 수정: LoRA 키 불일치 (#557), ControlNet (#360, #452), Sana (#380), offload segfault (#440)
  - forward-pass 텐서 연산 정리 (#491)
- **ComfyUI-nunchaku** (`nunchux-ai/ComfyUI-nunchaku`) — Contributor · 2025 · 2 merged PRs
  *Nunchaku 엔진의 ComfyUI 연동*
  - ComfyUI용 IP-Adapter 지원 (#305)
  - 캐시 메커니즘 파일 분리 (#474)
- **DreamO** (`bytedance/DreamO`) — Contributor · 2025 · 1 merged PRs
  *ByteDance의 통합 이미지 커스터마이제이션 프레임워크*
  - Nunchaku 엔진 연동을 위한 동적 FBCache / DoubleFBCache 지원 (#104)
- **Transformers** (`huggingface/transformers`) — Contributor · 2026 · 3 merged PRs
  *Hugging Face Transformers 라이브러리*
  - Gemma4 vision pooler의 float16 오버플로 수정 (#46277)
  - config 저장/로드마다 Gemma `sliding_window`가 반감되던 결함 수정 — EmbeddingGemma의 무증상 정확도 회귀 (#47940)
  - 양자화된 자식 모듈의 `weight`를 읽던 `_init_weights` 수정 — CLIP 계열 양자화 체크포인트 로드 실패 (#47921)

## Publications
- H2-Cache: A Novel Hierarchical Dual-Stage Cache for High-Performance Acceleration of Generative Diffusion Models. *IEEE Open Journal of the Computer Society*, 2025.
- A Novel VLM-Guided Diffusion Model for Remote Sensing Image Super-Resolution. *IEEE Geoscience and Remote Sensing Letters*, 2025. (Best Paper Award, KNU-EE Research Congress)
- DeCo-MeSC: Deep Compression-Based Memory-Constrained Split Computing Framework for Cooperative Inference of Neural Network. *IEEE Transactions on Vehicular Technology*, 2025.
- Generative Diffusion Model-Based Deep Learning Framework for Remaining Useful Life Prediction. *IEEE Internet of Things Journal*, 2025. (공동 제1저자)
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
- **[K-EXAONE 236B MoE 최적화 (Nota AI × LG AI Research × FuriosaAI)](https://blog.nota.ai/newsroom/k-exaone-moe-optimization)** (2026), Quantization Engineer — 성능 저하 구간 정밀 분석 기반 타깃 최적화로 236B MoE 모델을 FuriosaAI 데이터센터 NPU용으로 최적화 — 모델 크기 약 71% 감축, 정확도 약 99.2% 유지 (GPQA 79.80 / IFBench 68.98 / AIME25 88.57).
- **LLM 추론 최적화 (Samsung Challenge)** (2024), Lead Developer — Torch-TensorRT 변환과 메모리 인지 동적 배칭으로 Phi-3 추론 가속 파이프라인 설계.
- **첨단 CNC 공작기계 진단·예지 (한국전기연구원 KERI)** (2023), Lead Developer — 공구 마모 분류, 이상 감지, RUL 예지용 딥러닝 모델 개발 주도.
- **AI 기반 지능형 CCTV (ABB 과제)** (2023), AI Optimization Engineer — LSTR 행동 감지 모델을 엣지 디바이스용으로 최적화 — Knowledge Distillation (TransKD)과 Deep Compression으로 25배 모델 압축.
- **글로벌 기초연구실 (NRF 과제)** (2022), Participating Researcher — IRS 기반 통신 시스템을 위한 딥러닝 채널 추정 (CNN 디노이징, 자기지도학습) 개발.
- **ML 기반 센서 데이터 분석 (JS System 과제)** (2022), Lead Developer — ML 기반 센서 feature-importance 추출 및 모델 성능 최적화 주도.

## Awards
- Best Paper Award, KNU-EE Research Congress (2025) — A Novel VLM-Guided Diffusion Model for Remote Sensing Image Super-Resolution

## Skills
- **연구**: 모델 양자화, KV-cache 압축, 디퓨전/LLM 추론 가속, split computing, 초해상도, 롱컨텍스트 평가
- **프로그래밍**: Python, C++, CUDA C, MATLAB
- **프레임워크·도구**: PyTorch, HuggingFace Transformers, TensorRT, Triton, flash-attn, Docker, Git, LaTeX
- **방법론**: 사전등록, claims ledger, freeze 규율

## Languages
- 한국어: native
- 영어: 비즈니스 회화 가능
