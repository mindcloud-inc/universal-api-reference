# Legacy Submit Embedded Payment Step with TrueLayer

Submits a legacy embedded payment step in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/single-immediate-payment-initiation-requests/:id/authorization-flow/actions`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Legacy Submit Embedded Payment Step](https://docs.truelayer.com/reference/get-providers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer legacy payment initiation request ID. |
