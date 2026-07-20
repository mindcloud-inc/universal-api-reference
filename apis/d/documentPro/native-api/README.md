# DocumentPro: Native API Reference

A consolidated summary of DocumentPro's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.documentpro.ai/docs/getting-started/quick-start
- **API base URL:** `https://api.documentpro.ai`

## Authentication

### DocumentPro API Key

Use your DocumentPro API key. DocumentPro requires the key in the x-api-key header on every API request.

### Credentials

- **API Key:** `apiKey` · required · Your DocumentPro API key from the account settings page.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.documentpro.ai/docs/using-api/extract/upload-document)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Confirm Uploaded Document](actions/confirm-uploaded-document.md) | `POST /v1/documents` | [docs](https://docs.documentpro.ai/docs/using-api/extract/upload-document) |
| [Create Workflow](actions/create-workflow.md) | `POST /v1/templates` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/create-workflow) |
| [Delete Job](actions/delete-job.md) | `DELETE /files` | [docs](https://docs.documentpro.ai/docs/using-api/extract/delete-result) |
| [Delete Workflow](actions/delete-workflow.md) | `DELETE /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/delete-workflow) |
| [Disable Email Attachment Parsing](actions/disable-email-attachment-parsing.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Disable Email Body Parsing](actions/disable-email-body-parsing.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Disable Footer Removal](actions/disable-footer-removal.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Disable Header Removal](actions/disable-header-removal.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Disable OCR Checkbox Detection](actions/disable-ocr-checkbox-detection.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Disable OCR Layout Detection](actions/disable-ocr-layout-detection.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Disable OCR Table Detection](actions/disable-ocr-table-detection.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Disable PDF Splitting](actions/disable-pdf-splitting.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Disable Table Removal](actions/disable-table-removal.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Enable Email Attachment Parsing](actions/enable-email-attachment-parsing.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Enable Email Body Parsing](actions/enable-email-body-parsing.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Enable Footer Removal](actions/enable-footer-removal.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Enable Header Removal](actions/enable-header-removal.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Enable OCR Checkbox Detection](actions/enable-ocr-checkbox-detection.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Enable OCR Layout Detection](actions/enable-ocr-layout-detection.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Enable OCR Table Detection](actions/enable-ocr-table-detection.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Enable PDF Splitting](actions/enable-pdf-splitting.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Enable Table Removal](actions/enable-table-removal.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Get Large Upload URL](actions/get-large-upload-url.md) | `GET /v1/documents/upload_url` | [docs](https://docs.documentpro.ai/docs/using-api/extract/upload-document) |
| [Get Workflow](actions/get-workflow.md) | `GET /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/get-workflow) |
| [List Workflows](actions/list-workflows.md) | `GET /v1/templates` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/list-workflows) |
| [Poll Extract](actions/poll-extract.md) | `GET /files` | [docs](https://docs.documentpro.ai/docs/using-api/extract/get-result) |
| [Run Extract](actions/run-extract.md) | `GET /v1/documents/:document_id/run_parser` | [docs](https://docs.documentpro.ai/docs/using-api/extract/document-workflow) |
| [Set Workflow Date Format](actions/set-workflow-date-format.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Set Workflow Webhook URL](actions/set-workflow-webhook-url.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Update Workflow](actions/update-workflow.md) | `PUT /v1/templates/:template_id` | [docs](https://docs.documentpro.ai/docs/using-api/manage-workflows/update-workflow) |
| [Upload Document](actions/upload-document.md) | `POST /v1/documents` | [docs](https://docs.documentpro.ai/docs/using-api/extract/upload-document) |
