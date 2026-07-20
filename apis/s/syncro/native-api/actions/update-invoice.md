# Update Invoice with Syncro

Updates an existing invoice in Syncro.

## Endpoint

- **Method:** `PUT`
- **Path:** `/invoices/:id`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [Update Invoice](https://api-docs.syncromsp.com/#/Invoice/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required invoice ID to update. |
| `customer_id` | body | `number` | no | — |
| `number` | body | `string` | no | — |
| `date` | body | `date` | no | — |
| `customer_business_then_name` | body | `string` | no | — |
| `created_at` | body | `date` | no | — |
| `updated_at` | body | `date` | no | — |
| `due_date` | body | `date` | no | — |
| `subtotal` | body | `string` | no | — |
| `total` | body | `string` | no | — |
| `tax` | body | `string` | no | — |
| `ticket_id` | body | `number` | no | — |
| `pdf_url` | body | `string` | no | — |
| `location_id` | body | `number` | no | — |
| `po_number` | body | `string` | no | — |
| `contact_id` | body | `number` | no | — |
| `note` | body | `string` | no | — |
| `hardwarecost` | body | `number` | no | — |
