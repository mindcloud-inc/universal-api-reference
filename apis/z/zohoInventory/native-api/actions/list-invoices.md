# List Invoices with Zoho Inventory

Retrieves invoices from Zoho Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/invoices`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [List Invoices](https://www.zoho.com/inventory/api/v1/invoices/#list-invoices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
