# Docubee: Native API Reference

A consolidated summary of Docubee's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://docs.docubee.app/
- **API base URL:** `https://docubee.app/api/v2`

## Authentication

### API Key

Authenticate with a Docubee workspace access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.docubee.app/)

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Instance](actions/cancel-instance.md) | `DELETE /instances/:instanceId` | [docs](https://docs.docubee.app/#cancel-instance) |
| [Create Workflow](actions/create-workflow.md) | `POST /workflowTemplates` | [docs](https://docs.docubee.app/#create-new) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:documentId` | [docs](https://docs.docubee.app/#delete-existing-document) |
| [Delete Signature Process](actions/delete-signature-process.md) | `DELETE /signatures/:processId` | [docs](https://docs.docubee.app/#delete-signature-process) |
| [Download Document](actions/download-document.md) | `GET /documents/:documentId` | [docs](https://docs.docubee.app/#download) |
| [Embed Field Placement](actions/embed-field-placement.md) | `POST /embed` | [docs](https://docs.docubee.app/#embedded-field-placement) |
| [Embed Signing](actions/embed-signing.md) | `POST /embed` | [docs](https://docs.docubee.app/#embedded-signing) |
| [Embed Web Form](actions/embed-web-form.md) | `POST /embed` | [docs](https://docs.docubee.app/#embedded-web-forms) |
| [Embed Workflow Runtime](actions/embed-workflow-runtime.md) | `POST /embed` | [docs](https://docs.docubee.app/#embedded-workflow-runtime) |
| [Embed Workflow Start](actions/embed-workflow-start.md) | `POST /embed` | [docs](https://docs.docubee.app/#embedded-workflow-start-page) |
| [Export Workflow](actions/export-workflow.md) | `GET /workflowTemplates/:templateId` | [docs](https://docs.docubee.app/#export) |
| [Generate Short URL](actions/generate-short-url.md) | `POST /urls` | [docs](https://docs.docubee.app/#generate-a-short-url) |
| [Get Signature Process Status](actions/get-signature-process-status.md) | `GET /signatures/:processId/status` | [docs](https://docs.docubee.app/#get-signature-process-status) |
| [Get Workflow Start Form Data](actions/get-workflow-start-form-data.md) | `GET /workflowTemplates/:templateId/startForm` | [docs](https://docs.docubee.app/#get-start-form) |
| [Import Workflow](actions/import-workflow.md) | `PUT /workflowTemplates/:templateId` | [docs](https://docs.docubee.app/#import) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://docs.docubee.app/#list-documents) |
| [List Instance Documents](actions/list-instance-documents.md) | `GET /instances/:instanceId/documents` | [docs](https://docs.docubee.app/#list-instance-documents) |
| [List Instance Properties](actions/list-instance-properties.md) | `GET /instances/:instanceId/properties` | [docs](https://docs.docubee.app/#list-instance-properties) |
| [List Instance Tasks](actions/list-instance-tasks.md) | `GET /instances/:instanceId/tasks` | [docs](https://docs.docubee.app/#list-instance-tasks) |
| [List Signature Processes](actions/list-signature-processes.md) | `GET /signatures` | [docs](https://docs.docubee.app/#list-signature-processes) |
| [List Workflow Instances](actions/list-workflow-instances.md) | `GET /workflowTemplates/:templateId/instances` | [docs](https://docs.docubee.app/#list-instances) |
| [List Workflows](actions/list-workflows.md) | `GET /workflowTemplates` | [docs](https://docs.docubee.app/#list-workflows) |
| [Replace Document Content](actions/replace-document-content.md) | `POST /contentReplacers` | [docs](https://docs.docubee.app/#inline-replace-existing-document) |
| [Set Document Fields](actions/set-document-fields.md) | `PUT /documents/:documentId/fields` | [docs](https://docs.docubee.app/#fields) |
| [Start Signature Process](actions/start-signature-process.md) | `POST /signatures` | [docs](https://docs.docubee.app/#start-signature-process) |
| [Start Workflow](actions/start-workflow.md) | `POST /workflowTemplates/:templateId` | [docs](https://docs.docubee.app/#start-workflow) |
| [Update Document](actions/update-document.md) | `PUT /documents/:documentId` | [docs](https://docs.docubee.app/#update-existing-document) |
| [Upload Document](actions/upload-document.md) | `POST /documents` | [docs](https://docs.docubee.app/#upload) |
