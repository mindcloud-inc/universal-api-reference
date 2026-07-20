# Natif.ai: Native API Reference

A consolidated summary of Natif.ai's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.natif.ai/
- **OpenAPI specification:** https://api.natif.ai/openapi.json
- **API base URL:** `https://api.natif.ai`

## Authentication

### API Key

Use a Natif.ai API key in the Authorization header as `ApiKey <secret>`.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.natif.ai/getting_started/create_api_key/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Document Share Token](actions/create-document-share-token.md) | `POST /share-tokens/documents` | [docs](https://api.natif.ai/docs#/Document%20Capturing/create_share_token_share_tokens_documents_post) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/[:documentId]` | [docs](https://api.natif.ai/docs#/Document%20Capturing/delete_document_documents__document_id__delete) |
| [Find Uploaded Documents](actions/find-uploaded-documents.md) | `GET /documents` | [docs](https://api.natif.ai/docs#/Document%20Capturing/get_documents_documents_get) |
| [Get Document](actions/get-document.md) | `GET /documents/[:documentId]` | [docs](https://api.natif.ai/docs#/Document%20Capturing/get_document_documents__document_id__get) |
| [Get Document PDF](actions/get-document-pdf.md) | `GET /documents/[:documentId]/pdf` | [docs](https://api.natif.ai/docs#/Document%20Capturing/get_pdf_documents__document_id__pdf_get) |
| [Get Extraction Results](actions/get-extraction-results.md) | `GET /documents/[:documentId]/extractions` | [docs](https://api.natif.ai/docs#/Document%20Capturing/get_extractions_documents__document_id__extractions_get) |
| [Get OCR Results](actions/get-ocr-results.md) | `GET /documents/[:documentId]/ocr` | [docs](https://api.natif.ai/docs#/Document%20Capturing/get_ocr_documents__document_id__ocr_get) |
| [Get Processed Page Images](actions/get-processed-page-images.md) | `GET /documents/[:documentId]/processed` | [docs](https://api.natif.ai/docs#/Document%20Capturing/get_processed_pages_documents__document_id__processed_get) |
| [Get Workflow OpenAPI Spec](actions/get-workflow-openapi-spec.md) | `GET /processing/[:workflowId]/openapi` | [docs](https://api.natif.ai/docs#/Document%20Capturing/get_openapi_json_processing__workflow_id__openapi_get) |
| [List Available Workflows](actions/list-available-workflows.md) | `GET /processing/workflows` | [docs](https://api.natif.ai/docs#/Document%20Capturing/get_available_workflows_processing_workflows_get) |
| [List Document Share Tokens](actions/list-document-share-tokens.md) | `GET /share-tokens/documents` | [docs](https://api.natif.ai/docs#/Document%20Capturing/list_team_document_sharing_tokens_share_tokens_documents_get) |
| [List Reseller Customer Workflows](actions/list-reseller-customer-workflows.md) | `GET /reseller/customers/[:customerId]/workflows` | [docs](https://api.natif.ai/docs#/Reseller%20User%20Management/get_customer_workflows_reseller_customers__customer_id__workflows_get) |
| [List Reseller Customers](actions/list-reseller-customers.md) | `GET /reseller/customers` | [docs](https://api.natif.ai/docs#/Reseller%20User%20Management/get_customer_list_reseller_customers_get) |
| [List User Management Customers](actions/list-user-management-customers.md) | `GET /user-management/customers` | [docs](https://api.natif.ai/docs#/User%20Management/get_customer_list_user_management_customers_get) |
| [List User Management Users](actions/list-user-management-users.md) | `GET /user-management/users` | [docs](https://api.natif.ai/docs#/User%20Management/get_users_user_management_users_get) |
| [Report Document Extraction Error](actions/report-document-extraction-error.md) | `POST /documents/[:documentId]/error-report/extraction` | [docs](https://api.natif.ai/docs#/Document%20Capturing/report_extraction_error_documents__document_id__error_report_extraction_post) |
| [Report Extraction Errors](actions/report-extraction-errors.md) | `POST /processing/error-reports/extractions` | [docs](https://api.natif.ai/docs#/Document%20Capturing/report_extraction_error_processing_error_reports_extractions_post) |
| [Revoke Document Share Token](actions/revoke-document-share-token.md) | `DELETE /share-tokens/documents` | [docs](https://api.natif.ai/docs#/Document%20Capturing/revoke_doc_sharing_tokens_share_tokens_documents_delete) |
| [Send Processing Feedback](actions/send-processing-feedback.md) | `POST /processing/feedback/[:processingId]` | [docs](https://api.natif.ai/docs#/Document%20Capturing/report_feedback_processing_feedback__processing_id__post) |
| [Upload Document For Capturing](actions/upload-document-for-capturing.md) | `POST /documents` | [docs](https://api.natif.ai/docs#/Document%20Capturing/upload_document_documents_post) |
| [View Daily Workflow Usage](actions/view-daily-workflow-usage.md) | `GET /processing/[:workflowId]/usage/daily` | [docs](https://api.natif.ai/docs#/Document%20Capturing/J_processing__workflow_id__usage_daily_get) |
| [View Hourly Workflow Usage](actions/view-hourly-workflow-usage.md) | `GET /processing/[:workflowId]/usage/hourly` | [docs](https://api.natif.ai/docs#/Document%20Capturing/J_processing__workflow_id__usage_hourly_get) |
| [View Monthly Workflow Usage](actions/view-monthly-workflow-usage.md) | `GET /processing/[:workflowId]/usage/monthly` | [docs](https://api.natif.ai/docs#/Document%20Capturing/J_processing__workflow_id__usage_monthly_get) |
| [View Weekly Workflow Usage](actions/view-weekly-workflow-usage.md) | `GET /processing/[:workflowId]/usage/weekly` | [docs](https://api.natif.ai/docs#/Document%20Capturing/J_processing__workflow_id__usage_weekly_get) |
