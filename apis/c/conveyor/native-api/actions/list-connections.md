# List Connections with Conveyor

Retrieves connections from Conveyor with optional filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/exchange/connections`
- **Base URL:** `https://api.conveyor.com/api`
- **Official documentation:** [List Connections](https://docs.conveyor.com/reference/get-connections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | no | Filter by bare domain, for example example.com. Do not include https:// or www. |
