# <img src="https://images.mindcloud.co/apps/icons/docupipe-icon-final_1776449436868.png" alt="DocuPanda - Document Understanding logo" width="28" height="28"> DocuPanda - Document Understanding: Universal API

DocuPanda (now DocuPipe) provides document parsing, OCR, schema extraction, standardization, analysis, classification, review, workflow, and webhook APIs for understanding unstructured documents.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docuPandaDocumentUnderstanding/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 95
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.docupipe.ai
- **Vendor API docs:** https://docs.docupipe.ai/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (95)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Delete a Class](actions/delete-class.md) | DELETE | Deletes an existing class from DocuPanda. |
| [List Classes](actions/list-classes.md) | GET | Retrieves classes from DocuPanda. |
| [Add a Class](actions/post-add-class.md) | POST | Creates a new class in DocuPanda. |
| [Classify Documents](actions/post-classify-batch.md) | POST | Creates document classifications in DocuPanda. |
| [Copy a Class to Another Workspace](actions/post-copy-classification.md) | POST | Creates a class copy in another DocuPanda workspace. |
| [Expand Class Taxonomy](actions/post-expand-taxonomy.md) | POST | Creates class taxonomy expansions in DocuPanda. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Download OCR PDFs](actions/bulk-ocr-download.md) | POST | Creates a bulk OCR PDF download URL in DocuPanda. |
| [Bulk Download Original Documents](actions/bulk-original-download.md) | POST | Creates a bulk original document download URL in DocuPanda. |
| [Delete a Document](actions/delete-document.md) | DELETE | Deletes an existing document from DocuPanda. |
| [Delete Multiple Documents](actions/delete-documents.md) | DELETE | Deletes existing documents from DocuPanda. |
| [Download OCR URL](actions/download-ocr-url.md) | GET | Retrieves an OCR PDF download URL from DocuPanda. |
| [Download Original URL](actions/download-original-url.md) | GET | Retrieves an original document download URL from DocuPanda. |
| [Download Public URL](actions/download-public-url.md) | GET | Retrieves a public document URL from DocuPanda. |
| [Retrieve a Processed Document](actions/get-document.md) | GET | Retrieves a processed document from DocuPanda. |
| [Retrieve Detailed Processing Result](actions/get-document-detailed.md) | GET | Retrieves detailed processing results from DocuPanda. |
| [Get Document Count](actions/get-document-summary.md) | GET | Retrieves document counts from DocuPanda. |
| [Get Schema Proposals](actions/get-proposed-schemas.md) | GET | Retrieves schema proposals for a document from DocuPanda. |
| [List Dataset Names](actions/list-datasets.md) | GET | Retrieves dataset names from DocuPanda. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from DocuPanda. |
| [Submit a Document for Processing](actions/post-document.md) | POST | Creates a document processing request in DocuPanda. |
| [Merge Documents](actions/post-merge.md) | POST | Creates a merged document in DocuPanda. |
| [Split a Document](actions/post-split.md) | POST | Creates split documents from a DocuPanda document. |
| [Split a Document](actions/post-split-document.md) | POST | Creates split documents from a DocuPanda document. |
| [Search Documents](actions/search-documents.md) | GET | Finds documents in DocuPanda by filename or document ID. |
| [Update Dataset](actions/update-documents-dataset.md) | PUT | Updates document datasets in DocuPanda. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Download Standardization Excels](actions/bulk-excel-download.md) | POST | Creates a bulk standardization Excel download URL in DocuPanda. |
| [Bulk Download Standardization XMLs](actions/bulk-xml-download.md) | POST | Creates a bulk standardization XML download URL in DocuPanda. |
| [Delete Multiple Analyses](actions/delete-analyses.md) | DELETE | Deletes existing analyses from DocuPanda. |
| [Delete a Standardization](actions/delete-standardization.md) | DELETE | Deletes an existing standardization from DocuPanda. |
| [Delete Multiple Standardizations](actions/delete-standardizations.md) | DELETE | Deletes existing standardizations from DocuPanda. |
| [Download Excel URL](actions/download-excel-url.md) | GET | Retrieves a standardization Excel download URL from DocuPanda. |
| [Retrieve Analysis](actions/get-analysis.md) | GET | Retrieves an analysis from DocuPanda. |
| [Retrieve a Standardization JSON](actions/get-standardization.md) | GET | Retrieves a standardization JSON result from DocuPanda. |
| [Get Standardization Count](actions/get-standardization-count.md) | GET | Retrieves standardization counts from DocuPanda. |
| [Get Standardization Count](actions/get-standardization-summary.md) | GET | Retrieves standardization counts from DocuPanda. |
| [Retrieve a Standardization XML](actions/get-standardization-xml.md) | GET | Retrieves a standardization XML result from DocuPanda. |
| [List Analyses](actions/list-analyses.md) | GET | Retrieves analyses from DocuPanda. |
| [List Standardizations](actions/list-standardizations.md) | GET | Retrieves standardizations from DocuPanda. |
| [Match a standardization to a list of candidates](actions/match-standardization.md) | POST | Creates a standardization match in DocuPanda. |
| [Analyze Data](actions/post-analyze-data.md) | POST | Creates a batch analysis in DocuPanda. |
| [Analyze Document](actions/post-analyze-document.md) | POST | Creates a document analysis in DocuPanda. |
| [Query Standardizations](actions/post-query.md) | POST | Creates a natural-language standardization query in DocuPanda. |
| [Standardize Documents](actions/post-standardize-batch.md) | POST | Creates standardizations in DocuPanda. |
| [Standardize V2 (Stable)](actions/post-standardize-batch-v2.md) | POST | Creates V2 standardizations in DocuPanda. |
| [Standardize V3 (Beta)](actions/post-standardize-v3.md) | POST | Creates V3 standardizations in DocuPanda. |
| [Search Standardizations](actions/search-standardizations.md) | GET | Finds standardizations in DocuPanda by filename or IDs. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves service health details from DocuPanda. |
| [Health Check Post](actions/health-check-post.md) | POST |  |
| [Root](actions/root.md) | GET | Retrieves service details from DocuPanda. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Delete a Schema](actions/delete-schema.md) | DELETE | Deletes an existing schema from DocuPanda. |
| [Retrieve a Schema](actions/get-schema.md) | GET | Retrieves a schema from DocuPanda. |
| [Retrieve a Schema](actions/get-schema-by-id.md) | GET | Retrieves a schema from DocuPanda. |
| [List Schemas](actions/list-schemas.md) | GET | Retrieves schemas from DocuPanda. |
| [Copy a Schema to Another Workspace](actions/post-copy-schema.md) | POST | Creates a schema copy in another DocuPanda workspace. |
| [Edit a Schema](actions/post-edit-schema.md) | PUT | Updates an existing schema in DocuPanda. |
| [Expand a Schema](actions/post-expand-schema.md) | PUT | Updates an existing schema with new documents in DocuPanda. |
| [Refine a Schema](actions/post-refine-schema.md) | PUT | Updates an existing schema from feedback in DocuPanda. |
| [Add a New Schema](actions/post-schema.md) | POST | Creates a new schema in DocuPanda. |
| [AutoGenerate a Schema](actions/post-schema-autogenerate.md) | POST | Creates a schema from documents in DocuPanda. |
| [Update a Schema](actions/post-update-schema.md) | PUT | Updates a schema by creating a new version in DocuPanda. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [Delete Reviews](actions/delete-reviews.md) | DELETE | Deletes existing reviews from DocuPanda. |
| [Generate a Presigned URL for a Review](actions/get-presigned-url.md) | GET | Retrieves a presigned review URL from DocuPanda. |
| [Retrieve a Review by ID](actions/get-review-by-id.md) | GET | Retrieves a review by ID from DocuPanda. |
| [Retrieve review by standardization ID](actions/get-standardization-review.md) | GET | Retrieves a review by standardization ID from DocuPanda. |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves reviews from DocuPanda. |
| [Generate a Visual Review](actions/post-review-batch.md) | POST | Creates a visual review in DocuPanda. |
| [Update a Review](actions/update-review.md) | PUT | Updates an existing review in DocuPanda. |

### Webhookendpoint

| Action | Method | Description |
| --- | --- | --- |
| [Deregister an Endpoint](actions/delete-endpoint.md) | POST |  |
| [Register an Endpoint](actions/generate-endpoint.md) | POST | Creates a webhook endpoint in DocuPanda. |
| [Get Webhook Portal URL](actions/get-portal-link.md) | GET | Retrieves a webhook portal URL from DocuPanda. |
| [Webhook Readme](actions/webhook-readme.md) | POST |  |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Delete a Workflow](actions/delete-workflow.md) | DELETE | Deletes an existing workflow from DocuPanda. |
| [List your Workflows](actions/list-workflows.md) | GET | Retrieves workflows from DocuPanda. |
| [Create a Workflow](actions/post-workflow-on-submit-document.md) | POST | Creates an on-submit workflow in DocuPanda. |
| [Update a Workflow](actions/update-workflow.md) | PUT | Updates an existing workflow in DocuPanda. |

### Workflowrun

| Action | Method | Description |
| --- | --- | --- |
| [Delete Jobs](actions/delete-jobs.md) | DELETE | Deletes existing jobs from DocuPanda. |
| [Retrieve Classification Job](actions/get-classify-job.md) | GET | Retrieves a classification job from DocuPanda. |
| [Retrieve a Job](actions/get-job.md) | GET | Retrieves a job from DocuPanda. |
| [Get Job Count](actions/get-job-summary.md) | GET | Retrieves job counts from DocuPanda. |
| [Retrieve AutoGenerate Schema Job](actions/get-schema-autogenerate-job.md) | GET | Retrieves a schema generation job from DocuPanda. |
| [Retrieve Split Job](actions/get-split-job.md) | GET | Retrieves a split job from DocuPanda. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from DocuPanda. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Add Workspace Member](actions/add-workspace-member.md) | POST | Creates a workspace member in DocuPanda. |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in DocuPanda. |
| [Delete Workspace](actions/delete-workspace.md) | DELETE | Deletes an existing workspace from DocuPanda. |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves workspace account details from DocuPanda. |
| [Get Workspace Billing Info](actions/get-workspace-billing-info.md) | GET | Retrieves workspace billing details from DocuPanda. |
| [Leave Workspace](actions/leave-workspace.md) | DELETE | Deletes your workspace membership from DocuPanda. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from DocuPanda. |
| [Remove Workspace Member](actions/remove-workspace-member.md) | DELETE | Deletes a workspace member from DocuPanda. |
| [Remove Workspace Member By Email](actions/remove-workspace-member-by-email.md) | DELETE | Deletes a workspace member by email from DocuPanda. |
| [Update Workspace Apikey](actions/update-workspace-apikey.md) | PUT | Updates a workspace API key in DocuPanda. |
| [Update Workspace Member](actions/update-workspace-member.md) | PUT | Updates an existing workspace member in DocuPanda. |
| [Update Workspace Member Role](actions/update-workspace-member-role.md) | PUT | Updates a workspace member role in DocuPanda. |
| [Update Workspace Name](actions/update-workspace-name.md) | PUT | Updates an existing workspace name in DocuPanda. |

