# Create or Update Variant with Loyverse

Creates or updates a product variant in Loyverse.

## Endpoint

- **Method:** `POST`
- **Path:** `/variants`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [Create or Update Variant](https://developer.loyverse.com/docs/#tag/Items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variant_id` | body | `string` | no | The read only internal id of the variant. If included in the POST request it will cause an update instead of a creating a new object. |
| `item_id` | body | `string` | no | The item id this variant is attached to. |
| `sku` | body | `string` | no | The variant sku. It should be unique. |
| `reference_variant_id` | body | `string` | no | External reference id for the variant |
| `option1_value` | body | `string` | no | The value of the first option for this variant. Required if option1_name is set for the item this variant is attached to. |
| `option2_value` | body | `string` | no | The value of the second option for this variant. Required if option2_name is set for the item this variant is attached to. |
| `option3_value` | body | `string` | no | The value of the third option for this variant. Required if option3_name is set for the item this variant is attached to. |
| `barcode` | body | `string` | no | — |
| `cost` | body | `number` | no | The variant cost |
| `purchase_cost` | body | `number` | no | The variant purchase cost |
| `default_pricing_type` | body | `string` | no | The default variant pricing type. If the value is `VARIABLE` than the price is specified at the time of a sale. If there are several stores in the account than the price of the variant in each store is equal to this value by default unless different value is specified in the `stores` array for a particular store. |
| `default_price` | body | `number` | no | The default variant price (only for `pricing_type: FIXED`) If there are several stores in the account than the price of the variant in each store is equal to this value by default unless different value is specified in the `stores` array for a particular store. |
| `stores[]` | body | `array<object>` | no | The list of values that are unique for each store |
| `stores[]` | body | `array<object>` | no | The list of values that are unique for each store |
| `created_at` | body | `date` | no | The time when this resource was created |
| `updated_at` | body | `date` | no | The time when this resource was created |
| `deleted_at` | body | `date` | no | The time when this resource was created |
