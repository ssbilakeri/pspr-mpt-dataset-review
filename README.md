PSPR Multi-Person Tracking Dataset Review
This repository contains curated metadata and supplementary resources for the review manuscript:
From Detection to Identity Preservation: A PSPR Review of Datasets for Visual Multi-Person Tracking and Re-Identification
The review analyzes public datasets used across the visual multi-person tracking pipeline, including detection-support datasets, person re-identification/person-search datasets, and core tracking benchmarks. The repository is intended to improve transparency, discoverability, and reproducibility of the dataset review.
> **Note:** This repository does **not** redistribute the original datasets. It only provides curated metadata, review tables, search information, benchmark links, protocol summaries, and visualization resources.
---
Review scope
The review follows a tracking-by-detection perspective, where multi-person tracking is treated as a pipeline involving:
Person detection and localization
Person re-identification and appearance modelling
Data association and identity preservation
Trajectory generation and benchmark evaluation
The manuscript introduces the Pipeline–Scenario–Protocol–Readiness (PSPR) framework to analyze datasets according to:
Pipeline role: detector training, Re-ID training, person search, single-camera tracking, multi-camera tracking, long-term tracking, or synthetic training
Scenario complexity: occlusion, crowd density, camera motion, viewpoint change, small objects, nonlinear motion, long-term re-entry, and related visual challenges
Evaluation protocol: public/private detection settings, detection metrics, Re-ID metrics, tracking metrics, single-camera and multi-camera protocols
Deployment readiness: relevance to surveillance, traffic, autonomous driving, UAV/aerial monitoring, sports, campus, synthetic, open-world, or adverse-condition settings
Benchmark limitation: missing identity continuity, limited adverse-condition coverage, lack of multimodal data, weak long-term evaluation, open-set limitations, or restricted annotation richness
---
Dataset coverage
The curated review currently includes 37 public datasets, grouped as follows:
Dataset group	Count	Purpose
Detection-support datasets	8	Datasets mainly used for detector training or pedestrian localization before tracking
Person Re-ID/person-search datasets	9	Datasets used for identity-discriminative appearance learning, person retrieval, or detector-aware identity modelling
Core tracking benchmarks	20	Datasets used for trajectory-level evaluation, identity preservation, association robustness, multi-camera tracking, dense-crowd tracking, long-term tracking, sports tracking, driving-scene tracking, or synthetic tracking
The review prioritizes literature from 2005 onward. The current repository version records the curated metadata prepared for the manuscript revision in June 2026.
---
Repository contents
```text
pspr-mpt-dataset-review/
│
├── README.md
├── LICENSE
├── CITATION.cff
├── CHANGELOG.md
│
├── metadata/
│   ├── datasets_master.csv
│   ├── pspr_annotations.csv
│   ├── dataset_category_summary.csv
│   └── data_dictionary.md
│
├── search_strategy/
│   ├── search_strings.csv
│   ├── database_search_summary.csv
│   └── final_search_update.md
│
├── screening/
│   ├── screening_table.csv
│   ├── inclusion_exclusion_criteria.md
│   └── screening_summary.csv
│
├── benchmark_resources/
│   ├── official_dataset_links.csv
│   ├── benchmark_metrics_summary.csv
│   ├── benchmark_protocol_summary.csv
│   └── dataset_limitations_summary.csv
│
├── scripts/
│   ├── create_dataset_summary_tables.py
│   ├── create_pspr_summary.py
│   └── create_conceptual_difficulty_map.py
│
└── figures/
    ├── conceptual_difficulty_map.png
    └── conceptual_difficulty_map_source.csv


Contact
For questions about this repository or the associated review, contact the corresponding author listed in the manuscript.
