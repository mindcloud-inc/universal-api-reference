# Update Inventory with Cerbo

Updates an existing inventory item in Cerbo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/inventory/:id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Update Inventory](https://docs.cer.bo/#tag/Inventory/operation/updateInventory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The inventory item ID |
| `name` | body | `string` | no | Name of the inventory item |
| `nickname` | body | `string` | no | Short nickname |
| `charge_id` | body | `number` | no | ID of the associated charge |
| `preferred_stock_level` | body | `number` | no | Target stock level |
| `current_quantity` | body | `number` | no | Current quantity in stock |
| `preferred_restock_level` | body | `number` | no | Restock trigger level |
| `manufacturer` | body | `string` | no | Manufacturer name |
| `expiration_date` | body | `date` | no | Expiration date (must be in the future) |
| `lot_number` | body | `string` | no | Lot number |
| `discontinued` | body | `boolean` | no | Whether item is discontinued |
| `date_discontinued` | body | `date` | no | Discontinuation date |
| `external_identifier` | body | `string` | no | External system identifier |
| `location` | body | `string` | no | Location name |
| `package_properties` | body | `object` | no | Package-specific properties (only provided fields are updated) |
