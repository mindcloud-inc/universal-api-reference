# Create Inventory with Cerbo

Creates a new inventory item in Cerbo.

## Endpoint

- **Method:** `POST`
- **Path:** `/inventory`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Create Inventory](https://docs.cer.bo/#tag/Inventory/operation/createInventory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the inventory item |
| `nickname` | body | `string` | no | Short nickname for the item |
| `linked_product_type` | body | `string` | yes | Type of linked product: - `rxs`: Links to a medication in the drugs database - `plan_other`: Links to a supplement - `general`: General inventory item (no linked product) |
| `linked_product_id` | body | `number` | no | ID of the linked product. Required for "rxs" and "plan_other" types. |
| `charge_id` | body | `number` | yes | ID of the associated charge in the charge master |
| `preferred_stock_level` | body | `number` | yes | Target stock level to maintain |
| `current_quantity` | body | `number` | yes | Current quantity in stock |
| `preferred_restock_level` | body | `number` | no | Level at which to trigger restocking |
| `manufacturer` | body | `string` | no | Manufacturer name |
| `expiration_date` | body | `date` | no | Expiration date (must be in the future) |
| `lot_number` | body | `string` | no | Lot number for tracking |
| `discontinued` | body | `boolean` | no | Whether the item is discontinued |
| `date_discontinued` | body | `date` | no | Date the item was discontinued |
| `external_identifier` | body | `string` | no | External system identifier for integration |
| `location` | body | `string` | no | Location name (for multi-location practices) |
| `package_properties.ndc_code` | body | `string` | no | National Drug Code (for medications) |
| `package_properties.generic_for` | body | `string` | no | Brand name this is generic for |
| `package_properties.charge_per_dose` | body | `string` | no | Charge amount per dose |
| `package_properties.charge_per_dispense` | body | `string` | no | Charge amount per dispense |
| `package_properties.cost_per_dose` | body | `string` | no | Cost per dose |
| `package_properties.patient_information_url` | body | `string` | no | URL to patient information sheet |
| `package_properties.package_form` | body | `string` | no | Form of packaging |
| `package_properties.product_code` | body | `string` | no | Product code |
| `package_properties.description` | body | `string` | no | Product description/notes |
