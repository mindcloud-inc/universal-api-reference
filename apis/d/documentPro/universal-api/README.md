# <img src="https://images.mindcloud.co/apps/icons/documentpro-icon_1775661480643.png" alt="DocumentPro logo" width="28" height="28"> DocumentPro: Universal API

DocumentPro extracts structured data from documents and manages extraction workflows over the DocumentPro REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/documentPro/latest
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://documentpro.ai
- **Vendor API docs:** https://docs.documentpro.ai/docs/getting-started/quick-start

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workflows](actions/list-workflows.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/list-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Uploaded Document](actions/confirm-uploaded-document.md) | POST | Confirms a large uploaded document in DocumentPro. |
| [Upload Document](actions/upload-document.md) | POST | Uploads a document to DocumentPro. |

### Document Upload

| Action | Method | Description |
| --- | --- | --- |
| [Get Large Upload URL](actions/get-large-upload-url.md) | GET | Retrieves a large-file upload URL from DocumentPro. |

### Extract Job

| Action | Method | Description |
| --- | --- | --- |
| [Delete Job](actions/delete-job.md) | DELETE | Deletes an extract job from DocumentPro. |
| [Poll Extract](actions/poll-extract.md) | GET | Retrieves an extract job result from DocumentPro. |
| [Run Extract](actions/run-extract.md) | POST | Starts an extract job in DocumentPro. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a new workflow in DocumentPro. |
| [Delete Workflow](actions/delete-workflow.md) | DELETE | Deletes an existing workflow from DocumentPro. |
| [Disable Email Attachment Parsing](actions/disable-email-attachment-parsing.md) | PUT | Disables email attachment parsing for a DocumentPro workflow. |
| [Disable Email Body Parsing](actions/disable-email-body-parsing.md) | PUT | Disables email body parsing for a DocumentPro workflow. |
| [Disable Footer Removal](actions/disable-footer-removal.md) | PUT | Disables footer removal for a DocumentPro workflow. |
| [Disable Header Removal](actions/disable-header-removal.md) | PUT | Disables header removal for a DocumentPro workflow. |
| [Disable OCR Checkbox Detection](actions/disable-ocr-checkbox-detection.md) | PUT | Disables OCR checkbox detection for a DocumentPro workflow. |
| [Disable OCR Layout Detection](actions/disable-ocr-layout-detection.md) | PUT | Disables OCR layout detection for a DocumentPro workflow. |
| [Disable OCR Table Detection](actions/disable-ocr-table-detection.md) | PUT | Disables OCR table detection for a DocumentPro workflow. |
| [Disable PDF Splitting](actions/disable-pdf-splitting.md) | PUT | Disables PDF splitting for a DocumentPro workflow. |
| [Disable Table Removal](actions/disable-table-removal.md) | PUT | Disables table removal for a DocumentPro workflow. |
| [Enable Email Attachment Parsing](actions/enable-email-attachment-parsing.md) | PUT | Enables email attachment parsing for a DocumentPro workflow. |
| [Enable Email Body Parsing](actions/enable-email-body-parsing.md) | PUT | Enables email body parsing for a DocumentPro workflow. |
| [Enable Footer Removal](actions/enable-footer-removal.md) | PUT | Enables footer removal for a DocumentPro workflow. |
| [Enable Header Removal](actions/enable-header-removal.md) | PUT | Enables header removal for a DocumentPro workflow. |
| [Enable OCR Checkbox Detection](actions/enable-ocr-checkbox-detection.md) | PUT | Enables OCR checkbox detection for a DocumentPro workflow. |
| [Enable OCR Layout Detection](actions/enable-ocr-layout-detection.md) | PUT | Enables OCR layout detection for a DocumentPro workflow. |
| [Enable OCR Table Detection](actions/enable-ocr-table-detection.md) | PUT | Enables OCR table detection for a DocumentPro workflow. |
| [Enable PDF Splitting](actions/enable-pdf-splitting.md) | PUT | Enables PDF splitting for a DocumentPro workflow. |
| [Enable Table Removal](actions/enable-table-removal.md) | PUT | Enables table removal for a DocumentPro workflow. |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow from DocumentPro by ID. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from DocumentPro. |
| [Set Workflow Date Format](actions/set-workflow-date-format.md) | PUT | Updates the date format for a DocumentPro workflow. |
| [Set Workflow Webhook URL](actions/set-workflow-webhook-url.md) | PUT | Updates a workflow webhook URL in DocumentPro. |
| [Update Workflow](actions/update-workflow.md) | PUT | Updates an existing workflow in DocumentPro. |

