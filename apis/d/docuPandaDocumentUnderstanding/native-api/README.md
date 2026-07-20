# DocuPanda - Document Understanding: Native API Reference

A consolidated summary of DocuPanda - Document Understanding's API configuration and 95 documented operations, with links to official documentation.

- **Official docs:** https://docs.docupipe.ai/reference
- **OpenAPI specification:** https://docs.docupipe.ai/openapi/openapi.json
- **API base URL:** `https://app.docupipe.ai`

## Authentication

### API Key

Authenticate with a DocuPanda API key sent in the shared X-API-Key header on every request.

### Credentials

- **API Key:** `apiKey` · required · Your DocuPanda API key used in the X-API-Key header.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.docupipe.ai/reference)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (95 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Workspace Member](actions/add-workspace-member.md) | `POST /internal/workspace/member/add` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Bulk Download Standardization Excels](actions/bulk-excel-download.md) | `POST /standardization/download/bulk-excel` | [docs](https://docs.docupipe.ai/reference/bulk_excel_download) |
| [Bulk Download OCR PDFs](actions/bulk-ocr-download.md) | `POST /document/download/bulk-ocr-url` | [docs](https://docs.docupipe.ai/reference/bulk_ocr_download) |
| [Bulk Download Original Documents](actions/bulk-original-download.md) | `POST /document/download/bulk-original-url` | [docs](https://docs.docupipe.ai/reference/bulk_original_download) |
| [Bulk Download Standardization XMLs](actions/bulk-xml-download.md) | `POST /standardization/download/bulk-xml` | [docs](https://docs.docupipe.ai/reference/bulk_xml_download) |
| [Create Workspace](actions/create-workspace.md) | `POST /internal/workspace/create` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Delete Multiple Analyses](actions/delete-analyses.md) | `DELETE /analyses` | [docs](https://docs.docupipe.ai/reference/delete_analyses) |
| [Delete a Class](actions/delete-class.md) | `DELETE /class/:class_id` | [docs](https://docs.docupipe.ai/reference/delete_class) |
| [Delete a Document](actions/delete-document.md) | `DELETE /document/:document_id` | [docs](https://docs.docupipe.ai/reference/delete_document) |
| [Delete Multiple Documents](actions/delete-documents.md) | `DELETE /documents` | [docs](https://docs.docupipe.ai/reference/delete_documents) |
| [Deregister an Endpoint](actions/delete-endpoint.md) | `POST /webhook/delete-endpoint` | [docs](https://docs.docupipe.ai/reference/delete_endpoint) |
| [Delete Jobs](actions/delete-jobs.md) | `DELETE /jobs` | [docs](https://docs.docupipe.ai/reference/delete_jobs) |
| [Delete Reviews](actions/delete-reviews.md) | `DELETE /reviews` | [docs](https://docs.docupipe.ai/reference/delete_reviews) |
| [Delete a Schema](actions/delete-schema.md) | `DELETE /schema/:schema_id` | [docs](https://docs.docupipe.ai/reference/delete_schema) |
| [Delete a Standardization](actions/delete-standardization.md) | `DELETE /standardization/:standardization_id` | [docs](https://docs.docupipe.ai/reference/delete_standardization) |
| [Delete Multiple Standardizations](actions/delete-standardizations.md) | `DELETE /standardizations` | [docs](https://docs.docupipe.ai/reference/delete_standardizations) |
| [Delete a Workflow](actions/delete-workflow.md) | `DELETE /workflow/:workflow_id` | [docs](https://docs.docupipe.ai/reference/delete_workflow) |
| [Delete Workspace](actions/delete-workspace.md) | `DELETE /internal/workspace/delete` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Download Excel URL](actions/download-excel-url.md) | `GET /standardization/:standardization_id/download/excel-url` | [docs](https://docs.docupipe.ai/reference/download_excel_url) |
| [Download OCR URL](actions/download-ocr-url.md) | `GET /document/:document_id/download/ocr-url` | [docs](https://docs.docupipe.ai/reference/download_ocr_url) |
| [Download Original URL](actions/download-original-url.md) | `GET /document/:document_id/download/original-url` | [docs](https://docs.docupipe.ai/reference/download_original_url) |
| [Download Public URL](actions/download-public-url.md) | `GET /document/:document_id/download/public-url` | [docs](https://docs.docupipe.ai/reference/download_public_url) |
| [Register an Endpoint](actions/generate-endpoint.md) | `POST /webhook/generate-endpoint` | [docs](https://docs.docupipe.ai/reference/generate_endpoint) |
| [Get Account Information](actions/get-account-information.md) | `GET /account` | [docs](https://docs.docupipe.ai/reference/get_account) |
| [Retrieve Analysis](actions/get-analysis.md) | `GET /analysis/:analysis_id` | [docs](https://docs.docupipe.ai/reference/get_analysis) |
| [Retrieve Classification Job](actions/get-classify-job.md) | `GET /classify/:job_id` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
| [Retrieve a Processed Document](actions/get-document.md) | `GET /document/:document_id` | [docs](https://docs.docupipe.ai/reference/get_document) |
| [Retrieve Detailed Processing Result](actions/get-document-detailed.md) | `GET /document/:document_id/detailed` | [docs](https://docs.docupipe.ai/reference/get_document_detailed) |
| [Get Document Count](actions/get-document-summary.md) | `GET /documents/summary` | [docs](https://docs.docupipe.ai/reference/get_document_summary) |
| [Retrieve a Job](actions/get-job.md) | `GET /job/:job_id` | [docs](https://docs.docupipe.ai/reference/get_job) |
| [Get Job Count](actions/get-job-summary.md) | `GET /jobs/summary` | [docs](https://docs.docupipe.ai/reference/get_job_summary) |
| [Get Webhook Portal URL](actions/get-portal-link.md) | `GET /webhook/get-portal-link` | [docs](https://docs.docupipe.ai/reference/get_portal_link) |
| [Generate a Presigned URL for a Review](actions/get-presigned-url.md) | `GET /review/:review_id/presigned-url` | [docs](https://docs.docupipe.ai/reference/get_presigned_url) |
| [Get Schema Proposals](actions/get-proposed-schemas.md) | `GET /document/:document_id/proposed-schemas` | [docs](https://docs.docupipe.ai/reference/get_proposed_schemas) |
| [Retrieve a Review by ID](actions/get-review-by-id.md) | `GET /review/:review_id` | [docs](https://docs.docupipe.ai/reference/get_review_by_id) |
| [Retrieve a Schema](actions/get-schema.md) | `GET /schema/:schema_id` | [docs](https://docs.docupipe.ai/reference/get_schema) |
| [Retrieve AutoGenerate Schema Job](actions/get-schema-autogenerate-job.md) | `GET /schema/autogenerate/:job_id` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
| [Retrieve a Schema](actions/get-schema-by-id.md) | `GET /schema/id/:schema_id` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
| [Retrieve Split Job](actions/get-split-job.md) | `GET /split/:job_id` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
| [Retrieve a Standardization JSON](actions/get-standardization.md) | `GET /standardization/:standardization_id` | [docs](https://docs.docupipe.ai/reference/get_standardization) |
| [Get Standardization Count](actions/get-standardization-count.md) | `POST /internal/standardization/count` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Retrieve review by standardization ID](actions/get-standardization-review.md) | `GET /review` | [docs](https://docs.docupipe.ai/reference/get_standardization_review) |
| [Get Standardization Count](actions/get-standardization-summary.md) | `GET /standardizations/summary` | [docs](https://docs.docupipe.ai/reference/get_standardization_summary) |
| [Retrieve a Standardization XML](actions/get-standardization-xml.md) | `GET /standardization/:standardization_id/xml` | [docs](https://docs.docupipe.ai/reference/get_standardization_xml) |
| [Get Workspace Billing Info](actions/get-workspace-billing-info.md) | `GET /internal/workspace/billing-info` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://docs.docupipe.ai/reference/health_check) |
| [Health Check Post](actions/health-check-post.md) | `POST /health` | [docs](https://docs.docupipe.ai/reference/health_check_post) |
| [Leave Workspace](actions/leave-workspace.md) | `DELETE /internal/workspace/leave` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [List Analyses](actions/list-analyses.md) | `GET /analyses` | [docs](https://docs.docupipe.ai/reference/list_analyses) |
| [List Classes](actions/list-classes.md) | `GET /classes` | [docs](https://docs.docupipe.ai/reference/list_classes) |
| [List Dataset Names](actions/list-datasets.md) | `GET /dataset-names` | [docs](https://docs.docupipe.ai/reference/list_datasets) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://docs.docupipe.ai/reference/list_documents) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://docs.docupipe.ai/reference/list_jobs) |
| [List Reviews](actions/list-reviews.md) | `GET /reviews` | [docs](https://docs.docupipe.ai/reference/list_reviews) |
| [List Schemas](actions/list-schemas.md) | `GET /schemas` | [docs](https://docs.docupipe.ai/reference/list_schemas) |
| [List Standardizations](actions/list-standardizations.md) | `GET /standardizations` | [docs](https://docs.docupipe.ai/reference/list_standardizations) |
| [List your Workflows](actions/list-workflows.md) | `GET /workflows` | [docs](https://docs.docupipe.ai/reference/list_workflows) |
| [List Workspaces](actions/list-workspaces.md) | `GET /internal/workspace/list` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Match a standardization to a list of candidates](actions/match-standardization.md) | `POST /enterprise/matching` | [docs](https://docs.docupipe.ai/reference/match_standardization) |
| [Add a Class](actions/post-add-class.md) | `POST /class` | [docs](https://docs.docupipe.ai/reference/post_add_class) |
| [Analyze Data](actions/post-analyze-data.md) | `POST /analyze/data` | [docs](https://docs.docupipe.ai/reference/post_analyze_data) |
| [Analyze Document](actions/post-analyze-document.md) | `POST /analyze/document` | [docs](https://docs.docupipe.ai/reference/post_analyze_document) |
| [Classify Documents](actions/post-classify-batch.md) | `POST /classify/batch` | [docs](https://docs.docupipe.ai/reference/post_classify_batch) |
| [Copy a Class to Another Workspace](actions/post-copy-classification.md) | `POST /copy/classification` | [docs](https://docs.docupipe.ai/reference/post_copy_classification) |
| [Copy a Schema to Another Workspace](actions/post-copy-schema.md) | `POST /copy/schema` | [docs](https://docs.docupipe.ai/reference/post_copy_schema) |
| [Submit a Document for Processing](actions/post-document.md) | `POST /document` | [docs](https://docs.docupipe.ai/reference/post_document) |
| [Edit a Schema](actions/post-edit-schema.md) | `POST /schema/edit` | [docs](https://docs.docupipe.ai/reference/post_edit_schema) |
| [Expand a Schema](actions/post-expand-schema.md) | `POST /schema/expand` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
| [Expand Class Taxonomy](actions/post-expand-taxonomy.md) | `POST /class/expand` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
| [Merge Documents](actions/post-merge.md) | `POST /documents/merge` | [docs](https://docs.docupipe.ai/reference/post_merge) |
| [Query Standardizations](actions/post-query.md) | `POST /query` | [docs](https://docs.docupipe.ai/reference/post_query) |
| [Refine a Schema](actions/post-refine-schema.md) | `POST /schema/refine` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
| [Generate a Visual Review](actions/post-review-batch.md) | `POST /review/batch` | [docs](https://docs.docupipe.ai/reference/post_review_batch) |
| [Add a New Schema](actions/post-schema.md) | `POST /schema` | [docs](https://docs.docupipe.ai/reference/post_schema) |
| [AutoGenerate a Schema](actions/post-schema-autogenerate.md) | `POST /schema/autogenerate` | [docs](https://docs.docupipe.ai/reference/post_schema_autogenerate) |
| [Split a Document](actions/post-split.md) | `POST /split` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
| [Split a Document](actions/post-split-document.md) | `POST /document/split` | [docs](https://docs.docupipe.ai/reference/post_split_document) |
| [Standardize Documents](actions/post-standardize-batch.md) | `POST /standardize/batch` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
| [Standardize V2 (Stable)](actions/post-standardize-batch-v2.md) | `POST /v2/standardize/batch` | [docs](https://docs.docupipe.ai/reference/post_standardize_batch_v2) |
| [Standardize V3 (Beta)](actions/post-standardize-v3.md) | `POST /v3/standardize` | [docs](https://docs.docupipe.ai/reference/post_standardize_v3) |
| [Update a Schema](actions/post-update-schema.md) | `POST /schema/update` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
| [Create a Workflow](actions/post-workflow-on-submit-document.md) | `POST /workflow/on-submit-document` | [docs](https://docs.docupipe.ai/reference/post_workflow_on_submit_document) |
| [Remove Workspace Member](actions/remove-workspace-member.md) | `DELETE /internal/workspace/member/remove` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Remove Workspace Member By Email](actions/remove-workspace-member-by-email.md) | `POST /internal/workspace/member/remove-by-email` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Root](actions/root.md) | `GET /` | [docs](https://docs.docupipe.ai/reference/root) |
| [Search Documents](actions/search-documents.md) | `GET /documents/search` | [docs](https://docs.docupipe.ai/reference/search_documents) |
| [Search Standardizations](actions/search-standardizations.md) | `GET /standardizations/search` | [docs](https://docs.docupipe.ai/reference/search_standardizations) |
| [Update Dataset](actions/update-documents-dataset.md) | `POST /documents/update-dataset` | [docs](https://docs.docupipe.ai/reference/update_documents_dataset) |
| [Update a Review](actions/update-review.md) | `POST /review/:review_id/update` | [docs](https://docs.docupipe.ai/reference/update_review) |
| [Update a Workflow](actions/update-workflow.md) | `POST /workflow/:workflow_id/update` | [docs](https://docs.docupipe.ai/reference/update_workflow) |
| [Update Workspace Apikey](actions/update-workspace-apikey.md) | `POST /internal/workspace/update-apikey` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Update Workspace Member](actions/update-workspace-member.md) | `POST /internal/workspace/member/update` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Update Workspace Member Role](actions/update-workspace-member-role.md) | `POST /internal/workspace/member/update-role` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Update Workspace Name](actions/update-workspace-name.md) | `PUT /internal/workspace/update-name` | [docs](https://docs.docupipe.ai/openapi/docupipe.json) |
| [Webhook Readme](actions/webhook-readme.md) | `POST /readme-webhook` | [docs](https://docs.docupipe.ai/openapi/docupanda.json) |
