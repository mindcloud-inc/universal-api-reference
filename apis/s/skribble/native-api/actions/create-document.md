# Create Document with Skribble

Creates a document in Skribble from a PDF upload.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/documents`
- **Base URL:** `https://api.skribble.com`
- **Official documentation:** [Create Document](https://api-doc.skribble.com/#9cf195d0-bec5-4037-899d-1919b003b347)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | The base64 encoded PDF content. |
| `title` | body | `string` | no | The document title. |
