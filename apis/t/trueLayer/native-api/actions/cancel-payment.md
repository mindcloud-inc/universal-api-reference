# Cancel Payment with TrueLayer

Cancels a payment in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments/:id/actions/cancel`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Cancel Payment](https://docs.truelayer.com/reference/cancel-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payment ID. |
