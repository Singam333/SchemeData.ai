# SchemeData.ai

SchemeData.ai is an open-source project that converts government scheme PDF documents into structured, machine-readable datasets. It focuses on making public scheme information easier to access, analyse, and reuse.

## Problem Statement

In India, information about government schemes is mostly published as long PDF documents across multiple ministry and state websites. These PDFs are difficult to search, compare, and analyse. Important details such as eligibility, benefits, and application process remain locked inside unstructured text.

This limits access for citizens, MSMEs, researchers, startups, and developers who want to use scheme data effectively.

## Solution Overview

SchemeData.ai provides a structured data extraction pipeline that:
- Ingests public government scheme PDFs
- Parses documents page by page
- Extracts relevant scheme information using a predefined schema
- Outputs clean and standardised datasets in CSV and JSON formats

The primary output is a reusable dataset, not just a chatbot. Search or RAG-based interfaces can be built optionally on top of the structured data.

## Key Features

- Page-wise PDF parsing with source references
- Schema-driven extraction of scheme details
- Clean and machine-readable output formats (CSV / JSON)
- Designed for scalability across hundreds of scheme documents
- Open-source and reusable for other public data domains

## Example Extracted Fields

- Scheme name  
- Target beneficiaries  
- Eligibility criteria  
- Benefits and financial assistance  
- Application process  
- Validity or duration  
- Source document and page reference  

## Data Sources

The project uses publicly available government documents, including:
- Central government ministry websites
- State government scheme portals
- Official scheme guidelines and notifications

Only open and publicly accessible data is used.

## Project Status

This repository currently contains:
- Project documentation
- Architecture design
- Scheme dataset schema

Code and extraction pipelines will be added during the hackathon development phase.

## Open Source License

This project is released under the MIT License.  
You are free to use, modify, and distribute this project with attribution.

## Contributions

Contributions are welcome. You can:
- Open issues for suggestions or improvements
- Submit pull requests for enhancements
- Extend the schema for other public domains such as health or education

## Contact

This project is developed as part of the **Public Data Extraction & Structuring** initiative to improve accessibility and reuse of government scheme information.

