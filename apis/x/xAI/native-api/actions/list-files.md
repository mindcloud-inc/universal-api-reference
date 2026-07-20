# List Files with xAI

Retrieves files from the xAI API.

## Endpoint

- **Method:** `GET`
- **Path:** `/files`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [List Files](https://docs.x.ai/developers/rest-api-reference/files/manage#list-files)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of files to return. |
| `pagination_token` | query | `string` | no | Pagination token returned by a previous list files response. |
