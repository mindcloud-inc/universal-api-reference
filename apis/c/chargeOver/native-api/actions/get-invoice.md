# Get Invoice with ChargeOver

Retrieves detailed invoice records from ChargeOver.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoice/:invoice_id`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Get Invoice](https://developer.chargeover.com/docs/api/get-a-specific-invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `number` | yes | The ChargeOver invoice ID. |
