# Deliver Receipt with Quaderno

Delivers a receipt to the customer by email in Quaderno.

## Endpoint

- **Method:** `GET`
- **Path:** `/receipts/:id/deliver`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Deliver Receipt](https://developers.quaderno.io/api/#tag/Receipts/operation/deliverReceipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the desired receipt. |
