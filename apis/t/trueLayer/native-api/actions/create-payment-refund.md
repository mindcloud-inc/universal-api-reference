# Create Payment Refund with TrueLayer

Creates a payment refund in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments/:id/refunds`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Create Payment Refund](https://docs.truelayer.com/reference/create-payment-refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payment ID. |
