# Bulk Update Estimate Option Line Items with Housecall Pro

## Endpoint

- **Method:** `PUT`
- **Path:** `/estimates/:estimate_id/options/:option_id/line_items/bulk_update`
- **Base URL:** `https://api.housecallpro.com`
- **Official documentation:** [Bulk Update Estimate Option Line Items](https://docs.housecallpro.com/docs/housecall-public-api/b3e4391f7853f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `estimate_id` | path | `string` | yes | The estimate to update. |
| `option_id` | path | `string` | yes | The estimate option to update. |
| `line_items[]` | body | `array<object>` | no | Line items to update or create. |
| `line_items[].id` | body | `string` | no | Existing line item id to update. |
| `line_items[].service_item_id` | body | `string` | no | Service item id for the line item. |
| `line_items[].service_item_type` | body | `list<string>` | no | Service item type for the line item. Accepted values: `market_place`, `organizational`, `pricebook_material`. |
| `line_items[].name` | body | `string` | yes | Line item name. |
| `line_items[].unit_price` | body | `number` | no | Line item unit price. |
| `line_items[].unit_cost` | body | `number` | no | Line item unit cost. |
| `line_items[].quantity` | body | `number` | no | Line item quantity. |
| `line_items[].kind` | body | `list<string>` | no | Line item kind. Accepted values: `fixed discount`, `fixed gratuity`, `labor`, `materials`, `percent discount`. |
| `line_items[].taxable` | body | `boolean` | no | Whether the line item is taxable. |
| `line_items[].description` | body | `string` | no | Line item description. |
