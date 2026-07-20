# List Shift Types with Planday

Retrieves a list of shift types from Planday.

## Endpoint

- **Method:** `GET`
- **Path:** `/scheduling/v1.0/shifttypes`
- **Base URL:** `https://openapi.planday.com`
- **Official documentation:** [List Shift Types](https://openapi.planday.com/api/schedule/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `isActive` | query | `boolean` | no |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
