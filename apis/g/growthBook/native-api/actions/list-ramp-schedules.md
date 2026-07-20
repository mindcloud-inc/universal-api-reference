# Get all rampSchedules with GrowthBook

Retrieves ramp schedules from your GrowthBook organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/ramp-schedules`
- **Base URL:** `https://api.growthbook.io/api/v1`
- **Official documentation:** [Get all rampSchedules](https://docs.growthbook.io/api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | The number of items to return |
| `offset` | query | `number` | no | How many items to skip (use in conjunction with limit for pagination) |
| `featureId` | query | `string` | no | — |
| `status` | query | `string` | no | Filter by schedule status |
