# <img src="https://images.mindcloud.co/apps/icons/flackon-logo_1773686465359.jpeg" alt="Docupilot logo" width="28" height="28"> Docupilot: Universal API

Generate documents, manage templates, deliveries, content blocks, and e-signature envelopes in Docupilot.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/docupilot/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.docupilot.app/
- **Vendor API docs:** https://help.docupilot.app/developers/api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Folders](actions/list-folders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docupilot/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Generate Document](actions/generate-document.md) | POST | Generates a document from a Docupilot template. |
| [List Generated Documents](actions/list-generated-documents.md) | GET | Retrieves generated document history from Docupilot. |
| [Retry Document Delivery](actions/retry-document-delivery.md) | POST | Retries failed document delivery in Docupilot. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in Docupilot. |
| [Delete Folder](actions/delete-folder.md) | DELETE | Deletes an existing folder from Docupilot. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from Docupilot. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Docupilot. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Copy Template](actions/copy-template.md) | POST | Copies a template in Docupilot. |
| [Create Template](actions/create-template.md) | POST | Creates a template in Docupilot. |
| [Create Template Delivery](actions/create-template-delivery.md) | POST | Creates a template delivery in Docupilot. |
| [Create Template Merge Link](actions/create-template-merge-link.md) | POST | Creates a template merge link in Docupilot. |
| [Delete Template](actions/delete-template.md) | DELETE | Moves a template to trash in Docupilot. |
| [Delete Template Delivery](actions/delete-template-delivery.md) | DELETE | Deletes a template delivery from Docupilot. |
| [Delete Template Merge Link](actions/delete-template-merge-link.md) | DELETE | Deletes a template merge link from Docupilot. |
| [Delete Template Permanently](actions/delete-template-permanently.md) | DELETE | Permanently deletes a trashed template from Docupilot. |
| [Get Content Block](actions/get-content-block.md) | GET | Retrieves a content block from Docupilot. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from Docupilot. |
| [Get Template Delivery](actions/get-template-delivery.md) | GET | Retrieves a template delivery from Docupilot. |
| [Get Template Schema](actions/get-template-schema.md) | GET | Retrieves a template schema from Docupilot. |
| [Get Template Test Data](actions/get-template-test-data.md) | GET | Retrieves template test data from Docupilot. |
| [List Content Blocks](actions/list-content-blocks.md) | GET | Retrieves content blocks from Docupilot. |
| [List Template Deliveries](actions/list-template-deliveries.md) | GET | Retrieves template deliveries from Docupilot. |
| [List Template Merge Links](actions/list-template-merge-links.md) | GET | Retrieves template merge links from Docupilot. |
| [List Templates](actions/list-templates.md) | GET | Retrieves templates from Docupilot. |
| [List Trashed Templates](actions/list-trashed-templates.md) | GET | Retrieves trashed templates from Docupilot. |
| [Restore Template From Trash](actions/restore-template-from-trash.md) | PUT | Restores a template from trash in Docupilot. |
| [Update Template](actions/update-template.md) | PUT | Updates an existing template in Docupilot. |
| [Update Template Content](actions/update-template-content.md) | PUT | Updates template content in Docupilot. |
| [Update Template Delivery](actions/update-template-delivery.md) | PUT | Updates an existing template delivery in Docupilot. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Workspace](actions/get-current-workspace.md) | GET | Retrieves current workspace details from Docupilot. |

