# Create Package with Zoho Inventory

Creates a new package in Zoho Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/packages`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Create Package](https://www.zoho.com/inventory/api/v1/packages/#creating-a-package)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
| `salesorder_id` | query | `string` | yes | — |
| `package_number` | body | `string` | no | — |
| `date` | body | `string` | yes | — |
| `notes` | body | `string` | no | — |
| `line_items[]` | body | `array<object>` | yes | — |
| `line_items[].so_line_item_id` | body | `string` | yes | — |
| `line_items[].quantity` | body | `number` | yes | — |
