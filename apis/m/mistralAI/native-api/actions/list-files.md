# List Files with Mistral AI

Retrieves available files from Mistral AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/files`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [List Files](https://docs.mistral.ai/api/endpoint/files#operation-files_api_routes_list_files)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_total` | query | `boolean` | no | Include the total count in the file list response. |
| `sample_type[]` | query | `array<string>` | no | Optional sample type filter list. |
| `source[]` | query | `array<string>` | no | Optional source filter list. |
| `search` | query | `string` | no | Free-text search filter. |
| `purpose` | query | `string` | no | Optional file purpose filter. |
| `mimetypes[]` | query | `array<string>` | no | Optional mimetype filter list. |
