# List Affiliates with Eduzz

Retrieves affiliates from Eduzz using the provided filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/myeduzz/v1/affiliates`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [List Affiliates](https://developers.eduzz.com/reference/api/get-myeduzz-v1-affiliates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productIds` | query | `string` | no | Comma-separated product ids to filter affiliates. |
