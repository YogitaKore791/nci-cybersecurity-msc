# Digital Forensics and eDiscovery — CA2

### Machine Learning \& Data Analytics in Digital Forensics and eDiscovery

\---

## Assignment Details

|Field|Details|
|-|-|
|**Module**|Forensics and eDiscovery|
|**Assessment**|Continuous Assessment 2 (CA2) — 60% of module|
|**College**|National College of Ireland|
|**Programme**|MSc Cybersecurity|
|**Semester**|Semester 1 — 2025/2026|

\---

## Objective

This report investigates how **Machine Learning (ML) and Data Analytics** are applied in **Digital Forensics and eDiscovery**, specifically:

* How ML and AI reduce document review time from months to weeks
* How these technologies integrate with the **EDRM (Electronic Discovery Reference Model)** framework
* Comparing advantages and disadvantages of ML techniques vs manual review
* Understanding algorithms like NLP, TAR, CAL, and near-duplicate detection

\---

## Key Findings

* **CAL (Continuous Active Learning)** achieves 90-95% recall while requiring humans to review only 1-2% of the full document collection
* **NLP techniques** (TF-IDF, BERT transformers) convert raw text into structured data machines can analyse
* **Near-duplicate detection** using shingling and MinHash removes repeated content efficiently across millions of documents
* **Email threading** reduces document volume by grouping conversations so reviewers focus only on inclusive messages
* ML in **cybersecurity** is less standardised than legal TAR — fewer published benchmarks exist

\---

## ML Algorithms Covered

|Algorithm|Type|Use Case|
|-|-|-|
|**CAL (Continuous Active Learning)**|Supervised|Document relevance review|
|**BERT Transformers**|Supervised (NLP)|Text classification, Q\&A|
|**TF-IDF + Vector Space Model**|Unsupervised (NLP)|Document ranking and search|
|**K-Means Clustering**|Unsupervised|Grouping similar documents|
|**Shingling + MinHash**|Algorithm|Near-duplicate detection|
|**Name Normalisation**|ML-assisted|Entity resolution in emails|
|**Email Threading**|Rule-based + ML|Conversation grouping|

\---

## EDRM Integration

The **Electronic Discovery Reference Model** has 9 stages. ML/Data Analytics mainly work in:

|EDRM Stage|ML Application|
|-|-|
|**Collection**|Filtering duplicates, irrelevant files, sensitive data|
|**Processing**|Text extraction, deduplication, near-duplicate detection|
|**Review**|Active learning (CAL) for relevance classification|
|**Analysis**|Topic modelling, anomaly detection, fact development|

\---

## Key References

|Paper|Contribution|
|-|-|
|Grossman \& Cormack (2011)|TAR effectiveness — higher recall than manual review|
|Cormack \& Grossman (2016)|CAL validation — 95% recall with 1-2% human review|
|Broder (1997)|Near-duplicate detection using shingling and MinHash|
|Manning et al. (2008)|NLP — TF-IDF, tokenization, vector space models|
|Devlin et al. (2019)|BERT transformer — bidirectional language model|
|EDRM (2019)|Electronic Discovery Reference Model framework|
|Garfinkel (2010)|Digital forensics and large dataset challenges|
|The Sedona Conference (2023)|Legal defensibility of TAR|

\---

## File in this folder

|File|Description|
|-|-|
|`CA2-Digital-Forensics-eDiscovery.docx`|Full literature review report on ML \& Data Analytics in eDiscovery and Digital Forensics|



