# Update Invoice with FreeAgent

Updates an existing invoice in FreeAgent.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:id`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Update Invoice](https://dev.freeagent.com/docs/invoices#update-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | FreeAgent invoice ID. |
| `invoice` | body | `object` | no | Invoice payload. |
| `invoice.contact` | body | `string` | no | Contact being invoiced. |
| `invoice.project` | body | `string` | no | Project being invoiced. |
| `invoice.reference` | body | `string` | no | Invoice reference. |
| `invoice.dated_on` | body | `date` | no | Date of invoice in YYYY-MM-DD format. |
| `invoice.due_on` | body | `date` | no | When invoice is due, in YYYY-MM-DD format. |
| `invoice.payment_terms_in_days` | body | `number` | no | Set to zero to display Due on Receipt on the invoice. |
| `invoice.currency` | body | `string` | no | Invoice currency. |
| `invoice.comments` | body | `string` | no | Additional text added to the bottom of the invoice. |
