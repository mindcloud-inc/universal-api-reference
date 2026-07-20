# Email Invoice with ChargeOver

Emails an existing invoice from ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/:invoice_id/_action/email`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Email Invoice](https://developer.chargeover.com/docs/api/email-an-invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `number` | yes | The ChargeOver invoice ID. |
