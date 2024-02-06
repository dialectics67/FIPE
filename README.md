# Financial Reports Property Extraction (FIPE) dataset
This repository allows you to download the dataset FIPE for the paper "A Document-Level Challenge Dataset for Property Extraction: Evaluating In-Context Learning Capabilities of LLMs".

## Documents
All the documents are in .docx format. You can access the data from the `/data` directory. The documents consist of the company's financial reports, collected from the EDGAR database. The documents in the `/data` directory are categorized based on the company's name.

Each document is named in the format `{company_name}-{time}-{period}.docx`. For example: `AMD-2019.03.30-10-Q.docx`, `Apple-2019.09.28-10-K.docx`. `10-Q` indicates that it is a quarterly financial report, while `10-K` indicates that it is an annual financial report.

## Ground Truth
For each document, we manually annotated several test samples. The test data can be found in` ground_truth/ground_truth.json`. Each test data entry includes the following information: `company name, time, period, property name, property value, unit`. 

For example:
```
[
    [
        "Walmart",
        "2022.10.31",
        "three months",
        "Revenue",
        "152813000000.00",
        "USD"
    ]
]
```

## Basic Statistics
| \# Total Query            |                     | 4,725      |
|---------------------------|---------------------|--------------------|
| \# Document               |                     | 867       |
|                           |                     |                    |
| \# Quarterly Reports |                     | 637                |
| \# Annual Reports    |                     | 230                |
|                           |                     |                    |
| Token Number:             |                     |                    |
| Max \# Tokens        |                     | 381,739            |
| Min \# Tokens        |                     | 12,014             |
| Avg. \# Tokens       |                     | 60,455.8           |
|                           |                     |                    |
| Industry Coverage:         |                     |                    |
| Tech and Communications |                   | 29.23\%            |
| Financial Services   |                     | 16.92\%            |
| Biotech and Healthcare |                   | 18.46\%            |
| Consumer Goods       |                     | 35.38\%            |
|---------------------------|---------------------|--------------------|

The token number of each document was counted using [TikToken](https://github.com/openai/tiktoken).


