# <img src="https://images.mindcloud.co/apps/icons/icon-1_1781722611690.png" alt="Document AI logo" width="28" height="28"> Document AI: Universal API

Document AI: Extract text, fields, tables, and summaries

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/documentAI/latest
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudmersive.com/document-ai-api
- **Vendor API docs:** https://api.cloudmersive.com/docs/documentai.asp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Answer Document Questions](actions/answer-document-questions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/answer-document-questions?connectionId=$CONNECTION_ID&InputFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Advanced Document Classification

| Action | Method | Description |
| --- | --- | --- |
| [Classify Document Advanced](actions/classify-document-advanced.md) | GET | Classifies a document using advanced Document AI. |

### Advanced Document Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Document Advanced](actions/summarize-document-advanced.md) | GET |  |

### Advanced Extracted Document Fields

| Action | Method | Description |
| --- | --- | --- |
| [Extract Document Field Values Advanced](actions/extract-document-field-values-advanced.md) | GET | Extracts field values from a document using advanced Document AI. |

### Document Batch Job Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Document Batch Job Status](actions/get-document-batch-job-status.md) | GET | Retrieves the status and result of a Document AI batch job. |

### Document Classification

| Action | Method | Description |
| --- | --- | --- |
| [Classify Document](actions/classify-document.md) | GET | Classifies a document using Document AI. |

### Document Classification Batch Job

| Action | Method | Description |
| --- | --- | --- |
| [Start Document Classification Batch Job](actions/start-document-classification-batch-job.md) | POST | Creates a document classification batch job in Document AI. |

### Document Extraction Batch Job

| Action | Method | Description |
| --- | --- | --- |
| [Start Document Fields and Tables Batch Job](actions/start-document-fields-and-tables-batch-job.md) | POST | Creates a document extraction batch job in Document AI. |

### Document Field Batch Job

| Action | Method | Description |
| --- | --- | --- |
| [Start Document Field Values Batch Job](actions/start-document-field-values-batch-job.md) | POST | Creates a document field extraction batch job in Document AI. |

### Document Policy Result

| Action | Method | Description |
| --- | --- | --- |
| [Enforce Document Policies](actions/enforce-document-policies.md) | GET | Evaluates a document against policies in Document AI. |

### Document Question Answers

| Action | Method | Description |
| --- | --- | --- |
| [Answer Document Questions](actions/answer-document-questions.md) | GET |  |

### Document Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Document](actions/summarize-document.md) | GET | Generates a one-paragraph summary of a document using Document AI. |

### Document Text Batch Job

| Action | Method | Description |
| --- | --- | --- |
| [Start Document Text Batch Job](actions/start-document-text-batch-job.md) | POST | Creates a document text extraction batch job in Document AI. |

### Extracted Document Barcodes

| Action | Method | Description |
| --- | --- | --- |
| [Extract Document Barcodes](actions/extract-document-barcodes.md) | GET | Extracts barcodes from a document using Document AI. |

### Extracted Document Fields

| Action | Method | Description |
| --- | --- | --- |
| [Extract Document Field Values](actions/extract-document-field-values.md) | GET | Extracts field values from a document using Document AI. |

### Extracted Document Fields And Tables

| Action | Method | Description |
| --- | --- | --- |
| [Extract Document Fields and Tables](actions/extract-document-fields-and-tables.md) | GET | Extracts fields and tables from a document using Document AI. |

### Extracted Document Tables

| Action | Method | Description |
| --- | --- | --- |
| [Extract Document Tables](actions/extract-document-tables.md) | GET | Extracts tables from a document using Document AI. |

### Extracted Document Text

| Action | Method | Description |
| --- | --- | --- |
| [Extract Document Text](actions/extract-document-text.md) | GET | Extracts text from a document using Document AI. |

### Split Document Result

| Action | Method | Description |
| --- | --- | --- |
| [Split Document](actions/split-document.md) | GET |  |

