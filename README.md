# Bengali Legal Question-Answering Dataset

## Overview

This dataset contains **253 genuine legal question-answer pairs in Bengali**, carefully assembled to enable evaluation of large language models (LLMs) in real high-stakes legal reasoning settings. Unlike synthetic or translated legal benchmarks, our dataset includes questions that Bangladeshi citizens have actually asked for legitimate legal help, with responses from verified legal professionals.We created this dataset to assist our research on evaluation of AI and LLM effectiveness for real life legal questions in Bengali language.
## Data Source & Collection Methodology

The dataset is derived from **"Know Your Rights,"** Bangladesh's largest online legal help forum, a Facebook group with over 200,000 active members. On this platform, citizens post real legal questions in Bengali, and verified lawyers, legal aid practitioners, and retired judges respond via **comments** on these posts, covering domains such as family, property, commercial, criminal, and administrative law. The "Answer" field in this dataset corresponds to the lawyer's comment response to the original query.

**Sampling process:**
- Posts were systematically sampled from **January to May 2025**
- Started from a pool of **500+ candidate posts**
- Applied strict inclusion criteria:
  - Only questions where the responding commenter's credentials as a lawyer, legal aid practitioner, or retired judge could be manually verified were included
  - Only questions with **citable, expert-verified legal answers** were included
  - Only questions addressing **real, substantive legal issues** with **significant legal consequences** were kept
  - Posts that were purely emotional in nature, or that bundled multiple unrelated questions together, were **excluded**
- This filtering process, including the manual verification of commenter credentials, narrowed the pool down to a final set of **253 high-quality question–answer pairs**

## File

- `Bengali Legal Dataset.csv` — the main dataset file

## Schema

| Column | Type | Description |
|---|---|---|
| `ID` | string | Unique identifier for each QA pair |
| `Question (Bengali)` | string | The original legal question, as posted by the citizen, in Bengali |
| `Answer (Bengali)` | string | The expert-provided answer/response, in Bengali |
| `Legal Domain (Tag)` | string | The legal category/domain of the question (e.g., Family Law, Criminal Law, Property Law) |

## Dataset Size

- **Total QA pairs:** 253
- **Language:** Bengali (bn)

**Legal domain distribution:**

| Legal Domain | Count |
|---|---|
| Family Law | 110 |
| Property Law | 62 |
| Criminal Law | 43 |
| Civil Litigation | 25 |
| Other | 8 |
| Cyber Law | 3 |
| Labour Law | 2 |
| **Total** | **253** |

## Intended Use

This dataset is intended for **research purposes**, particularly for evaluating the legal reasoning and factual reliability of LLMs on authentic, low-resource-language legal questions. It is **not** intended to serve as a source of legal advice.

## Note on Opening in Microsoft Excel

If Bengali text does not render correctly when opening the file directly in Microsoft Excel, please open it via **Data → Get Data → From File → From Text/CSV** and set the file origin to **UTF-8**, or open the file in Google Sheets / LibreOffice Calc instead.

## License

This dataset is released under the **Creative Commons Attribution 4.0 International (CC-BY-4.0)** license. You are free to share and adapt this dataset for any purpose, including commercially, as long as appropriate credit is given.

See the `LICENSE` file for full terms.

## Citation

If you use this dataset, please cite:

```
[Placeholder — citation will be added upon publication]
```

## Ethical Considerations

All questions and answers were sourced from a public Facebook group where users voluntarily posted their queries seeking legal help. Prior to inclusion in this dataset, all posts were reviewed and anonymized to remove personally identifiable information (e.g., names, locations, and other identifying details), particularly given the sensitive nature of many Family Law queries.
