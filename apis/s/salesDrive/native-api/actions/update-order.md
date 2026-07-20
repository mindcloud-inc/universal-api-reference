# Update Order with SalesDrive

Updates an existing order in SalesDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/order/update/`
- **Base URL:** `https://{account}.salesdrive.me`
- **Official documentation:** [Update Order](https://api.salesdrive.me/api/docs/#/order/order-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | body | `string` | no | External order number; ignored when Order ID is provided. |
| `id` | body | `number` | no | SalesDrive order number. |
| `data` | body | `object` | no | Order fields to update. |
