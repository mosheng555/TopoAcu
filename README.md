# TopoAcu

This repository is the data release accompanying the manuscript
*"Meridian topology-aware graph-language alignment for acupuncture prescription
generation"* (submitted to Neurocomputing). It provides a representative,
de-identified subset of acupuncture case records to support the reproducibility
of the experimental results reported in the manuscript.

## Repository content

- `data/acupuncture_cases_complete.jsonl` — 567 de-identified acupuncture case
  records in JSONL format (one JSON object per line). Each record includes the
  case id, source document, demographic descriptor (age, sex), chief complaint,
  medical history, four-diagnostic information (symptoms, tongue, pulse, etc.),
  syndrome differentiation, treatment principle, acupuncture prescription
  (main/adjunct points, needling details, and normalized acupoint names),
  outcome description, and the corresponding topo-cot reasoning trace.

## Data availability

As stated in the Data Availability section of the manuscript, only a
representative de-identified subset of several hundred case records is released
here; the full training corpus of more than 20,000 case records is **not**
included in this release.

The complete corpus was compiled from classical acupuncture texts, modern TCM
literature, teaching cases, and de-identified retrospective case records, and
each record underwent deduplication, anonymization through automated and manual
desensitization, standardization according to WHO acupoint nomenclature,
knowledge-graph whitelist filtering, and narrative conversion into natural
language descriptions. Completing and maintaining this multi-step processing
pipeline for the complete corpus requires substantial ongoing effort, and the
original data sources cannot be fully redistributed.

The released subset is therefore sufficient to illustrate the data-processing
pipeline and to validate the proposed approach. Researchers interested in the
full corpus for research collaboration are welcome to contact the corresponding
author.

## Citation

If you use this repository or the data in your research, please cite the
manuscript:

> Wenqiang Zhang, Jinpeng Cui, Miaoqi Zhang, Meng Zhao, Yashuang Mu, Peng Li.
> Meridian topology-aware graph-language alignment for acupuncture prescription
> generation. Submitted to *Neurocomputing*.
