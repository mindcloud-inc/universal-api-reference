# Submit Payment Consent with TrueLayer

Submits payment consent in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments/:id/authorization-flow/actions/consent`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Submit Payment Consent](https://docs.truelayer.com/reference/submit-consent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payment ID. |
