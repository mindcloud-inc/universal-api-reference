# Submit Payment Branch Selection with TrueLayer

Submits payment branch selection in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments/:id/authorization-flow/actions/branch-selection`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Submit Payment Branch Selection](https://docs.truelayer.com/reference/submit-branch-selection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payment ID. |
