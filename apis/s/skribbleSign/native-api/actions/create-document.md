# Create Document with Skribble Sign

Creates a new document in Skribble Sign.

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
| `title` | body | `string` | no | The document title. |
| `content` | body | `string` | yes | The base64 encoded PDF content. |
