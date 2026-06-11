# Inclusion and Exclusion Criteria

This file documents the inclusion and exclusion criteria used for the PSPR review of datasets used in visual multi-person tracking and re-identification.

## Review scope

The review focuses on publicly available datasets relevant to visual multi-person tracking from a tracking-by-detection perspective. The dataset ecosystem is organized into three main groups:

1. Core multi-person or multi-object tracking benchmarks
2. Auxiliary person/pedestrian detection datasets
3. Auxiliary person re-identification or person-search datasets

The review prioritizes literature and benchmark resources from **2005 onward** and was prepared for the manuscript revision in **June 2026**.

## Inclusion criteria

A dataset was considered for inclusion if it satisfied at least one of the following conditions:

- It is a public benchmark directly used for evaluating multi-person or multi-object tracking, including single-camera, multi-camera, crowded-scene, sports, long-term, synthetic, driving-scene, or surveillance tracking scenarios.
- It is a person or pedestrian detection dataset commonly used to train, fine-tune, or evaluate detectors in tracking-by-detection studies.
- It is a person Re-ID, video Re-ID, or person-search dataset commonly used to learn identity-discriminative appearance representations or association models for identity preservation in tracking pipelines.
- It provides sufficient technical documentation to identify the task definition, dataset scope, annotation type, evaluation protocol, and intended benchmark use.
- It is described in an English-language journal, conference, workshop, challenge paper, authoritative preprint, or official dataset/benchmark webpage.

## Exclusion criteria

Datasets were excluded if they met any of the following conditions:

- The dataset is private, inaccessible, or insufficiently documented for extracting core dataset properties.
- The publication is method-only and does not introduce a dataset or provide substantial dataset characterization.
- The dataset is a generic object dataset with no clear or established role in multi-person tracking, pedestrian detection, person Re-ID, person search, or tracking-by-detection pipelines.
- The source is non-English.
- The source was published before the selected review window, unless it was indispensable for historical context.
- The same dataset family was described in multiple duplicate publications; in such cases, the canonical source or most relevant official benchmark paper was retained.
- The dataset belongs to unrelated modalities or applications and its relevance to person-tracking pipelines cannot be clearly justified.

## Counting convention

The repository follows the manuscript table organization and contains **37 dataset-role entries**:

- 8 detection-support entries
- 9 person Re-ID/person-search entries
- 20 core tracking benchmark entries

Because WILDTRACK/WildTrack is discussed in both detection-support and core tracking contexts, the unique dataset count is **36** if repeated role entries are merged.

## Notes for reuse

This repository does not redistribute original datasets. It provides curated metadata, official links, search information, and PSPR-based interpretation only. Users must follow the license, access, and ethical-use conditions of each original dataset.
