# dias_TWE_config_GRCh37_v3.0.3.json

This repo contains a JSON config file which is used with eggd_dias_batch to specify inputs for running the Dias pipeline for TWE data.

## What does the config do?
eggd_dias_batch ([https://github.com/eastgenomics/eggd_dias_batch](https://github.com/eastgenomics/eggd_dias_batch)) is a DNAnexus app that runs the Dias pipeline for germline sequence data analysis. The egg4_dias_TWE_config repo contains the dias_TWE_config file that specifies the executables and their input files to be used in the Dias pipeline for analysing TWE data on build GRCh37.

New versions of apps and app inputs for use in the Dias pipeline can be updated in the config without needing to update the pipeline itself.

## Parts of the config
The config specifies app IDs and workflow IDs at the top, followed by a `reference_files` dict for inputs that could be used in multiple running modes. The `modes` section specifies inputs specific to a running mode. The TWE config currently only has one running mode:
* dias_reports
    * specifies the inputs for dias_reports.

## Versions of workflows and dynamic files in the config
Workflows:
* Dias reports: **dias_reports_v2.1.1**
    * DNAnexus workflow ID: ``

Dynamic files:
| File      | File name | DNAnexus file ID |
| --------- | --------- | ---------------- |
| genepanels | **240213_genepanels.tsv** | `file-GgBG75Q433Gk4pY5qpxbgVyz` |
| exons_nirvana | **GCF_000001405.25_GRCh37.p13_genomic.exon_5bp_v2.0.0.tsv** | `file-GF611Z8433Gk7gZ47gypK7ZZ` |
| genes2transcripts | **240213_g2t.tsv** | `file-GgBG6p8433Gg7XK69fG7P9j7` |
| panel_dump for eggd_optimised_filtering | **240202_panelapp_dump.json** | `file-Gg35Vf845B5bV08VqJ0qGV5V` |
| exons_file for eggd_athena | **GCF_000001405.25_GRCh37.p13_genomic.symbols.exon_5bp_v2.0.0.tsv** | `file-GF611Z8433Gf99pBPbJkV7bq` |
| twe_vep_config for SNV reports | **twe_vep_config_v1.1.13.json** | `file-GgBz84Q4j4fZYV62y0XXG02g` |
