# <img src="https://images.mindcloud.co/apps/icons/dynalist_1776085335380.png" alt="Dynalist logo" width="28" height="28"> Dynalist: Universal API

Dynalist is an outlining and note organization service for documents, folders, inbox items, and document nodes.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dynalist/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dynalist.io/
- **Vendor API docs:** https://apidocs.dynalist.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Documents And Folders](actions/list-documents-and-folders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynalist/latest/actions/list-documents-and-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Read Document](actions/read-document.md) | GET | Retrieves a document from Dynalist. |

### Document Node

| Action | Method | Description |
| --- | --- | --- |
| [Batch Edit Document Nodes](actions/batch-edit-document-nodes.md) | PUT | Updates multiple document nodes in Dynalist. |
| [Delete Node](actions/delete-node.md) | DELETE | Deletes a document node from Dynalist. |
| [Insert Node](actions/insert-node.md) | POST | Creates a new document node in Dynalist. |
| [Move Node](actions/move-node.md) | PUT | Moves a document node in Dynalist. |
| [Update Node](actions/update-node.md) | PUT | Updates a document node in Dynalist. |

### Document Or Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Documents And Folders](actions/list-documents-and-folders.md) | GET | Retrieves documents and folders from Dynalist. |

### Document Version

| Action | Method | Description |
| --- | --- | --- |
| [Check Documents For Updates](actions/check-documents-for-updates.md) | GET | Checks Dynalist documents for updates. |

### File Or Folder

| Action | Method | Description |
| --- | --- | --- |
| [Batch Edit Files And Folders](actions/batch-edit-files-and-folders.md) | PUT | Updates multiple files and folders in Dynalist. |
| [Create File](actions/create-file.md) | POST | Creates a new file or folder in Dynalist. |
| [Move File](actions/move-file.md) | PUT | Moves a file or folder in Dynalist. |
| [Rename File](actions/rename-file.md) | PUT | Renames a file or folder in Dynalist. |

### Inbox Item

| Action | Method | Description |
| --- | --- | --- |
| [Send Item To Inbox](actions/send-item-to-inbox.md) | POST | Creates a new inbox item in Dynalist. |

### Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get Preference](actions/get-preference.md) | GET | Retrieves a preference value from Dynalist. |
| [Set Preference](actions/set-preference.md) | PUT | Updates a preference value in Dynalist. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Dynalist. |

