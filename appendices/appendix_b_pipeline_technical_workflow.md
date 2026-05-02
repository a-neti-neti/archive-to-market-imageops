# Appendix B - Pipeline and Technical Workflow

## 1. Archive intake

**Purpose:** keep originals untouched and make the archive addressable.

**Scripts:**

- `03_scripts/image_scan/inventory_images.py`

**Main folders / files:**

- `source/`
- `01_data/folder_inventory.csv`
- `01_data/photos_inventory_generated.csv`

**Produced outputs:**

- generated image inventory;
- folder / file counts;
- path-level archive map.

## 2. Decision schema setup

**Purpose:** define what must be judged per image.

**Main files:**

- `01_data/photos_master.csv`
- `01_data/lanes_master.csv`
- `01_data/technical_defects.csv`
- `01_data/tool_routing.csv`
- `01_data/material_routing.csv`
- `01_data/authenticity_matrix.csv`
- `01_data/series_candidates.csv`

**Supporting docs:**

- `00_docs/lane_taxonomy.md`
- `00_docs/photo_taxonomy.md`
- `00_docs/scoring_rubric.md`
- `00_docs/processing_pipeline.md`
- `00_docs/material_decision_matrix.md`

**Produced outputs:**

- working decision backbone;
- scoring structure;
- lane and defect taxonomy.

## 3. Working copies and sampling

**Purpose:** create safe subsets and flat experiments without touching originals.

**Scripts:**

- `03_scripts/image_scan/copy_source_to_experiment.py`

**Main folders / files:**

- `02_images/sample_batch/`
- `02_images/selected/`
- `02_images/working/`
- `02_images/working/unsorted_cluster_experiment_2026-04-29/flat_images/flat_copy_manifest.csv`

**Produced outputs:**

- sample batches;
- selected subsets;
- flat-copy experiment sets.

## 4. First-pass technical diagnostics

**Purpose:** generate machine-readable review cues before scoring.

**Scripts:**

- `03_scripts/image_analysis/analyze_folder_batch.py`

**Main folders / files:**

- `01_data/series_diagnostics/`
- `04_outputs/reports/first10_diagnostics_2026-04-30.csv`
- `04_outputs/reports/first10_diagnostics_contact_sheet_2026-04-30.jpg`

**Produced outputs:**

- diagnostics CSVs;
- contact sheets;
- technical flags;
- impact proxy scores.

## 5. Material / support routing

**Purpose:** connect technical condition to output-surface logic.

**Scripts:**

- `03_scripts/image_analysis/material_decision_engine.py`
- `03_scripts/image_analysis/apply_material_decisions_to_csv.py`
- `03_scripts/image_analysis/merge_material_suggestions_into_master.py`

**Main folders / files:**

- `00_docs/material_decision_matrix.md`
- `00_docs/print_surface_guidance.md`
- `01_data/material_routing.csv`

**Produced outputs:**

- first-pass substrate recommendations;
- rerouted material decisions;
- merged material fields for master CSVs.

## 6. Repair / authenticity routing

**Purpose:** decide what kind of intervention is acceptable before any serious repair.

**Main files:**

- `00_docs/authenticity_rules.md`
- `00_docs/local_first_image_repair_pipeline.md`
- `00_docs/ai_image_repair_stack_2026-04-25.md`
- `01_data/tool_routing.csv`
- `01_data/authenticity_matrix.csv`

**Utility script:**

- `03_scripts/image_repair/check_imageops_env.py`

**Produced outputs:**

- repair pathways;
- authenticity constraints;
- tool-choice logic;
- environment readiness check.

## 7. Semantic grouping / clustering

**Purpose:** recover structure when folders are incomplete or too noisy.

**Scripts:**

- `03_scripts/tagging/cluster_flat_images.py`
- `03_scripts/tagging/cluster_flat_images_semantic.py`
- `03_scripts/tagging/cluster_cached_embeddings_hdbscan.py`
- `03_scripts/tagging/cluster_cached_embeddings_umap_hdbscan.py`

**Main folders / files:**

- `02_images/working/unsorted_cluster_experiment_2026-04-29/semantic_clustering_clip_vitb32_full/`
- `02_images/working/unsorted_cluster_experiment_2026-04-29/semantic_clustering_siglip2_base_patch16_224_full_2026-04-30/`
- `02_images/working/unsorted_cluster_experiment_2026-04-29/semantic_hdbscan_*/`
- `02_images/working/unsorted_cluster_experiment_2026-04-29/semantic_umap_hdbscan_*/`

**Produced outputs:**

- cluster summaries;
- cluster assignments;
- embedding caches;
- contact sheets;
- noise-review sets;
- UMAP review maps.

## 8. Human naming and series extraction

**Purpose:** turn machine groupings into usable curatorial families.

**Main files:**

- `semantic_cluster_naming_template.csv`
- `umap_hdbscan_cluster_naming_template.csv`
- `umap_hdbscan_cluster_naming_first_pass_codex_2026-04-30.csv`

**Produced outputs:**

- human-readable cluster names;
- series candidates;
- split / merge review notes.

## 9. Lane mapping

**Purpose:** connect images and series to actual commercial or editorial routes.

**Main files:**

- `00_docs/lane_taxonomy.md`
- `00_docs/outreach_positioning.md`
- `01_data/lanes_master.csv`
- `01_data/series_candidates.csv`

**Produced outputs:**

- lane fit logic;
- sublane ideas;
- positioning guidance.

## 10. Research / OSINT

**Purpose:** validate real-world channels, targets, and route fit.

**Main files:**

- `05_research/research_queue.md`
- `05_research/community_cultural_targets/`
- `06_sales_assets/outreach/outreach_protocol_notes.md`

**Produced outputs:**

- target lists;
- outreach logic;
- route-specific notes;
- market / context validation.

## 11. Sales / website / outreach assets

**Purpose:** translate the internal system into outward-facing materials.

**Main files:**

- `06_sales_assets/outreach_templates/`
- `06_sales_assets/website_copy/site_structure_first_pass.md`
- `00_docs/website_platform_recommendation_2026-04-25.md`

**Produced outputs:**

- outreach drafts;
- website structure;
- platform recommendation;
- communication assets.

## 12. Reports and handoffs

**Purpose:** preserve findings and turn work into reusable artifacts.

**Main folders / files:**

- `04_outputs/reports/`

**Produced outputs:**

- review memos;
- handoff bundles;
- article support materials.
