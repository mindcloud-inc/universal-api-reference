# Submit Payment Scheme Selection with TrueLayer

Submits payment scheme selection in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments/:id/authorization-flow/actions/scheme-selection`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Submit Payment Scheme Selection](https://docs.truelayer.com/reference/submit-scheme-selection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payment ID. |
