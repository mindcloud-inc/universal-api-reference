# Submit Payment Form with TrueLayer

Submits a payment authorization form in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments/:id/authorization-flow/actions/form`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Submit Payment Form](https://docs.truelayer.com/reference/submit-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payment ID. |
