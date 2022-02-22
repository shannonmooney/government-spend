# Government Spend Analysis: Using a simple NLP normalization strategy to fuzzy match unique suppliers in the FY2016 USA spend dataset

## Description

This project loads in data from the FY2016 spend dataset using Dask for quicker performance on larger datasets, saves the data to parquet format for easier repeat access, narrows down to columns of interest to answer a number of questions, and then uses a fuzzy matching strategy with a simple spaCy and NLTK natural language normalization pipeline to obtain true unique suppliers in this dataset.

## Outputs

This project generated the following outputs:

- *Number of initial records in dataset:* There are **4,820,290** initial records in this dataset.
- *Count of unique suppliers (exact match only):* Initially, there are **153,462** unique suppliers.
- *Count of unique suppliers (fuzzy matching):* Using a simple NLP pipeline reduces the number of unique suppliers to **146,182**.


Navigate to the Jupyter notebook to view full project code and outputs. 

## Evaluation

In addition to the evaluation itself, which presents precision and recall measures as well as an overall F1 score, the evaluation section of the notebook also contains an idea for an alternative strategy that, if developed, may lead to more matching (and the ability for the analyst to control matching threshold).

## Next Steps

*(copied from notebook)* With a new code for true unique supplier, an analyst may return to the full dataset to attempt to answer questions such as the following with increased accuracy (these are just examples of the many questions that this data could be put to use for):

- What kinds of suppliers have agreements with the greatest number of offices and what kinds of offices have agreements with the greatest number of suppliers?
- Do these cluster in any sectors (using the sector indicator columns present in the original dataset)?
- Do offices or divisions have multiple agreements with the same supplier under different supplier names? (With multiple year datasets) are offices or divisions recording suppliers as new recipient_names when there is actually a preexisting relationship with the same supplier under a preexisting name?





