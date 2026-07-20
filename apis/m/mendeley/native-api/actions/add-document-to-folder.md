# Add Document To Folder with Mendeley

## Endpoint

- **Method:** `POST`
- **Path:** `/folders/:id/documents`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Add Document To Folder](https://dev.mendeley.com/methods/#adding-a-document-to-a-folder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the folder. |
| `id` | body | `string` | yes | Identifier of the document to add to the folder. |
