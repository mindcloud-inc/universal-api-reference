# Create Document with Documenso

Creates a new document in Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/create`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Create Document](https://docs.documenso.com/docs/developers/api/documents)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `payload` | body | `object` | yes |
| `files` | body | `file` | yes |
