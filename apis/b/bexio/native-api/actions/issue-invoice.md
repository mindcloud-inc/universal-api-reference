# Issue Invoice with Bexio

Issues an invoice in Bexio.

## Endpoint

- **Method:** `POST`
- **Path:** `/2.0/kb_invoice/:invoice_id/issue`
- **Base URL:** `https://api.bexio.com`
- **Official documentation:** [Issue Invoice](https://docs.bexio.com/#tag/Invoices/operation/v2IssueInvoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `number` | yes | The ID of the invoice. |
