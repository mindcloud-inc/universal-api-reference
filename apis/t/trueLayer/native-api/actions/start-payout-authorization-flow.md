# Start Payout Authorization Flow with TrueLayer

Starts a payout authorization flow in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payouts/:id/authorization-flow`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Start Payout Authorization Flow](https://docs.truelayer.com/reference/start-payout-authorization-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | TrueLayer payout ID. |
