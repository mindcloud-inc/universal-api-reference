# Get all experiments with GrowthBook

Retrieves experiments from your GrowthBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/experiments`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get all experiments](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
| `projectId` | query | `string` | no | Filter by project id |
| `datasourceId` | query | `string` | no | Filter by Data Source |
| `experimentId` | query | `string` | no | Filter the returned list by the experiment tracking key (id) |
| `status` | query | `string` | no | — |
