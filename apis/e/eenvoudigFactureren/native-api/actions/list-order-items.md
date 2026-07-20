# List Order Items with EenvoudigFactureren

Retrieves order items from EenvoudigFactureren.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/:order_id/items`
- **Base URL:** `https://eenvoudigfactureren.be/api/v1`
- **Official documentation:** [List Order Items](https://help.eenvoudigfactureren.be/support/solutions/articles/101000381990-api-bestelbonnen)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `string` | yes | EenvoudigFactureren order ID. |
