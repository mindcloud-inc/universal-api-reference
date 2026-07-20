# Download File with Mistral AI

Retrieves file content from Mistral AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/files/:file_id/content`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Download File](https://docs.mistral.ai/api/endpoint/files#operation-files_api_routes_download_file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | The ID of the file. |
