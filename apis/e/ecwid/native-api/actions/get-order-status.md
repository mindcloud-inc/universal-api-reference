# Get Order Status with Ecwid

Retrieves an order status from Ecwid.

## Endpoint

- **Method:** `GET`
- **Path:** `/:storeId/profile/order_status/:statusId`
- **Base URL:** `https://app.ecwid.com/api/v3`
- **Official documentation:** [Get Order Status](https://docs.ecwid.com/api-reference/rest-api/orders/order-statuses/get-order-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `statusId` | path | `string` | yes | Ecwid order status ID. |
