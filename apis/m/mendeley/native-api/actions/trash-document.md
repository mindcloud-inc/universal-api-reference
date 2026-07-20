# Trash Document with Mendeley

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:id/trash`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Trash Document](https://dev.mendeley.com/methods/#move-a-document-to-the-trash)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier (UUID) of the document. |
