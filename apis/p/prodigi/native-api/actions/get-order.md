# Get Order with Prodigi

Retrieves details for a specific Prodigi order.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/[:prodigiOrderId]`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [Get Order](https://www.prodigi.com/print-api/docs/reference/#get-order-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prodigiOrderId` | path | `string` | yes | Prodigi order ID, such as ord_123456. |
