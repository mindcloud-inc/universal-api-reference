# Submit Payment Provider Selection with TrueLayer

Submits payment provider selection in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments/:id/authorization-flow/actions/provider-selection`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Submit Payment Provider Selection](https://docs.truelayer.com/reference/submit-provider-selection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payment ID. |
