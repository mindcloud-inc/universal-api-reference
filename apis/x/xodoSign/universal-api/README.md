# <img src="https://images.mindcloud.co/apps/icons/xodo-pdf-reader_1774905248079.jpeg" alt="Xodo Sign logo" width="28" height="28"> Xodo Sign: Universal API

Xodo Sign is an e-signature platform for sending documents for legally binding signatures, managing templates, and tracking audit trails.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/xodoSign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://xodo.com/fr
- **Vendor API docs:** https://eversign.com/api/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Businesses](actions/list-businesses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xodoSign/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Bulk Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Bulk Job](actions/create-bulk-job.md) | POST | Creates a new bulk job in Xodo Sign. |
| [Get Bulk Job](actions/get-bulk-job.md) | GET | Retrieves a bulk job from Xodo Sign. |
| [Get Bulk Job Status](actions/get-bulk-job-status.md) | GET | Retrieves bulk job status from Xodo Sign. |
| [List Bulk Job Documents](actions/list-bulk-job-documents.md) | GET | Retrieves documents from a bulk job in Xodo Sign. |

### Bulk Jobs

| Action | Method | Description |
| --- | --- | --- |
| [List Bulk Jobs](actions/list-bulk-jobs.md) | GET | Retrieves bulk jobs from Xodo Sign. |

### Bulk Sending

| Action | Method | Description |
| --- | --- | --- |
| [Validate Bulk Sending CSV](actions/validate-bulk-sending-csv.md) | GET | Validates a bulk sending CSV for a template in Xodo Sign. |

### Business

| Action | Method | Description |
| --- | --- | --- |
| [List Businesses](actions/list-businesses.md) | GET | Retrieves businesses from Xodo Sign. |

### Csv

| Action | Method | Description |
| --- | --- | --- |
| [Generate Blank Bulk CSV](actions/generate-blank-bulk-csv.md) | GET | Retrieves a blank bulk sending CSV for a template in Xodo Sign. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Document](actions/cancel-document.md) | DELETE | Cancels an existing document in Xodo Sign. |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Xodo Sign. |
| [Delete Document or Template](actions/delete-document-or-template.md) | DELETE | Deletes an existing document or template from Xodo Sign. |
| [Get Document or Template](actions/get-document-or-template.md) | GET | Retrieves a document or template from Xodo Sign. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Xodo Sign. |
| [Reassign Signer](actions/reassign-signer.md) | PUT | Reassigns a document signer to another person in Xodo Sign. |
| [Send Reminder](actions/send-reminder.md) | PUT | Sends a reminder to a document signer in Xodo Sign. |
| [Trash Document or Template](actions/trash-document-or-template.md) | DELETE | Moves a document or template to trash in Xodo Sign. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Xodo Sign. |

### Log

| Action | Method | Description |
| --- | --- | --- |
| [Audit Log](actions/audit-log.md) | GET | Retrieves a document audit log from Xodo Sign. |

### Pdf

| Action | Method | Description |
| --- | --- | --- |
| [Download Final PDF](actions/download-final-pdf.md) | GET | Retrieves the final PDF from Xodo Sign. |
| [Download Original PDF](actions/download-original-pdf.md) | GET | Retrieves the original PDF from Xodo Sign. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in Xodo Sign. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Xodo Sign. |
| [Use Template](actions/use-template.md) | POST | Creates a new document from a template in Xodo Sign. |

