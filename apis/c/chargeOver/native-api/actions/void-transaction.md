# Void Transaction with ChargeOver

Voids an existing transaction in ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/transaction/:transaction_id/_action/void`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Void Transaction](https://developer.chargeover.com/docs/api/void-a-transaction/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The ChargeOver transaction ID. |
