# Start Payment Authorization Flow with TrueLayer

Starts a payment authorization flow in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments/:id/authorization-flow`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Start Payment Authorization Flow](https://docs.truelayer.com/reference/start-payment-authorization-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payment ID. |
