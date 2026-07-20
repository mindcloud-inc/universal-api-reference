# Get all filters for a fact table with GrowthBook

Retrieves filters for a GrowthBook fact table.

## Endpoint

- **Method:** `GET`
- **Path:** `/fact-tables/:factTableId/filters`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get all filters for a fact table](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `factTableId` | path | `string` | yes | Specify a specific fact table |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
