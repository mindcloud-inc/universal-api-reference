# Search Order Extra Fields with Ecwid

Finds order extra fields in Ecwid.

## Endpoint

- **Method:** `GET`
- **Path:** `/:storeId/orders/:orderId/extraFields`
- **Base URL:** `https://app.ecwid.com/api/v3`
- **Official documentation:** [Search Order Extra Fields](https://docs.ecwid.com/api-reference/rest-api/orders/order-extra-fields/search-order-extra-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `number` | yes | Ecwid order ID. |
