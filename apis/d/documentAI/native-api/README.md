# Document AI: Native API Reference

A consolidated summary of Document AI's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://api.cloudmersive.com/docs/documentai.asp
- **OpenAPI specification:** https://api-console.cloudmersive.com/swagger/api/spec/documentai
- **API base URL:** `https://api.cloudmersive.com`

## Authentication

### API Key

Cloudmersive API key authentication using the Apikey request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Apikey: <apiKey>
```

[Official authentication documentation](https://api.cloudmersive.com/docs/documentai.asp)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Answer Document Questions](actions/answer-document-questions.md) | `POST /document-ai/document/analyze/answer-questions` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-analyze-answer-questions-post) |
| [Classify Document](actions/classify-document.md) | `POST /document-ai/document/extract/classify` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-classify-post) |
| [Classify Document Advanced](actions/classify-document-advanced.md) | `POST /document-ai/document/extract/classify/advanced` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-classify-advanced-post) |
| [Enforce Document Policies](actions/enforce-document-policies.md) | `POST /document-ai/document/analyze/enforce-policy` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-analyze-enforce-policy-post) |
| [Extract Document Barcodes](actions/extract-document-barcodes.md) | `POST /document-ai/document/extract/barcodes` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-barcodes-post) |
| [Extract Document Field Values](actions/extract-document-field-values.md) | `POST /document-ai/document/extract/fields` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-fields-post) |
| [Extract Document Field Values Advanced](actions/extract-document-field-values-advanced.md) | `POST /document-ai/document/extract/fields/advanced` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-fields-advanced-post) |
| [Extract Document Fields and Tables](actions/extract-document-fields-and-tables.md) | `POST /document-ai/document/extract/all` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-all-post) |
| [Extract Document Tables](actions/extract-document-tables.md) | `POST /document-ai/document/extract/tables` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-tables-post) |
| [Extract Document Text](actions/extract-document-text.md) | `POST /document-ai/document/extract/text` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-text-post) |
| [Get Document Batch Job Status](actions/get-document-batch-job-status.md) | `GET /document-ai/document/batch-job/batch-job/status` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-batch-job-batch-job-status-get) |
| [Split Document](actions/split-document.md) | `POST /document-ai/document/extract/split` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-split-post) |
| [Start Document Classification Batch Job](actions/start-document-classification-batch-job.md) | `POST /document-ai/document/batch-job/extract/classify` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-batch-job-extract-classify-post) |
| [Start Document Field Values Batch Job](actions/start-document-field-values-batch-job.md) | `POST /document-ai/document/batch-job/extract/fields/advanced` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-batch-job-extract-fields-advanced-post) |
| [Start Document Fields and Tables Batch Job](actions/start-document-fields-and-tables-batch-job.md) | `POST /document-ai/document/batch-job/extract/all` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-batch-job-extract-all-post) |
| [Start Document Text Batch Job](actions/start-document-text-batch-job.md) | `POST /document-ai/document/batch-job/extract/text` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-batch-job-extract-text-post) |
| [Summarize Document](actions/summarize-document.md) | `POST /document-ai/document/extract/summary` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-summary-post) |
| [Summarize Document Advanced](actions/summarize-document-advanced.md) | `POST /document-ai/document/extract/summary/advanced` | [docs](https://api.cloudmersive.com/docs/documentai.asp#operation--document-ai-document-extract-summary-advanced-post) |
