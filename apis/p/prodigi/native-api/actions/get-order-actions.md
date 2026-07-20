# Get Order Actions with Prodigi

Retrieves available actions for a Prodigi order.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/[:prodigiOrderId]/actions`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [Get Order Actions](https://www.prodigi.com/print-api/docs/reference/#get-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prodigiOrderId` | path | `string` | yes | Prodigi order ID, such as ord_123456. |
