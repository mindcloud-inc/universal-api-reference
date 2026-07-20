# List Batches with xAI

Retrieves batches from the xAI API.

## Endpoint

- **Method:** `GET`
- **Path:** `/batches`
- **Base URL:** `https://api.x.ai/v1`
- **Official documentation:** [List Batches](https://docs.x.ai/developers/rest-api-reference/inference/batches#list-batches)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of batches to return. |
| `pagination_token` | query | `string` | no | Page token from a previous list batches response. |
