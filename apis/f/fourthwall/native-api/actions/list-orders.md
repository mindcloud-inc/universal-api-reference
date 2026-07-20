# List Orders with Fourthwall

Retrieves a paginated list of orders from Fourthwall.

## Endpoint

- **Method:** `GET`
- **Path:** `/open-api/v1.0/order`
- **Base URL:** `https://api.fourthwall.com`
- **Official documentation:** [List Orders](https://docs.fourthwall.com/api-reference/platform/orders/list-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter orders by customer email. |
| `createdAt[gt]` | query | `date` | no | Filter orders created after this timestamp. |
| `createdAt[lt]` | query | `date` | no | Filter orders created before this timestamp. |
| `updatedAt[gt]` | query | `date` | no | Filter orders updated after this timestamp. |
| `updatedAt[lt]` | query | `date` | no | Filter orders updated before this timestamp. |
| `status` | query | `list` | no | Filter orders by status. Accepted values: `CANCELLED`, `COMPLETED`, `CONFIRMED`, `DELIVERED`, `IN_PRODUCTION`, `PARTIALLY_DELIVERED`, `PARTIALLY_IN_PRODUCTION`, `PARTIALLY_SHIPPED`, `SHIPPED`. Send multiple values as a array. |
