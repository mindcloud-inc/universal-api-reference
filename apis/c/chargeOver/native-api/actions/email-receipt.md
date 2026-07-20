# Email Receipt with ChargeOver

Emails a transaction receipt from ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/transaction/:transaction_id/_action/email`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Email Receipt](https://developer.chargeover.com/docs/api/email-a-receipt/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The ChargeOver transaction ID. |
