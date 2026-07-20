# Create Sales Order with Zoho Inventory

Creates a new sales order in Zoho Inventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/salesorders`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Create Sales Order](https://www.zoho.com/inventory/api/v1/salesorders/#create-a-sales-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
| `customer_id` | body | `string` | yes | Customer to bill on the sales order. |
| `salesorder_number` | body | `string` | yes | Unique number for the sales order. |
| `date` | body | `string` | no | Sales order date in YYYY-MM-DD format. |
| `reference_number` | body | `string` | no | External reference number for the sales order. |
| `notes` | body | `string` | no | Notes shown on the sales order. |
| `line_items[]` | body | `array<object>` | yes | One or more sales order line items. |
| `line_items[].item_id` | body | `string` | yes | Item to add on this line. |
| `line_items[].quantity` | body | `number` | yes | Quantity to order for this line. |
| `line_items[].rate` | body | `number` | no | Rate for this line item. |
| `line_items[].description` | body | `string` | no | Description for this line item. |
| `ignore_auto_number_generation` | query | `boolean` | no | — |
