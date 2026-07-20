# Download File with Dify

Retrieves a file preview or download from Dify.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:file_id/preview`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Download File](https://docs.dify.ai/api-reference/files/download-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | Uploaded file ID to download. |
| `as_attachment` | query | `boolean` | no | Whether to force download as an attachment. |
| `user` | query | `string` | no | User identifier. |
