# Get Invoice with Metronome

Retrieves an invoice from Metronome.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers/:customer_id/invoices/:invoice_id`
- **Base URL:** `https://api.metronome.com`
- **Official documentation:** [Get Invoice](https://docs.metronome.com/api-reference/invoices/get-an-invoice)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customer_id` | path | `string` | yes |
| `invoice_id` | path | `string` | yes |
