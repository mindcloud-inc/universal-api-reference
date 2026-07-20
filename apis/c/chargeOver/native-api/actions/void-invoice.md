# Void Invoice with ChargeOver

Voids an existing invoice in ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/:invoice_id/_action/void`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Void Invoice](https://developer.chargeover.com/docs/api/void-an-invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `number` | yes | The ChargeOver invoice ID. |
