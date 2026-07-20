# List Subscriptions with Smartcar

Retrieves subscriptions from Smartcar.

## Endpoint

- **Method:** `GET`
- **Path:** `https://management.api.smartcar.com/v3/subscriptions`
- **Base URL:** `https://vehicle.api.smartcar.com/v3`
- **API:** rest
- **Official documentation:** [List Subscriptions](https://smartcar.com/docs/api-reference/list-subscriptions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[userId]` | query | `string` | no | Filter subscriptions by user ID. |
| `filter[vehicle.mode]` | query | `string` | no | Filter subscriptions by vehicle mode. |
| `filter[vehicleId]` | query | `string` | no | Filter subscriptions by vehicle ID. |
| `filter[webhookId]` | query | `string` | no | Filter subscriptions by webhook ID. |
