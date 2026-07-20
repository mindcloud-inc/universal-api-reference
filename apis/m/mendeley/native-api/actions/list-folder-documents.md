# List Folder Documents with Mendeley

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:id/documents`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [List Folder Documents](https://dev.mendeley.com/methods/#retrieving-documents-in-a-folder)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the folder. |
