# Data Anonymization & Privacy Analysis

This project explores data anonymization and privacy protection using the **Adult dataset**, a demographic and socio-economic dataset commonly used for evaluating anonymization techniques.

The work was developed using the **ARX Data Anonymization Tool**, focusing on the application of privacy models, re-identification risk assessment and data utility analysis.

## Project Overview

The main objective was to evaluate how different anonymization configurations affect the balance between individual privacy and data utility.

The project involved analyzing the dataset attributes, defining generalization hierarchies, applying privacy models and comparing the resulting anonymized datasets against the original data.

## Attribute Classification

The dataset attributes were classified according to their privacy relevance:

- **Quasi-Identifiers:** Age, workclass, education, marital status, occupation, race, sex and native country.
- **Sensitive Attribute:** Income.
- **Insensitive Attributes:** Education-number, relationship, fnlwgt, capital-gain and capital-loss.
- **Identifying Attributes:** No direct identifying attributes were identified.

Generalization hierarchies were defined for the quasi-identifiers to support the anonymization process.

## Privacy Models

Two privacy configurations were implemented and evaluated, both incorporating k-anonymity:

**Model 1 – k-Anonymity + l-Diversity**

Applied with l = 2, ensuring that each equivalence class contains at least two distinct values of the sensitive attribute (income).

Different k values (5, 10, 25 and 50) and suppression limits (5%, 10% and 15%) were tested to evaluate their impact on privacy and utility.

**Model 2 – k-Anonymity + t-Closeness**

Applied with t = 0.5, limiting the difference between the distribution of the sensitive attribute within each equivalence class and its global distribution.

The same experimental approach was used to compare different k values and suppression limits.

## Risk & Utility Analysis

The anonymization results were evaluated using ARX privacy risk and data utility metrics.

**Privacy Risk Metrics:**
- Average Prosecutor Risk
- Highest Prosecutor Risk
- Estimated Prosecutor Risk
- Records Affected by Highest Risk

**Data Utility Metrics:**
- Granularity
- Normalized Entropy
- Discernibility

The experiments included comparisons against the original dataset and visual analysis of how different anonymization parameters affected privacy and information preservation.

## Results & Conclusions

Both privacy models significantly reduced re-identification risk compared with the original dataset.

The analysis indicated that **t-closeness provided a more favorable balance between privacy and utility** for the Adult dataset.

Two configurations stood out:

- **k = 10, suppression = 10%:** A favorable balance between data utility and privacy protection.
- **k = 25, suppression = 10%:** Lower re-identification risk, with a moderate reduction in data utility.

The results highlight the importance of selecting anonymization parameters according to the desired balance between privacy protection and information preservation.

## Tools & Technologies

- ARX Data Anonymization Tool
- Adult Dataset
- CSV
- Data Privacy & Anonymization
- Privacy Risk Assessment
- Data Utility Analysis

## Project Files

- **Assignment3.pdf:** Original project assignment.
- **Trabalho_SP3.pdf:** Final project report, including attribute classification, methodology, results and conclusions.
- **.deid files:** Anonymization project files for the l-diversity and t-closeness configurations.
- **CSV files:** Original dataset and consolidated experimental results.
- **PNG files:** Risk and utility analysis visualizations.
