┌─────────────────────────────────────────────────────────┐
│           ARCHITECTURE: PDF TO AI-READY DATA            │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────┐    ┌─────────────┐    ┌─────────────┐ │
│  │   Input     │    │  Parsing    │    │  Storage    │ │
│  │  PDF Docs   │───▶│  Pipeline   │───▶│  (JSON +    │ │
│  │             │    │             │    │   Images)   │ │
│  └─────────────┘    └─────────────┘    └─────────────┘ │
│           │                     │               │       │
│           └─────────────────────┴───────────────┘       │
│                                 │                       │
│                    ┌────────────▼────────────┐          │
│                    │  LLM Processing Layer   │          │
│                    ├─────────────────────────┤          │
│                    │ 1. Relevance Filtering  │          │
│                    │ 2. Schema Extraction    │          │
│                    └────────────┬────────────┘          │
│                                 │                       │
│                    ┌────────────▼────────────┐          │
│                    │  Data Normalization     │          │
│                    │  & Validation           │          │
│                    └────────────┬────────────┘          │
│                                 │                       │
│                    ┌────────────▼────────────┐          │
│                    │  AI-Ready Dataset       │          │
│                    │  (CSV/JSON Format)      │          │
│                    └────────────┬────────────┘          │
│                                 │                       │
│                    ┌────────────▼────────────┐          │
│                    │  Optional Interfaces    │          │
│                    │  • Search               │          │
│                    │  • RAG System           │          │
│                    │  • Analytics            │          │
│                    └─────────────────────────┘          │
│                                                         │
└─────────────────────────────────────────────────────────┘



📚 GOVERNMENT SCHEME PDFS (Ministry/State Portals)
        ⬇
🔧 [1] DOCUMENT INGESTION
   ├─ PDF Loader
   └─ Document ID assignment
        ⬇
🔍 [2] PAGE-WISE PARSING
   ├─ Extract text
   ├─ Extract tables
   ├─ Extract images
   └─ Preserve page numbers
        ⬇
📐 [3] LAYOUT & CONTENT EXTRACTION
   ├─ Headings
   ├─ Paragraphs
   ├─ Tables
   └─ Bullet points
        ⬇
💾 [4] RAW CONTENT STORAGE
   ├─ One JSON per PDF
   └─ Image files stored locally
        ⬇
🤖 [5] SCHEME RELEVANCE CLASSIFICATION (LLM)
   ├─ Identify pages defining schemes
   └─ Ignore non-scheme commentary
        ⬇
🎯 [6] SCHEMA-GUIDED EXTRACTION (LLM)
   ├─ Fixed scheme schema
   └─ No hallucination (null if missing)
        ⬇
✅ [7] VALIDATION & NORMALISATION
   ├─ Standardise terms
   ├─ Remove duplicates
   └─ Field validation
        ⬇
📊 [8] AI-READY DATASET
   ├─ CSV / JSON format
   └─ Reusable without LLM
        ⬇
🔗 [9] OPTIONAL: SEARCH / RAG / ANALYTICS INTERFACE
