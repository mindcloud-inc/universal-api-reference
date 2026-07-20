# Get all fact metrics with GrowthBook

Retrieves fact metrics from your GrowthBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/fact-metrics`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get all fact metrics](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
| `datasourceId` | query | `string` | no | Filter by Data Source |
| `projectId` | query | `string` | no | Filter by project id |
| `factTableId` | query | `string` | no | Filter by Fact Table Id (for ratio metrics, we only look at the numerator) |
