# Corporate AI Disclosure Measures

AI disclosure measures from Barrios, Campbell, Johnson, and Liu, "Signals or
Smoke? The Determinants and Informativeness of Corporate Artificial Intelligence
(AI) Disclosures," *Review of Accounting Studies*, forthcoming.

Sentences are classified with a fine-tuned FinBERT model. Each measure is the
number of AI-related sentences divided by the total number of sentences in the
document, in percentage points.

## `ai_10k.csv`

| column | description |
|---|---|
| `cik` | SEC Central Index Key |
| `gvkey` | Compustat firm identifier (see note) |
| `filing_date` | date the 10-K was filed |
| `file_id` | EDGAR file name: `<filing date>_<form type>_edgar_data_<CIK>_<accession number>.txt` |
| `ai_10k` | AI measure for Items 1, 1A and 7 of the 10-K |

`cik` is the 10-K's own identifier. `gvkey` is added using the SEC CIK-GVKEY link table and is blank where no unique link exists.

## `ai_cc.csv`

| column | description |
|---|---|
| `gvkey` | Compustat firm identifier |
| `call_date` | date of the call |
| `cal_year`, `cal_quarter` | calendar year and quarter of the call date |
| `ai_cc` | AI measure for the call transcript |

## `ai_ea.csv`

| column | description |
|---|---|
| `gvkey`, `cik` | firm identifiers |
| `datadate` | Compustat fiscal quarter end |
| `announcement_date` | earnings announcement date (Compustat `rdq`; missing for 14,362 rows) |
| `ai_ea` | AI measure for the earnings announcement |
