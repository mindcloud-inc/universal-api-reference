# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-31-140842_1774976952225.png" alt="Docubee logo" width="28" height="28"> Docubee: Universal API

Docubee is a document workflow and eSignature platform for managing documents, workflow templates, workflow instances, signature processes, embedded experiences, and short URL generation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docubee/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.docubee.com
- **Vendor API docs:** https://docs.docubee.app/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Documents](actions/list-documents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docubee/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Docubee. |
| [Download Document](actions/download-document.md) | GET | Downloads a document from Docubee. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from Docubee. |
| [List Instance Documents](actions/list-instance-documents.md) | GET | Retrieves documents for a Docubee workflow instance. |
| [Replace Document Content](actions/replace-document-content.md) | POST | Replaces templated content in a Docubee document. |
| [Set Document Fields](actions/set-document-fields.md) | PUT | Sets fields on a document in Docubee. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Docubee. |
| [Upload Document](actions/upload-document.md) | POST | Uploads a new document to Docubee. |

### Embed Session

| Action | Method | Description |
| --- | --- | --- |
| [Embed Field Placement](actions/embed-field-placement.md) | POST | Creates an embedded field placement session in Docubee. |
| [Embed Signing](actions/embed-signing.md) | POST | Creates an embedded signing session in Docubee. |
| [Embed Web Form](actions/embed-web-form.md) | POST | Creates an embedded web form session in Docubee. |
| [Embed Workflow Runtime](actions/embed-workflow-runtime.md) | POST | Creates an embedded workflow runtime session in Docubee. |
| [Embed Workflow Start](actions/embed-workflow-start.md) | POST | Creates an embedded workflow start session in Docubee. |

### Short Url

| Action | Method | Description |
| --- | --- | --- |
| [Generate Short URL](actions/generate-short-url.md) | POST | Generates a temporary short URL for a Docubee link. |

### Signature Request

| Action | Method | Description |
| --- | --- | --- |
| [Delete Signature Process](actions/delete-signature-process.md) | DELETE | Deletes a signature process from Docubee. |
| [Get Signature Process Status](actions/get-signature-process-status.md) | GET | Retrieves the status of a Docubee signature process. |
| [List Signature Processes](actions/list-signature-processes.md) | GET | Retrieves signature processes from Docubee. |
| [Start Signature Process](actions/start-signature-process.md) | POST | Starts a signature process in Docubee. |

### Workflow Run

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Instance](actions/cancel-instance.md) | DELETE | Cancels or removes a Docubee workflow instance. |
| [List Instance Properties](actions/list-instance-properties.md) | GET | Retrieves properties for a Docubee workflow instance. |
| [List Workflow Instances](actions/list-workflow-instances.md) | GET | Retrieves instances for a Docubee workflow. |
| [Start Workflow](actions/start-workflow.md) | POST | Starts a workflow in Docubee. |

### Workflow Task

| Action | Method | Description |
| --- | --- | --- |
| [List Instance Tasks](actions/list-instance-tasks.md) | GET | Retrieves tasks for a Docubee workflow instance. |

### Workflow Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Workflow](actions/create-workflow.md) | POST | Creates a new workflow in Docubee. |
| [Export Workflow](actions/export-workflow.md) | GET | Exports a workflow from Docubee. |
| [Get Workflow Start Form Data](actions/get-workflow-start-form-data.md) | GET | Retrieves start form fields for a Docubee workflow. |
| [Import Workflow](actions/import-workflow.md) | PUT | Imports a workflow into Docubee. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from Docubee. |

