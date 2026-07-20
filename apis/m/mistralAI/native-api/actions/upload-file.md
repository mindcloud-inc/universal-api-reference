# Upload File with Mistral AI

Uploads a new file to Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Upload File](https://docs.mistral.ai/api/endpoint/files#operation-files_api_routes_upload_file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file object to upload. |
| `purpose` | body | `string` | no | Optional file purpose. |
| `expiry` | body | `number` | no | Optional expiry in hours. |
| `visibility` | body | `string` | no | File visibility setting. |
