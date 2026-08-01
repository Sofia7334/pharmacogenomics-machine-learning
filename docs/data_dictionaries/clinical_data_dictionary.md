# Clinical Variants Data Dictionary

**Project:** Pharmacogenomics Machine Learning

## Dataset Summary
**Dataset:** clinicalVariants.tsv
**File Type:** TSV
**Description:** This file contains a list of variant-drug pairs and the level of evidence for each association.
**Source:** ClinPGx
**Records:** 5,190 entries
**Features:** 6 columns
**License:** (Reference the DATA_LICENSE.md from ClinPGx.)

| Column | Data Type | Description | Example | Missing Values | Notes |
|:-------|:---------:|:-----------:|:-------:|:--------------:|:------|
| variant | Text | Name or symbol of the variant | CYP3A5*1, CYP3A5*3 | None | Haplotype-based star(*) system and reference SNP cluster IDs (rIDs) |
| gene | Categorical | Gene associated with the variant | CYP2C9 | Yes | HGNC ID of the gene |
| type | Categorical | Category or categories that the annotation falls in | Metabolism/PK | None | Aspect of drug therapy affected by variant |
| level of evidence | Ordinal Categorical | Strength of the evidence for the annotation | 1A | None | Primarily informed by the ClinPGx annotation scoring systems |
| chemicals | Text | Drug(s) associated with the variant in the annotation | warfarin | None | From the ClinPGx drug vocabulary |
| phenotypes | Text | Associated disease phenotype(s), where applicable | Neoplasms | Yes | Multiple values possible |

## Data Quality Notes
- Asses variant naming conventions.
- Verify capitalization consistency.
- Check for multiple drugs stored in one field.
- Check for multiple phenotypes stored in one field.