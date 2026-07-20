# Upload Document with Column

## Endpoint

- **Method:** `POST`
- **Path:** `/documents`
- **Base URL:** `https://api.column.com`
- **Official documentation:** [Upload Document](https://column.com/docs/api/#documents/upload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Document file to upload. |
| `type` | body | `list` | yes | Document type. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
| `description` | body | `string` | no | Description of the document. |
| `tag` | body | `string` | no | Optional tag for document identification. |
