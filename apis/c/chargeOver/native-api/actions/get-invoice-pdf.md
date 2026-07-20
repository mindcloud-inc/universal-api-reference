# Get Invoice PDF with ChargeOver

Retrieves an invoice PDF from ChargeOver.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice/:invoice_id/_action/pdf`
- **Base URL:** `https://{siteName}.chargeover.com/api/v3`
- **Official documentation:** [Get Invoice PDF](https://developer.chargeover.com/docs/api/get-a-pdf-of-an-invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `number` | yes | The ChargeOver invoice ID. |
