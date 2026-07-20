# Get list of all code references for the current organization with GrowthBook

Retrieves code references from your GrowthBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/code-refs`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get list of all code references for the current organization](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
