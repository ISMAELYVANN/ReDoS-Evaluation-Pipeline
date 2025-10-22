# ReDoS-Evaluation-Pipeline

## Description (Français)
Ce dépôt contient les **résultats complets du pipeline d’évaluation ReDoS** développé dans le cadre de l’essai de maîtrise à l’Université du Québec en Outaouais (UQO).  
Il regroupe les étapes de **prétraitement**, de **détection**, d’**étiquetage** et d’**analyse statistique** des vulnérabilités ReDoS sur trois jeux de données distincts.

---

##  Description (English)
This repository contains the **complete results of the ReDoS evaluation pipeline**, developed as part of a Master’s thesis at the Université du Québec en Outaouais (UQO).  
It includes all stages of **preprocessing**, **vulnerability detection**, **labeling**, and **statistical analysis** of ReDoS vulnerabilities across three different datasets.

---

##  Datasets
The three analyzed datasets are:

- **Regex_before**: Regular expressions before correction  
- **Regex_after**: Regular expressions after correction  
  > These two datasets come from vulnerable GitHub projects listed in the **CVEfixes** database.  
- **Regexlib**: Regular expressions collected from the public **RegexLib** repository  

Each dataset includes:
- a **cleaned** version (valid regex after preprocessing);  
- a **to_fix_2.txt** version (detection tool outputs);  
- a **labeled.csv** version (labeled from multi-tool detection results);  
- and the **raw datasets** `regex_before.txt`, `regex_after.txt`, and `regexlib_onlyregex.txt` for full pipeline traceability.

---

## Pipeline d’évaluation / Evaluation Pipeline
The ReDoS evaluation pipeline consists of four main steps:

1. **Extraction and cleaning** of regular expressions (sanitization and syntax filtering)  
2. **Detection** of ReDoS vulnerabilities using the tools:  
   `SafeRegex`, `ReScue`, `ReDoSHunter`, `Revealer`, and `RAT`  
3. **Labeling and aggregation** of regex patterns based on cross-tool results  
4. **Analysis and visualization** through UpSet plots, intersection matrices, summary tables, and CVE-based statistics  

Figures illustrating the pipeline and SQL queries:
- `pipeline_diagram/pipeline_overview.png`
- `pipeline_diagram/ReDoS_SQL_Query.png`
- `pipeline_diagram/ReDoS_Vulnerabilities_Capture.png`

---

## Analyses disponibles / Available Analyses
- `analyses/UPSETCHAR.pdf` — UpSet figures showing detection intersections  
- `analyses/results_tables.pdf` — Summary tables (cleaned datasets and cross-tool detections)  
- `analyses/CVE_ReDoS_Analysis.pdf` — Statistical analysis of CVEs related to ReDoS vulnerabilities  
- `analyses/redos_summary_filtered.json` — Filtered summary of ReDoS vulnerabilities from the NVD feeds  
- `analyses/summary_statistics.csv` — Consolidated numerical data  

---

## Matrices d’intersection / Intersection Matrices
The intersection matrices provide a **cross-analysis** of detection results from different ReDoS tools.  
They highlight areas of **agreement** and **divergence** between static and dynamic analysis approaches, offering a synthetic view of detection consistency.

Files available:
- `analyses/intersection_matrix_regex_before.csv` — Cross results for **Regex_before** dataset  
- `analyses/intersection_matrix_regex_after.csv` — Cross results for **Regex_after** dataset  
- `analyses/intersection_matrix_regexlib.csv` — Cross results for **RegexLib** dataset  

Each matrix reports, for every tool, the number of detected vulnerable regexes and multi-tool overlaps (double, triple, or quadruple detections).

---

## Référence / Reference
Les résultats et analyses sont présentés dans l’essai de maîtrise :  
**“Détection et correction automatisées des vulnérabilités ReDoS : une approche empirique au service de la cybersécurité appliquée.”**  
_Ismaël-Yvann Mahassadi_, Université du Québec en Outaouais, 2025.

Results and analyses are detailed in the Master’s thesis:  
**“Automated Detection and Correction of ReDoS Vulnerabilities: An Empirical Approach to Applied Cybersecurity.”**  
_Ismaël Yvann Mahassadi_, Université du Québec en Outaouais, 2025.

---

© 2025 — **ReDoS Evaluation Pipeline** | Research Project @ UQO  
