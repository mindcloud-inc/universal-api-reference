# Submit Payment User Account Selection with TrueLayer

Submits payment user account selection in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments/:id/authorization-flow/actions/user-account-selection`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Submit Payment User Account Selection](https://docs.truelayer.com/reference/submit-user-account-selection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payment ID. |
