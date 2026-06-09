# Data Dictionary

This document defines the fields used in the curated metadata files for the PSPR multi-person tracking dataset review repository.

The repository follows the manuscript's table organization. The main metadata file contains **37 dataset-role entries**. Because WILDTRACK/WildTrack is discussed in both detection-support and core tracking contexts, the **unique dataset count is 36** if that repeated role entry is merged.

Fields marked as `Not specified in manuscript` were not explicitly reported in the reviewed manuscript text or tables and should be verified from the official dataset source before being used for numerical comparison.

---

## `metadata/datasets_master.csv`

One row is provided for each dataset-role entry discussed in the manuscript tables.

| Column | Description |
|---|---|
| `dataset_id` | Repository-specific identifier. Prefix `D` = detection-support, `R` = Re-ID/person-search, `T` = core tracking benchmark. |
| `dataset_name` | Dataset or benchmark name. |
| `dataset_category` | Broad category used in the review: detection-support dataset, person Re-ID/person-search dataset, or core tracking benchmark. |
| `subcategory` | More specific role or scenario grouping. |
| `year` | Dataset release/publication year when available from the manuscript or commonly established benchmark identity; otherwise marked as not specified. |
| `primary_reference` | Dataset or benchmark reference name. |
| `citation_key` | Manuscript reference number placeholder, formatted as `manuscript_ref_X`. |
| `doi_or_arxiv` | DOI/arXiv identifier when included or easily traceable; left blank where not recorded. |
| `official_dataset_url` | Official dataset, challenge, or project URL when available. Some historical or retired datasets are marked with access notes instead of direct URLs. |
| `task_type` | Main computer-vision task associated with the dataset. |
| `pipeline_role` | Role in the tracking-by-detection pipeline. |
| `domain_or_scene_type` | Main visual domain or scenario represented by the dataset. |
| `camera_setting` | Camera configuration, such as image-level, single-camera, multi-camera, moving-camera, or surveillance setting. |
| `modality` | Data modality, usually RGB image/video, with notes for synthetic, segmentation, or sensor-rich datasets. |
| `number_of_images_or_frames` | Number of images/frames when recorded; otherwise `Not specified in manuscript`. |
| `number_of_videos_or_sequences` | Number of videos/sequences when recorded; otherwise `Not specified in manuscript`. |
| `number_of_identities` | Number of identities when recorded; otherwise `Not specified in manuscript` or `Not applicable`. |
| `annotation_type` | Type of annotations available, such as boxes, masks, identities, tracklets, trajectories, or person-search labels. |
| `evaluation_metrics` | Typical evaluation metrics or protocols associated with the dataset. |
| `public_private_detection_protocol` | Whether a public/private detection protocol, query-gallery protocol, or benchmark-specific protocol applies. |
| `main_challenge` | Dominant difficulty or challenge captured by the dataset. |
| `best_suited_for` | Practical use of the dataset in multi-person tracking research. |
| `key_limitation` | Main limitation identified from the PSPR interpretation. |
| `access_status` | Current high-level access note. Authors should verify access before final archival release. |
| `license_or_usage_notes` | Reminder to follow the original dataset license and usage terms. |
| `included_in_manuscript_table` | Manuscript table in which the dataset appears. |
| `notes` | Additional clarification, including duplicate role-entry notes. |

---

## `metadata/pspr_annotations.csv`

This file records the PSPR-based interpretation of each dataset-role entry.

| Column | Description |
|---|---|
| `dataset_id` | Repository-specific identifier matching `datasets_master.csv`. |
| `dataset_name` | Dataset or benchmark name. |
| `pipeline_role` | Functional role in the tracking-by-detection pipeline. |
| `scenario_complexity` | Main visual or temporal difficulty captured by the dataset. |
| `evaluation_protocol` | Metrics or benchmark protocol relevant to the dataset. |
| `deployment_readiness` | Practical deployment scenario represented by the dataset. |
| `benchmark_limitation` | What the dataset does not adequately test. |
| `pspr_comment` | Short interpretation explaining the dataset's role in the review. |

---

## `metadata/dataset_category_summary.csv`

This file summarizes dataset-role counts by category.

| Column | Description |
|---|---|
| `dataset_category` | Dataset group or count type. |
| `count` | Number of entries in that group. |
| `description` | Explanation of the group and counting convention. |

---

## `search_strategy/search_strings.csv`

This file documents the search strings used to identify dataset and benchmark sources.

| Column | Description |
|---|---|
| `database` | Scholarly or benchmark source searched. |
| `date_searched` | Date of final revision search/update. |
| `search_string` | Search phrase used. |
| `filters_used` | Filters applied, such as date range, language, public dataset, or task scope. |
| `number_of_records_found` | Record count if documented. If not recorded, marked as not reported. |
| `notes` | Clarifying note on search purpose. |

---

## `screening/inclusion_exclusion_criteria.md`

Markdown file describing the inclusion and exclusion criteria used in the dataset review.

---

## `benchmark_resources/official_dataset_links.csv`

This file lists available dataset, benchmark, paper, and access links.

| Column | Description |
|---|---|
| `dataset_id` | Repository-specific identifier matching `datasets_master.csv`. |
| `dataset_name` | Dataset or benchmark name. |
| `official_url` | Official dataset/project/benchmark URL when available. |
| `benchmark_url` | Benchmark or leaderboard URL when different from official URL. |
| `paper_url` | Paper or project reference URL when official dataset URL is unavailable or uncertain. |
| `access_status` | High-level access note. |
| `license_or_usage_notes` | Reminder to follow original usage terms. |
| `last_checked` | Date of repository preparation/check. |
| `notes` | Additional access or verification comments. |

---

## `benchmark_resources/dataset_limitations_summary.csv`

This file summarizes dataset-level limitations identified using the PSPR interpretation.

| Column | Description |
|---|---|
| `dataset_name` | Dataset or benchmark name. |
| `dataset_category` | Dataset group used in the review. |
| `main_limitation` | Main limitation associated with the dataset. |
| `affected_pipeline_stage` | Tracking pipeline stage most affected by the limitation. |
| `implication_for_tracking` | Why the limitation matters for multi-person tracking. |
| `future_dataset_requirement` | Suggested future dataset requirement or improvement. |
