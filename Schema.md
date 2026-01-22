# Scheme Dataset Schema

This document defines the standard schema used by **SchemeData.ai** to extract and structure information from government scheme PDF documents.

The goal of this schema is to ensure consistency, comparability, and reusability of scheme data across different ministries, states, and documents.

---

## Overview

Each row or record in the final dataset represents **one government scheme**.

The schema is designed to:
- Capture key scheme details clearly
- Support analysis and comparison across schemes
- Avoid ambiguity and hallucination during extraction

Missing information should be recorded as `null`.

---

## Schema Fields

### 1. scheme_name
- **Type:** String  
- **Description:** Official name of the government scheme as mentioned in the document  
- **Example:** `PMEGP Scheme`

---

### 2. implementing_authority
- **Type:** String  
- **Description:** Ministry, department, or government body implementing the scheme  
- **Example:** `Ministry of MSME`

---

### 3. scheme_type
- **Type:** String  
- **Description:** Broad category of the scheme  
- **Examples:**  
  - `MSME`  
  - `Women Empowerment`  
  - `Self Employment`  
  - `Startup Support`

---

### 4. target_beneficiaries
- **Type:** String  
- **Description:** Intended beneficiaries of the scheme  
- **Example:** `Women entrepreneurs, SHGs, first-time business owners`

---

### 5. eligibility_criteria
- **Type:** String  
- **Description:** Eligibility conditions required to apply for the scheme  
- **Example:** `Women above 18 years with a valid Aadhaar`

---

### 6. benefits
- **Type:** String  
- **Description:** Non-financial benefits provided under the scheme  
- **Example:** `Skill training and mentorship`

---

### 7. financial_assistance
- **Type:** String  
- **Description:** Details of monetary support, subsidy, or grant  
- **Example:** `Subsidy up to ₹50,000`

---

### 8. application_process
- **Type:** String  
- **Description:** How beneficiaries can apply for the scheme  
- **Example:** `Online application through official portal`

---

### 9. documents_required
- **Type:** String  
- **Description:** List of documents required for application  
- **Example:** `Aadhaar, PAN, bank account details`

---

### 10. scheme_validity
- **Type:** String  
- **Description:** Validity period or duration of the scheme  
- **Example:** `Ongoing` or `2023–2026`

---

### 11. state_or_central
- **Type:** String  
- **Description:** Whether the scheme is central or state-specific  
- **Example:** `Central Government`

---

### 12. source_document
- **Type:** String  
- **Description:** Name or identifier of the source PDF document  
- **Example:** `PMEGP_Guidelines_2023.pdf`

---

### 13. source_pages
- **Type:** Array of Integers  
- **Description:** Page numbers from which the information was extracted  
- **Example:** `[3, 4, 5]`

---

## Notes on Extraction

- Only information explicitly present in the document should be extracted.
- If a field is not available, it must be set to `null`.
- No assumptions or inferred values should be added.
- Page references must be preserved for transparency and verification.

---

## Extensibility

This schema can be extended in the future to include:
- Sector-specific tags
- Language information
- Regional applicability
- Impact or outcome indicators

Contributors are encouraged to propose schema extensions through pull requests.
