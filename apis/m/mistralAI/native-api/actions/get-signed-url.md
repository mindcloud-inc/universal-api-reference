# Get Signed URL with Mistral AI

Retrieves a signed file URL from Mistral AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/files/:file_id/url`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Get Signed URL](https://docs.mistral.ai/api/endpoint/files#operation-files_api_routes_get_signed_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | The ID of the file. |
| `expiry` | query | `number` | no | Number of hours before the signed URL expires. |
