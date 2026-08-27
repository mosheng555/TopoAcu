# TopoAcu

This repository is the data release accompanying the manuscript
*"Meridian topology-aware graph-language alignment for acupuncture prescription
generation"* (submitted to Neurocomputing). It provides de-identified
acupuncture case records drawn from part of the data used in the study.

## Repository content

- `data/acupuncture_cases_complete.jsonl` — 567 de-identified acupuncture case
  records in JSONL format (one JSON object per line). Each record includes the
  case id, source document, demographic descriptor (age, sex), chief complaint,
  medical history, four-diagnostic information (symptoms, tongue, pulse, etc.),
  syndrome differentiation, treatment principle, acupuncture prescription
  (main/adjunct points, needling details, and normalized acupoint names),
  outcome description, and the corresponding topo-cot reasoning trace.

## Data availability

Part of the data used in the study is publicly available here; the full training
corpus of more than 20k case records is **not** included in this release.

The complete corpus was compiled from classical acupuncture texts, modern TCM
literature, teaching cases, and de-identified retrospective case records, and
each record underwent deduplication, anonymization through automated and manual
desensitization, standardization according to WHO acupoint nomenclature,
knowledge-graph whitelist filtering, and narrative conversion into natural
language descriptions. Completing and maintaining this multi-step processing
pipeline for the complete corpus requires substantial ongoing effort, and the
original data sources cannot be fully redistributed.

The released data illustrate the data format and processing outputs. Researchers
interested in the full corpus for research collaboration are welcome to contact
the corresponding author.
