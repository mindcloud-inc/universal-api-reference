# Get Payment Refund with TrueLayer

Retrieves a payment refund from TrueLayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/payments/:payment_id/refunds/:refund_id`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Get Payment Refund](https://docs.truelayer.com/reference/get-payment-refund)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payment_id` | path | `string` | yes | TrueLayer payment ID. |
| `refund_id` | path | `string` | yes | TrueLayer refund ID. |
