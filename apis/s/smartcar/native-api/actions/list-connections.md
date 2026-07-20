# List Connections with Smartcar

Retrieves connections from Smartcar.

## Endpoint

- **Method:** `GET`
- **Path:** `/connections`
- **Base URL:** `https://vehicle.api.smartcar.com/v3`
- **API:** rest
- **Official documentation:** [List Connections](https://smartcar.com/docs/api-reference/list-connections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[userId]` | query | `string` | no | Filter connections by Smartcar user ID. |
| `filter[vehicle.mode]` | query | `string` | no | Filter connections by vehicle mode. |
| `filter[vehicleId]` | query | `string` | no | Filter connections by vehicle ID. |
