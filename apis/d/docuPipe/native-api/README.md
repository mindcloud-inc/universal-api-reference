# DocuPipe: Native API Reference

A consolidated summary of DocuPipe's API configuration and 71 documented operations, with links to official documentation.

- **Official docs:** https://docs.docupipe.ai/reference
- **API base URL:** `https://app.docupipe.ai`

## Authentication

### DocuPipe API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.docupipe.ai/reference/getting-started-with-docupipe)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 0–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (71 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add a Class](actions/add-a-class.md) | `POST /class` | [docs](https://docs.docupipe.ai/reference/post_add_class) |
| [Add a New Schema](actions/add-a-new-schema.md) | `POST /schema` | [docs](https://docs.docupipe.ai/reference/post_schema) |
| [Analyze Data](actions/analyze-data.md) | `POST /analyze/data` | [docs](https://docs.docupipe.ai/reference/post_analyze_data) |
| [Analyze Document](actions/analyze-document.md) | `POST /analyze/document` | [docs](https://docs.docupipe.ai/reference/post_analyze_document) |
| [AutoGenerate a Schema](actions/auto-generate-a-schema.md) | `POST /schema/autogenerate` | [docs](https://docs.docupipe.ai/reference/post_schema_autogenerate) |
| [Bulk Download OCR PDFs](actions/bulk-download-ocrpd-fs.md) | `POST /document/download/bulk-ocr-url` | [docs](https://docs.docupipe.ai/reference/bulk_ocr_download) |
| [Bulk Download Original Documents](actions/bulk-download-original-documents.md) | `POST /document/download/bulk-original-url` | [docs](https://docs.docupipe.ai/reference/bulk_original_download) |
| [Bulk Download Standardization Excels](actions/bulk-download-standardization-excels.md) | `POST /standardization/download/bulk-excel` | [docs](https://docs.docupipe.ai/reference/bulk_excel_download) |
| [Bulk Download Standardization XMLs](actions/bulk-download-standardization-xm-ls.md) | `POST /standardization/download/bulk-xml` | [docs](https://docs.docupipe.ai/reference/bulk_xml_download) |
| [Classify Documents](actions/classify-documents.md) | `POST /classify/batch` | [docs](https://docs.docupipe.ai/reference/post_classify_batch) |
| [Copy a Class to Another Workspace](actions/copy-a-class-to-another-workspace.md) | `POST /copy/classification` | [docs](https://docs.docupipe.ai/reference/post_copy_classification) |
| [Copy a Schema to Another Workspace](actions/copy-a-schema-to-another-workspace.md) | `POST /copy/schema` | [docs](https://docs.docupipe.ai/reference/post_copy_schema) |
| [Create a Workflow](actions/create-a-workflow.md) | `POST /workflow/on-submit-document` | [docs](https://docs.docupipe.ai/reference/post_workflow_on_submit_document) |
| [Delete a Class](actions/delete-a-class.md) | `DELETE /class/:classId` | [docs](https://docs.docupipe.ai/reference/delete_class) |
| [Delete a Document](actions/delete-a-document.md) | `DELETE /document/:documentId` | [docs](https://docs.docupipe.ai/reference/delete_document) |
| [Delete a Schema](actions/delete-a-schema.md) | `DELETE /schema/:schemaId` | [docs](https://docs.docupipe.ai/reference/delete_schema) |
| [Delete a Standardization](actions/delete-a-standardization.md) | `DELETE /standardization/:standardizationId` | [docs](https://docs.docupipe.ai/reference/delete_standardization) |
| [Delete a Workflow](actions/delete-a-workflow.md) | `DELETE /workflow/:workflowId` | [docs](https://docs.docupipe.ai/reference/delete_workflow) |
| [Delete Jobs](actions/delete-jobs.md) | `DELETE /jobs` | [docs](https://docs.docupipe.ai/reference/delete_jobs) |
| [Delete Multiple Analyses](actions/delete-multiple-analyses.md) | `DELETE /analyses` | [docs](https://docs.docupipe.ai/reference/delete_analyses) |
| [Delete Multiple Documents](actions/delete-multiple-documents.md) | `DELETE /documents` | [docs](https://docs.docupipe.ai/reference/delete_documents) |
| [Delete Multiple Standardizations](actions/delete-multiple-standardizations.md) | `DELETE /standardizations` | [docs](https://docs.docupipe.ai/reference/delete_standardizations) |
| [Delete Reviews](actions/delete-reviews.md) | `DELETE /reviews` | [docs](https://docs.docupipe.ai/reference/delete_reviews) |
| [Deregister an Endpoint](actions/deregister-an-endpoint.md) | `POST /webhook/delete-endpoint` | [docs](https://docs.docupipe.ai/reference/delete_endpoint) |
| [Download Excel URL](actions/download-excel-url.md) | `GET /standardization/:standardizationId/download/excel-url` | [docs](https://docs.docupipe.ai/reference/download_excel_url) |
| [Download OCR URL](actions/download-ocrurl.md) | `GET /document/:documentId/download/ocr-url` | [docs](https://docs.docupipe.ai/reference/download_ocr_url) |
| [Download Original URL](actions/download-original-url.md) | `GET /document/:documentId/download/original-url` | [docs](https://docs.docupipe.ai/reference/download_original_url) |
| [Download Public URL](actions/download-public-url.md) | `GET /document/:documentId/download/public-url` | [docs](https://docs.docupipe.ai/reference/download_public_url) |
| [Edit a Schema](actions/edit-a-schema.md) | `POST /schema/edit` | [docs](https://docs.docupipe.ai/reference/post_edit_schema) |
| [Generate a Presigned URL for a Review](actions/generate-a-presigned-url-for-a-review.md) | `GET /review/:reviewId/presigned-url` | [docs](https://docs.docupipe.ai/reference/get_presigned_url) |
| [Generate a Visual Review](actions/generate-a-visual-review.md) | `POST /review/batch` | [docs](https://docs.docupipe.ai/reference/post_review_batch) |
| [Get Account Information](actions/get-account-information.md) | `GET /account` | [docs](https://docs.docupipe.ai/reference/get_account) |
| [Get Document Count](actions/get-document-count.md) | `GET /documents/summary` | [docs](https://docs.docupipe.ai/reference/get_document_summary) |
| [Get Job Count](actions/get-job-count.md) | `GET /jobs/summary` | [docs](https://docs.docupipe.ai/reference/get_job_summary) |
| [Get Schema Proposals](actions/get-schema-proposals.md) | `GET /document/:documentId/proposed-schemas` | [docs](https://docs.docupipe.ai/reference/get_proposed_schemas) |
| [Get Standardization Count](actions/get-standardization-count.md) | `GET /standardizations/summary` | [docs](https://docs.docupipe.ai/reference/get_standardization_summary) |
| [Get Webhook Portal URL](actions/get-webhook-portal-url.md) | `GET /webhook/get-portal-link` | [docs](https://docs.docupipe.ai/reference/get_portal_link) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://docs.docupipe.ai/reference/health_check) |
| [Health Check Post](actions/health-check-post.md) | `POST /health` | [docs](https://docs.docupipe.ai/reference/health_check_post) |
| [List Analyses](actions/list-analyses.md) | `GET /analyses` | [docs](https://docs.docupipe.ai/reference/list_analyses) |
| [List Classes](actions/list-classes.md) | `GET /classes` | [docs](https://docs.docupipe.ai/reference/list_classes) |
| [List Dataset Names](actions/list-dataset-names.md) | `GET /dataset-names` | [docs](https://docs.docupipe.ai/reference/list_datasets) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://docs.docupipe.ai/reference/list_documents) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://docs.docupipe.ai/reference/list_jobs) |
| [List Reviews](actions/list-reviews.md) | `GET /reviews` | [docs](https://docs.docupipe.ai/reference/list_reviews) |
| [List Schemas](actions/list-schemas.md) | `GET /schemas` | [docs](https://docs.docupipe.ai/reference/list_schemas) |
| [List Standardizations](actions/list-standardizations.md) | `GET /standardizations` | [docs](https://docs.docupipe.ai/reference/list_standardizations) |
| [List your Workflows](actions/list-your-workflows.md) | `GET /workflows` | [docs](https://docs.docupipe.ai/reference/list_workflows) |
| [Match a standardization to a list of candidates](actions/match-a-standardization-to-a-list-of-candidates.md) | `POST /enterprise/matching` | [docs](https://docs.docupipe.ai/reference/match_standardization) |
| [Merge Documents](actions/merge-documents.md) | `POST /documents/merge` | [docs](https://docs.docupipe.ai/reference/post_merge) |
| [Query Standardizations](actions/query-standardizations.md) | `POST /query` | [docs](https://docs.docupipe.ai/reference/post_query) |
| [Register an Endpoint](actions/register-an-endpoint.md) | `POST /webhook/generate-endpoint` | [docs](https://docs.docupipe.ai/reference/generate_endpoint) |
| [Retrieve a Job](actions/retrieve-a-job.md) | `GET /job/:jobId` | [docs](https://docs.docupipe.ai/reference/get_job) |
| [Retrieve a Processed Document](actions/retrieve-a-processed-document.md) | `GET /document/:documentId` | [docs](https://docs.docupipe.ai/reference/get_document) |
| [Retrieve a Review by ID](actions/retrieve-a-review-by-id.md) | `GET /review/:reviewId` | [docs](https://docs.docupipe.ai/reference/get_review_by_id) |
| [Retrieve a Schema](actions/retrieve-a-schema.md) | `GET /schema/:schemaId` | [docs](https://docs.docupipe.ai/reference/get_schema) |
| [Retrieve a Standardization JSON](actions/retrieve-a-standardization-json.md) | `GET /standardization/:standardizationId` | [docs](https://docs.docupipe.ai/reference/get_standardization) |
| [Retrieve a Standardization XML](actions/retrieve-a-standardization-xml.md) | `GET /standardization/:standardizationId/xml` | [docs](https://docs.docupipe.ai/reference/get_standardization_xml) |
| [Retrieve Analysis](actions/retrieve-analysis.md) | `GET /analysis/:analysisId` | [docs](https://docs.docupipe.ai/reference/get_analysis) |
| [Retrieve Detailed Processing Result](actions/retrieve-detailed-processing-result.md) | `GET /document/:documentId/detailed` | [docs](https://docs.docupipe.ai/reference/get_document_detailed) |
| [Retrieve review by standardization ID](actions/retrieve-review-by-standardization-id.md) | `GET /review` | [docs](https://docs.docupipe.ai/reference/get_standardization_review) |
| [Root](actions/root.md) | `GET /` | [docs](https://docs.docupipe.ai/reference/root) |
| [Search Documents](actions/search-documents.md) | `GET /documents/search` | [docs](https://docs.docupipe.ai/reference/search_documents) |
| [Search Standardizations](actions/search-standardizations.md) | `GET /standardizations/search` | [docs](https://docs.docupipe.ai/reference/search_standardizations) |
| [Split a Document](actions/split-a-document.md) | `POST /document/split` | [docs](https://docs.docupipe.ai/reference/post_split_document) |
| [Standardize V2 (Stable)](actions/standardize-v2-stable.md) | `POST /v2/standardize/batch` | [docs](https://docs.docupipe.ai/reference/post_standardize_batch_v2) |
| [Standardize V3 (Beta)](actions/standardize-v3-beta.md) | `POST /v3/standardize` | [docs](https://docs.docupipe.ai/reference/post_standardize_v3) |
| [Submit a Document for Processing](actions/submit-a-document-for-processing.md) | `POST /document` | [docs](https://docs.docupipe.ai/reference/post_document) |
| [Update a Review](actions/update-a-review.md) | `POST /review/:reviewId/update` | [docs](https://docs.docupipe.ai/reference/update_review) |
| [Update a Workflow](actions/update-a-workflow.md) | `POST /workflow/:workflowId/update` | [docs](https://docs.docupipe.ai/reference/update_workflow) |
| [Update Dataset](actions/update-dataset.md) | `POST /documents/update-dataset` | [docs](https://docs.docupipe.ai/reference/update_documents_dataset) |
