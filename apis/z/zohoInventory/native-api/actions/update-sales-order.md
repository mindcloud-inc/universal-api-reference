# Update Sales Order with Zoho Inventory

Updates an existing sales order in Zoho Inventory.

## Endpoint

- **Method:** `PUT`
- **Path:** `/salesorders/:salesorder_id`
- **Base URL:** `{api_domain}/inventory/v1`
- **Official documentation:** [Update Sales Order](https://www.zoho.com/inventory/api/v1/salesorders/#update-a-sales-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `salesorder_id` | path | `string` | yes | The Zoho Inventory salesorder_id for the sales order. |
| `organization_id` | query | `string` | yes | Zoho Inventory organization ID to run this request against. |
| `customer_id` | body | `string` | yes | Customer to bill on the sales order. |
| `salesorder_number` | body | `string` | yes | Unique number for the sales order. |
| `date` | body | `string` | no | Sales order date in YYYY-MM-DD format. |
| `reference_number` | body | `string` | no | External reference number for the sales order. |
| `notes` | body | `string` | no | Notes shown on the sales order. |
| `line_items[]` | body | `array<object>` | yes | One or more sales order line items. |
| `line_items[].line_item_id` | body | `string` | no | Existing line item identifier when updating a line. |
| `line_items[].item_id` | body | `string` | yes | Item to set on this line. |
| `line_items[].quantity` | body | `number` | yes | Quantity to order for this line. |
| `line_items[].rate` | body | `number` | no | Rate for this line item. |
