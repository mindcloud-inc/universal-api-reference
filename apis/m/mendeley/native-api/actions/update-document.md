# Update Document with Mendeley

## Endpoint

- **Method:** `PATCH`
- **Path:** `/documents/:id`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Update Document](https://dev.mendeley.com/methods/#updating-documents)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |
| `Content-Type` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the document. |
| `title` | body | `string` | yes | Updated document title. |
