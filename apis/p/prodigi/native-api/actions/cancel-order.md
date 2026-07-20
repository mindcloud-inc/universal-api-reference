# Cancel Order with Prodigi

Cancels a specific order in Prodigi.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/[:prodigiOrderId]/actions/cancel`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [Cancel Order](https://www.prodigi.com/print-api/docs/reference/#cancel-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prodigiOrderId` | path | `string` | yes | Prodigi order ID to cancel. |
