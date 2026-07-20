# List Batch Results with xAI

Retrieves batch results from the xAI API.

## Endpoint

- **Method:** `GET`
- **Path:** `/batches/:batch_id/results`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [List Batch Results](https://docs.x.ai/developers/rest-api-reference/inference/batches#list-batch-results)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | no | Batch identifier whose results should be listed. |
| `pagination_token` | query | `string` | no | Page token from a previous list results response. |
| `limit` | query | `number` | no | Maximum results to return. |
