# Get all metrics with GrowthBook

Retrieves metrics from your GrowthBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/metrics`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get all metrics](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
| `projectId` | query | `string` | no | Filter by project id |
| `datasourceId` | query | `string` | no | Filter by Data Source |
