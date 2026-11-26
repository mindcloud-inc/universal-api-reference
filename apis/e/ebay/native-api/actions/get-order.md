# Get Order with eBay

Use this call to retrieve the contents of an order based on its unique identifier, orderId. This value is returned in the getOrders call's orders.orderId field when you search for orders by creation date, modification date, or fulfillment status.

## Endpoint

- **Method:** `GET`
- **Path:** `sell/fulfillment/v1/order/{orderID}`
- **Base URL:** `https://api.ebay.com/`
- **API:** REST
- **Official documentation:** [Get Order](https://developer.ebay.com/api-docs/sell/fulfillment/resources/order/methods/getOrders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderID` | query | `string` | yes |
