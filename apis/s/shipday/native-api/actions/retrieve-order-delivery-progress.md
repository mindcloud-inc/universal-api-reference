# Retrieve Order Delivery Progress with Shipday

Retrieves order delivery progress from Shipday.

## Endpoint

- **Method:** `GET`
- **Path:** `/order/progress/:trackingId`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Retrieve Order Delivery Progress](https://docs.shipday.com/reference/order-delivery-progress)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackingId` | path | `string` | yes | Shipday tracking token from the order tracking link. |
