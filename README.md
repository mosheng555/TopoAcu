# TopoAcu

This repository provides the accompanying data and model implementation details for the TopoAcu project.

## Model & Backbone Configurations

TopoAcu decouples acupoint entity semantics from meridian-relation topology alignment via a multi-stage curriculum. The model configurations across different backbone architectures are as follows:

- **Primary Backbone (Main Results & Ablations):**
  - Base Model: `Qwen/Qwen2.5-7B-Instruct`
  - Adaptation: LoRA (rank $r = 8$, alpha $\alpha = 16$) applied to projection layers in self-attention and feed-forward networks.
  - Training Pipeline: Stage 0 (graph pre-training) followed by Stage 1 (pure SFT) and Stage 2 (topological alignment with linear curriculum loss warmup).

- **Secondary Backbone (Cross-Architecture Generalization):**
  - Base Model: `meta-llama/Meta-Llama-3.1-8B-Instruct`
  - Used for backbone-agnostic validation to assess latent structural probing and strong generalization across unseen graph edges.

## Repository Content

data_case.jsonl — De-identified acupuncture case records in JSONL format (one JSON object per line). Each record includes the case id, source document, demographic descriptor (age, sex), chief complaint, medical history, four-diagnostic information (symptoms, tongue, pulse, etc.), syndrome differentiation, treatment principle, acupuncture prescription (main/adjunct points, needling details, and normalized acupoint names), outcome description, and the corresponding topo-cot reasoning trace.

## Data Availability

Part of the data used in the study is publicly available here; the full training corpus of more than 20k case records is **not** included in this release.

The complete corpus was compiled from classical acupuncture texts, modern TCM literature, teaching cases, and de-identified retrospective case records, and each record underwent deduplication, anonymization through automated and manual desensitization, standardization according to WHO acupoint nomenclature, knowledge-graph whitelist filtering, and narrative conversion into natural language descriptions. Completing and maintaining this multi-step processing pipeline for the complete corpus requires substantial ongoing effort, and the original data sources cannot be fully redistributed.

The released data illustrate the data format and processing outputs. Researchers interested in the full corpus for research collaboration are welcome to contact the corresponding author.
