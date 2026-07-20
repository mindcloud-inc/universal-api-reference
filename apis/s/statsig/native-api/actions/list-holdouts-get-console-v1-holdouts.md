# List Holdouts with Statsig

Retrieves holdouts from Statsig.

## Endpoint

- **Method:** `GET`
- **Path:** `/console/v1/holdouts`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [List Holdouts](https://docs.statsig.com/api-reference/holdouts/list-holdouts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `creatorName` | query | `string` | no | Name of the creator. |
| `creatorID` | query | `string` | no | ID of the user who created the entity. |
| `tags` | query | `string` | no | Filter by tags |
| `limit` | query | `number` | no | Results per page |
| `page` | query | `number` | no | Page number |
