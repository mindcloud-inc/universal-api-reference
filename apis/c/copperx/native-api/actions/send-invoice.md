# Send Invoice with Copperx

Sends an invoice and finalizes it if needed in Copperx.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/{id}/send`
- **Base URL:** `https://api.copperx.dev/api/v1`
- **Official documentation:** [Send Invoice](https://copperx.readme.io/reference/invoicecontroller_finalizeandsendinvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Invoice ID path parameter. |
