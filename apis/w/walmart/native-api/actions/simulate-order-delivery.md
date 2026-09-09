# Simulate Order Delivery with Walmart

This request updates an order with delivery information in the Marketplace dynamic sandbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/simulations/orders/:purchaseOrderId/deliver`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Simulate Order Delivery](https://developer.walmart.com/us-marketplace/reference/simulatereturn)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderLines.orderLine[]` | body | `array` | no | — |
| `orderLines.orderLine[].lineNumber` | body | `number` | no | Line number of an item within the order to return. |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[]` | body | `array<object>` | no | — |
| `orderLines.orderLine[].orderLineStatuses.orderLineStatus[].status` | body | `string` | no | Allowed: 'Delivered' |
| `purchaseOrderId` | path | `string` | yes | Purchase order identifier for the order being used in the return simulation. |
| `orderLines.orderLine[].orderLineStatuses` | body | `object` | no | Order line status information. |
| `orderLines` | body | `object` | no | — |
