# List Orders with SalesDrive

Retrieves a list of orders from SalesDrive.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/order/list/`
- **Base URL:** `https://{account}.salesdrive.me`
- **Official documentation:** [List Orders](https://api.salesdrive.me/api/docs/#/order/order-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[updateAt][from]` | query | `string` | no | Filter orders updated from this value. |
| `filter[updateAt][to]` | query | `string` | no | Filter orders updated to this value. |
| `filter[orderTime][from]` | query | `string` | no | Filter orders by order time from this value. |
| `filter[orderTime][to]` | query | `string` | no | Filter orders by order time to this value. |
| `filter[statusId]` | query | `string` | no | Filter orders by status ID. |
| `filter[id][from]` | query | `number` | no | Filter orders with IDs from this value. |
| `filter[id][to]` | query | `number` | no | Filter orders with IDs to this value. |
| `filter[organizationId]` | query | `number` | no | Filter orders by organization ID. |
