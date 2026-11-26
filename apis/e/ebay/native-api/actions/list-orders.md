# List Orders with eBay

## Endpoint

- **Method:** `GET`
- **Path:** `sell/fulfillment/v1/order`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [List Orders](https://developer.ebay.com/api-docs/sell/fulfillment/resources/order/methods/getOrders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `creationDateStart` | query | `string` | no | — |
| `creationDateEnd` | query | `string` | no | — |
| `lastModifiedDateStart` | query | `string` | no | — |
| `lastModifiedDateEnd` | query | `string` | no | — |
| `orderfulfillmentstatus` | query | `list` | no | **Not Started - In Progress**: specifies orders for which no shipping fulfillments have been started, plus orders for which at least one shipping fulfillment has been started but not completed.  **Fulfilled - In Progress**:specifies orders for which all shipping fulfillments have been completed, plus orders for which at least one shipping fulfillment has been started but not completed. |
