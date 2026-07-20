# List Positions with Planday

Retrieves a list of positions from Planday.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheduling/v1.0/positions`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [List Positions](https://openapi.planday.com/api/schedule/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `isActive` | query | `boolean` | no |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
