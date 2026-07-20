# Get Repeat Order URL with Ecwid

Retrieves a repeat order URL from Ecwid.

## Endpoint

- **Method:** `GET`
- **Path:** `/:storeId/orders/:orderId/repeatURL`
- **Base URL:** `https://app.ecwid.com/api/v3`
- **Official documentation:** [Get Repeat Order URL](https://docs.ecwid.com/api-reference/rest-api/orders/get-repeat-order-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Ecwid order ID. |
