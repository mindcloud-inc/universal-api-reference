# Create Invoice with FreeAgent

Creates a new invoice in FreeAgent.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoices`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Create Invoice](https://dev.freeagent.com/docs/invoices#create-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice` | body | `object` | no | Invoice payload. |
| `invoice.contact` | body | `string` | yes | Contact being invoiced. |
| `invoice.project` | body | `string` | no | Project being invoiced. |
| `invoice.reference` | body | `string` | no | Invoice reference. |
| `invoice.dated_on` | body | `date` | yes | Date of invoice in YYYY-MM-DD format. |
| `invoice.due_on` | body | `date` | no | When invoice is due, in YYYY-MM-DD format. |
| `invoice.payment_terms_in_days` | body | `number` | yes | Set to zero to display Due on Receipt on the invoice. |
| `invoice.currency` | body | `string` | no | Invoice currency. |
| `invoice.comments` | body | `string` | no | Additional text added to the bottom of the invoice. |
