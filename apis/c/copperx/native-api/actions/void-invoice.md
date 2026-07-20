# Void Invoice with Copperx

Voids an existing invoice in Copperx.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices/{id}/void`
- **Base URL:** `https://api.copperx.dev/api/v1`
- **Official documentation:** [Void Invoice](https://copperx.readme.io/reference/invoicecontroller_voidinvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Invoice ID path parameter. |
