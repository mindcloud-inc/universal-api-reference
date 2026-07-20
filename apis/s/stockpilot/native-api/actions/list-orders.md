# List Orders with Stockpilot

Retrieves orders from Stockpilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [List Orders](https://api.stockpilot.dev/redoc#operation/get_orders_list_orders_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status` | query | `string` | no |
| `is_forwarded` | query | `string` | no |
