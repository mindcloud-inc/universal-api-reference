# List Batch Requests with xAI

Retrieves batch requests from the xAI API.

## Endpoint

- **Method:** `GET`
- **Path:** `/batches/:batch_id/requests`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [List Batch Requests](https://docs.x.ai/developers/rest-api-reference/inference/batches#list-batch-requests)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batch_id` | path | `string` | no | Unique batch identifier. |
