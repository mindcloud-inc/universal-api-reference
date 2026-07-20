# Create Document with Mendeley

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://api.mendeley.com`
- **Official documentation:** [Create Document](https://dev.mendeley.com/methods/#creating-a-document-from-metadata)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.mendeley-document.1+json` |
| `Content-Type` | `application/vnd.mendeley-document.1+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Title of the document to create. |
| `type` | body | `list` | yes | Document type. Accepted values: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `17`, `18`, `19`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
