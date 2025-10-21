# ReDoS-Evaluation-Pipeline

## Description
Ce dépôt contient les **résultats complets du pipeline d’évaluation ReDoS** développé dans le cadre de lessai de maîtrise à l’Université du Québec en Outaouais (UQO).  
Il regroupe les étapes de prétraitement, de détection, d’étiquetage et d’analyse statistique des vulnérabilités ReDoS sur trois jeux de données distincts.

## Datasets
Les trois jeux de données étudiés sont :
- **1Regex_before** : expressions régulières avant correction ;
- **Regex_after** : expressions régulières après correction ;
 > Ces deux ensembles précédents proviennent de projets GitHub comportant des vulnérabilités ReDoS recensées dans la base de données **CVEfixes**.  
- **Regexlib** : expressions issues de la base publique **RegexLib**.

- **Regexlib** : expressions issues de la base publique RegexLib.

Chaque dataset comprend :
- la version **cleaned** (regex valides après prétraitement) ;
- la version **to_fix_2.txt** (résultats des outils de détection) ;
- la version **labeled.csv** (étiquetée selon la détection multi-outils).

## Pipeline d’évaluation
Le pipeline suit quatre étapes principales :
1. **Extraction et nettoyage** des regex (sanitization et filtrage syntaxique)  
2. **Détection** des vulnérabilités ReDoS à l’aide des outils : SafeRegex, ReScue, ReDoSHunter, Revealer, RAT  
3. **Étiquetage et regroupement** des regex selon les résultats croisés  
4. **Analyse et visualisation** : UpSet plots, tableaux de résultats et statistiques CVE

Les figures du pipeline et des requêtes SQL associées sont disponibles dans :
- `pipeline_diagram/pipeline_overview.png`
- `pipeline_diagram/ReDoS_SQL_Query.png`
- `pipeline_diagram/ReDoS_Vulnerabilities_Capture.png`

## Analyses disponibles
- `analyses/UPSETCHAR.pdf` : Figures d’UpSet montrant les intersections entre outils de détection  
- `analyses/results_tables.pdf` : Tableaux récapitulatifs (datasets cleaned et détections croisées)  
- `analyses/CVE_ReDoS_Analysis.pdf` : Étude statistique des CVEs liées aux vulnérabilités ReDoS  
- 
## Référence
Les résultats et analyses sont présentés dans l’essai:  
**“DETECTION ET CORRECTION AUTOMATISEES DES VULNERABILITES ReDoS: UNE APPROCHE EMPIRIQUE AU SERVICE DE LA CYBERSECURITE APPLIQUEE”**,  
Ismaël-Yvann Mahassadi, Université du Québec en Outaouais, 2025.


---
© 2025 — ReDoS Evaluation Pipeline | Research Project @ UQO
