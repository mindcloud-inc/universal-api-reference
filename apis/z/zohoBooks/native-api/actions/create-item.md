# Create Item with Zoho Books

## Endpoint

- **Method:** `POST`
- **Path:** `/items`
- **Base URL:** `https://www.zohoapis.com/books/v3`
- **Official documentation:** [Create Item](https://www.zoho.com/books/api/v3/items/#create-an-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | query | `list<string>` | yes | ID of the organization. |
| `name` | body | `string` | yes | Name of the item. Maximum length: 100. |
| `rate` | body | `number` | yes | Price of the item. |
| `description` | body | `string` | no | Description for the item. Maximum length: 2000. |
| `sku` | body | `string` | no | SKU value for the item. |
| `product_type` | body | `list<string>` | no | Type of the item. Accepted values: `capital_goods`, `capital_service`, `digital_service`, `goods`, `service`. |
| `item_type` | body | `list<string>` | no | Commercial type of the item. Accepted values: `inventory`, `purchases`, `sales`, `sales_and_purchases`. |
| `tax_id` | body | `string` | no | Tax ID for the item. |
| `is_taxable` | body | `boolean` | no | Whether the item is taxable. |
| `tax_exemption_id` | body | `string` | no | Tax exemption ID when the item is not taxable. |
| `account_id` | body | `string` | no | Revenue account ID for the item. |
| `vendor_id` | body | `string` | no | Preferred vendor ID. |
| `reorder_level` | body | `number` | no | Reorder level for the item. |
| `purchase_description` | body | `string` | no | Purchase description for the item. |
| `purchase_rate` | body | `number` | no | Purchase price of the item. |
| `purchase_account_id` | body | `string` | no | COGS account ID for purchase or inventory items. |
| `inventory_account_id` | body | `string` | no | Inventory account ID for inventory items. |
| `locations[]` | body | `array<object>` | no | Per-location opening stock details. |
| `locations[].location_id` | body | `string` | no | Location ID. |
| `locations[].initial_stock` | body | `number` | no | Opening stock for the location. |
| `locations[].initial_stock_rate` | body | `number` | no | Unit price of the opening stock. |
