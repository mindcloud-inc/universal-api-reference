# Remove Document From Folder with Mendeley

## Endpoint

- **Method:** `DELETE`
- **Path:** `/folders/:id/documents/:document_id`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Remove Document From Folder](https://dev.mendeley.com/methods/#deleting-a-document-from-a-folder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the folder. |
| `document_id` | path | `string` | yes | Identifier of the document to remove from the folder. |
