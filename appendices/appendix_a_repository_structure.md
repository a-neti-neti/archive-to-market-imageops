# Appendix A - Repository Structure

```text
/
├── 00_docs
│   ├── authenticity_rules.md
│   ├── fixability_rules.md
│   ├── lane_taxonomy.md
│   ├── local_first_image_repair_pipeline.md
│   ├── material_decision_matrix.md
│   ├── outreach_positioning.md
│   ├── photo_taxonomy.md
│   ├── print_surface_guidance.md
│   ├── processing_pipeline.md
│   ├── scoring_rubric.md
│   └── technical_issues.md
├── 01_data
│   ├── series_diagnostics
│   ├── authenticity_matrix.csv
│   ├── folder_inventory.csv
│   ├── lanes_master.csv
│   ├── material_routing.csv
│   ├── photos_inventory_generated.csv
│   ├── photos_master.csv
│   ├── technical_defects.csv
│   └── tool_routing.csv
├── 02_images
│   ├── previews
│   ├── sample_batch
│   ├── selected
│   └── working
├── 03_scripts
│   ├── exports
│   ├── image_analysis
│   │   ├── analyze_folder_batch.py
│   │   ├── apply_material_decisions_to_csv.py
│   │   ├── material_decision_engine.py
│   │   └── merge_material_suggestions_into_master.py
│   ├── image_repair
│   ├── image_scan
│   └── tagging
├── 04_outputs
│   ├── exports
│   ├── proposals
│   ├── reports
│   └── shortlist
├── 05_research
│   ├── direct_sales
│   ├── editorial_licensing
│   ├── environmental_graphics
│   ├── interior_b2b
│   ├── community_cultural_targets
│   ├── low_tier_mass
│   ├── pod_marketplaces
│   ├── prestige_signal
│   ├── productized_art
│   └── research_queue.md
├── 06_sales_assets
│   ├── outreach
│   ├── outreach_templates
│   ├── product_descriptions
│   └── website_copy
├── source
├── .gitignore
├── AGENTS.md
├── README.md
└── requirements-imageops.txt
```
