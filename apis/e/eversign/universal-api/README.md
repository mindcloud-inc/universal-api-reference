# <img src="https://images.mindcloud.co/apps/icons/eversign_1776279218288.png" alt="Eversign logo" width="28" height="28"> Eversign: Universal API

Use Eversign (Xodo Sign) to manage businesses, documents, templates, bulk jobs, files, and audit logs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/eversign/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://eversign.com
- **Vendor API docs:** https://eversign.com/api/documentation/methods

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Businesses](actions/list-businesses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eversign/latest/actions/list-businesses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [Audit Log](actions/audit-log.md) | GET | Retrieves a document audit log from Eversign. |

### Bulk Job

| Action | Method | Description |
| --- | --- | --- |
| [List Bulk Jobs](actions/list-bulk-jobs.md) | GET | Retrieves bulk sending jobs from Eversign. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Document](actions/cancel-document.md) | PUT | Cancels an existing document in Eversign. |
| [Create Draft Document](actions/create-draft-document.md) | POST | Creates a draft document in Eversign. |
| [Create Embedded Document](actions/create-embedded-document.md) | POST | Creates an embedded signing document in Eversign. |
| [Create My Action Document](actions/create-my-action-document.md) | POST | Creates a document assigned to you in Eversign. |
| [Create Sandbox Document](actions/create-sandbox-document.md) | POST | Creates a sandbox document in Eversign. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Eversign. |
| [Download Document PDF](actions/download-document-pdf.md) | GET | Downloads a document PDF from Eversign. |
| [Download Final PDF](actions/download-final-pdf.md) | GET | Downloads a final document PDF from Eversign. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Eversign by hash. |
| [List Cancelled Documents](actions/list-cancelled-documents.md) | GET | Retrieves cancelled documents from your Eversign account. |
| [List Documents](actions/list-documents.md) | GET | Retrieves document records from your Eversign account. |
| [List Draft Documents](actions/list-draft-documents.md) | GET | Retrieves draft documents from your Eversign account. |
| [List My Action Required Documents](actions/list-my-action-required-documents.md) | GET | Retrieves documents requiring your action in Eversign. |
| [List Waiting For Others Documents](actions/list-waiting-for-others-documents.md) | GET | Retrieves documents waiting for other signers in Eversign. |
| [Reassign Signer](actions/reassign-signer.md) | PUT | Reassigns a signer on a document in Eversign. |
| [Send Reminder](actions/send-reminder.md) | PUT | Sends a signer reminder in Eversign. |
| [Trash Document](actions/trash-document.md) | DELETE | Moves a document to trash in Eversign. |
| [Use Template](actions/use-template.md) | POST | Creates a document from a template in Eversign. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates an active template in Eversign. |
| [Create Template Draft](actions/create-template-draft.md) | POST | Creates a draft template in Eversign. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from Eversign. |
| [Download Template PDF](actions/download-template-pdf.md) | GET | Downloads a template PDF from Eversign. |
| [Generate Blank CSV](actions/generate-blank-csv.md) | GET | Downloads a blank bulk-send CSV from Eversign. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Eversign by hash. |
| [List Template Drafts](actions/list-template-drafts.md) | GET | Retrieves draft templates from your Eversign account. |
| [List Templates](actions/list-templates.md) | GET | Retrieves active templates from your Eversign account. |
| [Trash Template](actions/trash-template.md) | DELETE | Moves a template to trash in Eversign. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Businesses](actions/list-businesses.md) | GET | Retrieves business records from your Eversign account. |

