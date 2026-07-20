# Parse Document with Langbase

## Endpoint

- **Method:** `POST`
- **Path:** `v1/parser`
- **Base URL:** `https://api.langbase.com`
- **Official documentation:** [Parse Document](https://langbase.com/docs/api-reference/parser)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document` | body | `file` | yes | Document file to parse. |
| `documentName` | body | `string` | yes | Display name for the uploaded document. |
