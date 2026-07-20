# <img src="https://images.mindcloud.co/apps/icons/cropped-favicon-natif_1776100824963.png" alt="Natif.ai logo" width="28" height="28"> Natif.ai: Universal API

Document AI API for uploading documents, extracting OCR and structured data, managing workflows, and checking usage in Natif.ai.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/natifai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://natif.ai
- **Vendor API docs:** https://developer.natif.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Available Workflows](actions/list-available-workflows.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/natifai/latest/actions/list-available-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Share Token](actions/create-document-share-token.md) | POST | Creates a document sharing token in Natif.ai. |
| [List Document Share Tokens](actions/list-document-share-tokens.md) | GET | Retrieves document sharing tokens from Natif.ai. |
| [Revoke Document Share Token](actions/revoke-document-share-token.md) | DELETE | Deletes an existing document sharing token from Natif.ai. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Reseller Customers](actions/list-reseller-customers.md) | GET | Retrieves reseller customer records from Natif.ai. |
| [List User Management Customers](actions/list-user-management-customers.md) | GET | Retrieves customers from Natif.ai user management. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Natif.ai. |
| [Find Uploaded Documents](actions/find-uploaded-documents.md) | GET | Finds uploaded documents in Natif.ai by filter criteria. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document and its processing status from Natif.ai. |
| [Get Document PDF](actions/get-document-pdf.md) | GET | Retrieves a processed document PDF from Natif.ai. |
| [Get Extraction Results](actions/get-extraction-results.md) | GET | Retrieves extraction results for a document from Natif.ai. |
| [Get OCR Results](actions/get-ocr-results.md) | GET | Retrieves OCR results for a document from Natif.ai. |
| [Get Processed Page Images](actions/get-processed-page-images.md) | GET | Retrieves processed page images for a document from Natif.ai. |
| [Upload Document For Capturing](actions/upload-document-for-capturing.md) | POST | Creates a new document for capturing in Natif.ai. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Report Document Extraction Error](actions/report-document-extraction-error.md) | POST | Creates an extraction error report for a document in Natif.ai. |
| [Report Extraction Errors](actions/report-extraction-errors.md) | POST | Creates an extraction error report for Natif.ai processing. |
| [Send Processing Feedback](actions/send-processing-feedback.md) | POST | Creates processing feedback for a document in Natif.ai. |
| [View Daily Workflow Usage](actions/view-daily-workflow-usage.md) | GET | Retrieves daily usage details for a Natif.ai workflow. |
| [View Hourly Workflow Usage](actions/view-hourly-workflow-usage.md) | GET | Retrieves hourly usage details for a Natif.ai workflow. |
| [View Monthly Workflow Usage](actions/view-monthly-workflow-usage.md) | GET | Retrieves monthly usage details for a Natif.ai workflow. |
| [View Weekly Workflow Usage](actions/view-weekly-workflow-usage.md) | GET | Retrieves weekly usage details for a Natif.ai workflow. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List User Management Users](actions/list-user-management-users.md) | GET | Retrieves users from Natif.ai user management. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow OpenAPI Spec](actions/get-workflow-openapi-spec.md) | GET | Retrieves the OpenAPI spec for a Natif.ai workflow. |
| [List Available Workflows](actions/list-available-workflows.md) | GET | Retrieves available processing workflows from Natif.ai. |
| [List Reseller Customer Workflows](actions/list-reseller-customer-workflows.md) | GET | Retrieves workflows for a reseller customer in Natif.ai. |

