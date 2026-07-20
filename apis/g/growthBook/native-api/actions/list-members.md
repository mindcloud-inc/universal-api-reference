# Get all organization members with GrowthBook

Retrieves organization members from your GrowthBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/members`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get all organization members](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
| `userName` | query | `string` | no | Name of the user. |
| `userEmail` | query | `string` | no | Email address of the user. |
| `globalRole` | query | `string` | no | Name of the global role |
