# Add Order Note with SalesDrive

Adds a note to an order in SalesDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/order/note/`
- **Base URL:** `https://{account}.salesdrive.me`
- **Official documentation:** [Add Order Note](https://api.salesdrive.me/api/docs/#/order/order-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | body | `number` | yes | SalesDrive order number. |
| `text` | body | `string` | yes | Note text. |
