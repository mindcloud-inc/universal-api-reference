# Get Invoice with Zoho Inventory

Retrieves an invoice from Zoho Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices/:invoice_id`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Get Invoice](https://www.zoho.com/inventory/api/v1/invoices/#get-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice_id` | path | `string` | yes | The Zoho Inventory invoice_id for the invoice. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
