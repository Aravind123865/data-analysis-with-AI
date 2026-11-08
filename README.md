# IMF Country Report Analysis and Dashboard

## Project Overview

This project analyses the Dominican Republic's IMF Country Report No. 25/305 (2025) using Python and a local language model. It extracts macroeconomic indicators, identifies financial stability themes, summarises key findings, and presents the results through a visual dashboard.

## Tools and Technologies

- Python and Google Colab
- Qwen2.5-1.5B-Instruct
- PyPDF for document extraction
- Sentence Transformers and FAISS for RAG
- Pandas, NumPy and Matplotlib for data analysis and visualisation

## Implementation

The project consists of four tasks:

1. *PDF Processing and Summarisation:* Extracts and cleans report text, creates overlapping chunks, and generates section summaries.
2. *Thematic and Indicator Extraction:* Analyses seven financial stability themes and extracts key economic indicators into JSON files.
3. *Retrieval-Augmented Generation:* Uses sentence embeddings and FAISS to retrieve relevant IMF passages for question answering.
4. *Dashboard Visualisation:* Creates four charts showing thematic distribution, inflation and interest rates, RAG performance, and GDP growth versus unemployment.

An additional multi-query RAG experiment compares baseline retrieval with reciprocal-rank fusion.

## How to Run

1. Open the project notebook in Google Colab.
2. Enable a T4 GPU runtime.
3. Upload the Dominican Republic IMF report PDF.
4. Run the notebook cells sequentially.
5. Access the generated JSON, CSV, PNG and PDF outputs in /content/imf_outputs/.

## Key Results

- 116 PDF pages processed into 253 text chunks.
- Seven financial stability themes identified.
- Six economic indicators extracted, with missing values recorded as null.
- FAISS retrieval evaluated on six questions.
- Multi-query retrieval improved reference-page coverage from 66.67% to 83.33%.
- Four-panel financial dashboard generated at 300 DPI.

## Limitations

Some language-model responses contained numerical inaccuracies or incomplete citations. Source verification and rule-based checks were used to identify these issues. Improved retrieval did not consistently improve factual answer accuracy.

## Data Source

International Monetary Fund (2025). Dominican Republic: 2025 Article IV Consultation. IMF Country Report No. 25/305.
