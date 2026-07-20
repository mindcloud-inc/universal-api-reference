# Create File with Orq.ai

Uploads a file to Orq.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/files`
- **Base URL:** `https://api.orq.ai`
- **Official documentation:** [Create File](https://docs.orq.ai/reference/files/create-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `purpose` | body | `string` | yes |
