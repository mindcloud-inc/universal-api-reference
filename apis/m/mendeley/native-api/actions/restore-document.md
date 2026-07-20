# Restore Document with Mendeley

## Endpoint

- **Method:** `POST`
- **Path:** `/trash/:id/restore`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Restore Document](https://dev.mendeley.com/methods/#restoring-a-document)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier (UUID) of the document. |
