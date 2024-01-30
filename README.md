# PubMed Data Analysis for Case Reports on Renal Anomalies

**Paper Under Review**
- **Journal**: Radiology Case Reports
- **Corresponding Author**: Mirsadra Molaei
- **First Author**: Roseminasadat Moulaei
- **Date of Submission**: 13th October 2023
- **Manuscript Number**: RCR-D-23-01504

This repository contains analysis and documentation related to a case report focused on renal anomalies, specifically the L-shaped renal ectopia.

## Requirements

The analysis is based on Google Colab, and requires the following packages:

```bash
!pip install biopython

from Bio import Entrez
import pandas as pd
import re
```

## Data Fetching

Data fetched from PubMed is structured into a dataframe with the following columns:

- **Authors**: List of authors associated with the publication.
- **Title**: Title of the publication.
- **Abstract**: Abstract text of the publication.
- **Language**: Language in which the publication is written.
- **Year**: Year of publication.
- **Keywords**: Keywords associated with the publication.
- **Type**: Type of the article, e.g., case report, review, etc.

This structured dataframe allows for efficient querying and data manipulation to extract relevant information for our case report analysis.

## Queries

To retrieve relevant case reports from PubMed, the following queries were utilized:

- **Query 1 (For Table 1):** `L-shaped renal ectopia OR L-shaped crossed renal ectopia OR L-shaped crossed fused AND Case Reports[PT]`
- **Query 2 (For Table 2):** `single ureter AND crossed-fused AND Case Reports[PT]`

## Manual Data Adjustment
### **Tokgöz et al Case Report**  
Tokgöz et al presented two L-shaped CFRE cases in one case report. We've duplicated the second case for clarity.
### **Additional Case Details**
Manual additions were made to include case presentation details that were not fetched directly from the queries.
### **Data Filtration**
During our first pass of data filtration, we focused on ensuring the relevance and applicability of the cases to our study. Specifically, we filtered out:

- **Cases without Case Presentation:** Records that did not provide detailed case presentations were excluded as they lacked the depth and clarity required for our analysis.

- **Non-human reports:** Reports or case studies that were based on non-human subjects, such as cats, were excluded to maintain the focus on human clinical findings and implications.

This initial filtration step was crucial to ensure that our dataset was tailored to provide meaningful insights for our research objectives.


### **Custom Table Creation**

## Further Data Clearance

After our initial data retrieval and processing, we further refined our dataset by excluding certain records. The reasons for these exclusions, based on the PMID (PubMed ID), are detailed below:

- **PMID 28603157:** This was a dissection report and not directly relevant to our analysis.
  
- **PMID 33194464:** The case did not involve a `single` ureter.
  
- **PMID 26252333:** This case described a duplex kidney and was not a CFRE (Crossed Fused Renal Ectopia) case.
  
- **PMID 10806577:** This Japanese case was excluded due to the lack of a DOI (Digital Object Identifier) and the manuscript being inaccessible.
  
- **PMID 2678982:** The K Arai et al case from 1989 was excluded because of missing DOI and inaccessible manuscript.
  
- **PMID 1159928:** Although this report mentioned CFRE and a single ureter, it did not specify the type. The description closely resembled that of a duplex kidney, so it was deemed not fitting for our analysis.

These clearance steps ensure that our dataset is both accurate and relevant to the focus of our research.


### Manual Data Entry

A specific manual entry was made based on the following source:

> Türkvatan A, Olçer T, Cumhur T. _Multidetector CT urography of renal fusion anomalies_. Diagn Interv Radiol. 2009 Jun;15(2):127-34.

From this source, we extracted a notable case detail: A 23-year-old male diagnosed with L-shaped CFRE.

This manual intervention ensures that even data points not captured through our automated processes are adequately represented in our analysis.
