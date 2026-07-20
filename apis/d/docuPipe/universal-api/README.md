# <img src="https://images.mindcloud.co/apps/icons/docu-pipe_1775676934015.png" alt="DocuPipe logo" width="28" height="28"> DocuPipe: Universal API

Upload documents, extract data, standardize results, and automate workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docuPipe/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 71
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.docupipe.ai
- **Vendor API docs:** https://docs.docupipe.ai/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Information](actions/get-account-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/get-account-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (71)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Information](actions/get-account-information.md) | GET | Retrieves account information from DocuPipe. |

### Analysi

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Data](actions/analyze-data.md) | POST | Analyzes structured data in DocuPipe. |
| [Delete Multiple Analyses](actions/delete-multiple-analyses.md) | DELETE | Deletes multiple analyses from DocuPipe. |
| [List Analyses](actions/list-analyses.md) | GET | Retrieves analyses from DocuPipe. |
| [Retrieve Analysis](actions/retrieve-analysis.md) | GET | Retrieves an analysis from DocuPipe. |

### Classification

| Action | Method | Description |
| --- | --- | --- |
| [Add a Class](actions/add-a-class.md) | POST | Creates a class in DocuPipe. |
| [Copy a Class to Another Workspace](actions/copy-a-class-to-another-workspace.md) | POST | Copies a class to another DocuPipe workspace. |
| [Delete a Class](actions/delete-a-class.md) | DELETE | Deletes a class from DocuPipe. |
| [List Classes](actions/list-classes.md) | GET | Retrieves classes from DocuPipe. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Document](actions/analyze-document.md) | POST | Analyzes a document in DocuPipe. |
| [Bulk Download OCR PDFs](actions/bulk-download-ocrpd-fs.md) | POST | Creates bulk OCR PDF download URLs in DocuPipe. |
| [Bulk Download Original Documents](actions/bulk-download-original-documents.md) | POST | Creates bulk original document download URLs in DocuPipe. |
| [Classify Documents](actions/classify-documents.md) | POST | Classifies documents in DocuPipe. |
| [Delete a Document](actions/delete-a-document.md) | DELETE | Deletes a document from DocuPipe. |
| [Delete Multiple Documents](actions/delete-multiple-documents.md) | DELETE | Deletes multiple documents from DocuPipe. |
| [Download OCR URL](actions/download-ocrurl.md) | GET | Retrieves an OCR PDF download URL from DocuPipe. |
| [Download Original URL](actions/download-original-url.md) | GET | Retrieves an original document download URL from DocuPipe. |
| [Download Public URL](actions/download-public-url.md) | GET | Retrieves a public document download URL from DocuPipe. |
| [Get Document Count](actions/get-document-count.md) | GET | Retrieves the document count from DocuPipe. |
| [Get Schema Proposals](actions/get-schema-proposals.md) | GET | Retrieves schema proposals for a DocuPipe document. |
| [List Dataset Names](actions/list-dataset-names.md) | GET | Retrieves dataset names from DocuPipe. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from DocuPipe. |
| [Merge Documents](actions/merge-documents.md) | POST | Merges documents in DocuPipe. |
| [Retrieve a Processed Document](actions/retrieve-a-processed-document.md) | GET | Retrieves a processed document from DocuPipe. |
| [Retrieve Detailed Processing Result](actions/retrieve-detailed-processing-result.md) | GET | Retrieves detailed processing results from DocuPipe. |
| [Search Documents](actions/search-documents.md) | GET | Finds documents in DocuPipe. |
| [Split a Document](actions/split-a-document.md) | POST | Splits a document in DocuPipe. |
| [Submit a Document for Processing](actions/submit-a-document-for-processing.md) | POST | Submits a document for processing in DocuPipe. |
| [Update Dataset](actions/update-dataset.md) | PUT | Updates a dataset for DocuPipe documents. |

### Health Check

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves DocuPipe health status. |

### Health Check Post

| Action | Method | Description |
| --- | --- | --- |
| [Health Check Post](actions/health-check-post.md) | POST | Performs a POST health check in DocuPipe. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Delete Jobs](actions/delete-jobs.md) | DELETE | Deletes jobs from DocuPipe. |
| [Get Job Count](actions/get-job-count.md) | GET | Retrieves the job count from DocuPipe. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from DocuPipe. |
| [Retrieve a Job](actions/retrieve-a-job.md) | GET | Retrieves a job from DocuPipe. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [Delete Reviews](actions/delete-reviews.md) | DELETE | Deletes reviews from DocuPipe. |
| [Generate a Presigned URL for a Review](actions/generate-a-presigned-url-for-a-review.md) | GET | Retrieves a presigned review URL from DocuPipe. |
| [Generate a Visual Review](actions/generate-a-visual-review.md) | POST | Creates a visual review in DocuPipe. |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves reviews from DocuPipe. |
| [Retrieve a Review by ID](actions/retrieve-a-review-by-id.md) | GET | Retrieves a review from DocuPipe by ID. |
| [Retrieve review by standardization ID](actions/retrieve-review-by-standardization-id.md) | GET | Retrieves a review by standardization ID in DocuPipe. |
| [Update a Review](actions/update-a-review.md) | PUT | Updates a review in DocuPipe. |

### Root

| Action | Method | Description |
| --- | --- | --- |
| [Root](actions/root.md) | GET | Retrieves the DocuPipe API root response. |

### Schema

| Action | Method | Description |
| --- | --- | --- |
| [Add a New Schema](actions/add-a-new-schema.md) | POST | Creates a schema in DocuPipe. |
| [AutoGenerate a Schema](actions/auto-generate-a-schema.md) | POST | Generates a schema in DocuPipe. |
| [Copy a Schema to Another Workspace](actions/copy-a-schema-to-another-workspace.md) | POST | Copies a schema to another DocuPipe workspace. |
| [Delete a Schema](actions/delete-a-schema.md) | DELETE | Deletes a schema from DocuPipe. |
| [Edit a Schema](actions/edit-a-schema.md) | PUT | Updates a schema in DocuPipe. |
| [List Schemas](actions/list-schemas.md) | GET | Retrieves schemas from DocuPipe. |
| [Retrieve a Schema](actions/retrieve-a-schema.md) | GET | Retrieves a schema from DocuPipe. |

### Standardization

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Download Standardization Excels](actions/bulk-download-standardization-excels.md) | POST | Creates bulk Excel download URLs for DocuPipe standardizations. |
| [Bulk Download Standardization XMLs](actions/bulk-download-standardization-xm-ls.md) | POST | Creates bulk XML download URLs for DocuPipe standardizations. |
| [Delete a Standardization](actions/delete-a-standardization.md) | DELETE | Deletes a standardization from DocuPipe. |
| [Delete Multiple Standardizations](actions/delete-multiple-standardizations.md) | DELETE | Deletes multiple standardizations from DocuPipe. |
| [Download Excel URL](actions/download-excel-url.md) | GET | Retrieves an Excel download URL from DocuPipe. |
| [Get Standardization Count](actions/get-standardization-count.md) | GET | Retrieves the standardization count from DocuPipe. |
| [List Standardizations](actions/list-standardizations.md) | GET | Retrieves standardizations from DocuPipe. |
| [Match a standardization to a list of candidates](actions/match-a-standardization-to-a-list-of-candidates.md) | POST | Matches a standardization to candidates in DocuPipe. |
| [Query Standardizations](actions/query-standardizations.md) | POST | Queries standardizations in DocuPipe. |
| [Retrieve a Standardization JSON](actions/retrieve-a-standardization-json.md) | GET | Retrieves standardization JSON from DocuPipe. |
| [Retrieve a Standardization XML](actions/retrieve-a-standardization-xml.md) | GET | Retrieves standardization XML from DocuPipe. |
| [Search Standardizations](actions/search-standardizations.md) | GET | Finds standardizations in DocuPipe. |
| [Standardize V2 (Stable)](actions/standardize-v2-stable.md) | POST | Standardizes documents in DocuPipe using V2. |
| [Standardize V3 (Beta)](actions/standardize-v3-beta.md) | POST | Standardizes documents in DocuPipe using V3. |

### Webhook Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Deregister an Endpoint](actions/deregister-an-endpoint.md) | DELETE | Deletes a webhook endpoint from DocuPipe. |
| [Get Webhook Portal URL](actions/get-webhook-portal-url.md) | GET | Retrieves the webhook portal URL from DocuPipe. |
| [Register an Endpoint](actions/register-an-endpoint.md) | POST | Registers a webhook endpoint in DocuPipe. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create a Workflow](actions/create-a-workflow.md) | POST | Creates a workflow in DocuPipe. |
| [Delete a Workflow](actions/delete-a-workflow.md) | DELETE | Deletes a workflow from DocuPipe. |
| [List your Workflows](actions/list-your-workflows.md) | GET | Retrieves workflows from DocuPipe. |
| [Update a Workflow](actions/update-a-workflow.md) | PUT | Updates a workflow in DocuPipe. |

