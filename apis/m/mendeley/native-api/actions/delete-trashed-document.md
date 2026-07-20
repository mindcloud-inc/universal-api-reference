# Delete Trashed Document with Mendeley

## Endpoint

- **Method:** `DELETE`
- **Path:** `/trash/:id`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Delete Trashed Document](https://dev.mendeley.com/methods/#deleting-a-trashed-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier (UUID) of the document. |
