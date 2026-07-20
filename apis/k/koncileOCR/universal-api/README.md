# <img src="https://images.mindcloud.co/apps/icons/koncile-icon-256_1776956976194.png" alt="Koncile OCR logo" width="28" height="28"> Koncile OCR: Universal API

Koncile OCR is an AI-powered document extraction platform for managing folders, templates, fields, instructions, uploads, tasks, and extracted document data through the Koncile REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/koncileOCR/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.koncile.ai/en
- **Vendor API docs:** https://docs.koncile.ai/api-setup/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check API Key](actions/check-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/koncileOCR/latest/actions/check-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Check API Key](actions/check-api-key.md) | GET |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Delete Document](actions/delete-document.md) | DELETE |  |
| [Get Document Data](actions/get-document-data.md) | GET |  |
| [List Documents](actions/list-documents.md) | GET |  |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST |  |
| [Delete Field](actions/delete-field.md) | DELETE |  |
| [Get Field](actions/get-field.md) | GET |  |
| [Update Field](actions/update-field.md) | PUT |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET |  |
| [Download Files Batch](actions/download-files-batch.md) | GET |  |
| [Upload File](actions/upload-file.md) | POST |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Delete Folder](actions/delete-folder.md) | DELETE |  |
| [Get Folder](actions/get-folder.md) | GET |  |
| [List Folders](actions/list-folders.md) | GET |  |
| [Update Folder](actions/update-folder.md) | PUT |  |

### Instruction

| Action | Method | Description |
| --- | --- | --- |
| [Create Instruction](actions/create-instruction.md) | POST |  |
| [Delete Instruction](actions/delete-instruction.md) | DELETE |  |
| [Get Instruction](actions/get-instruction.md) | GET |  |
| [Update Instruction](actions/update-instruction.md) | PUT |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Task Result](actions/retrieve-task-result.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST |  |
| [Delete Template](actions/delete-template.md) | DELETE |  |
| [Get Template](actions/get-template.md) | GET |  |
| [Update Template](actions/update-template.md) | PUT |  |

