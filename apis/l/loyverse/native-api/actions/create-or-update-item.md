# Create or Update Item with Loyverse

Creates or updates an item in Loyverse.

## Endpoint

- **Method:** `POST`
- **Path:** `/items`
- **Base URL:** `https://api.loyverse.com/v1.0`
- **Official documentation:** [Create or Update Item](https://developer.loyverse.com/docs/#tag/Items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Read-only internal id of the item. If included in the POST request it will cause an update instead of a creating a new object. |
| `handle` | body | `string` | no | — |
| `item_name` | body | `string` | yes | The item name. |
| `description` | body | `string` | no | The item description. |
| `reference_id` | body | `string` | no | External reference id for the item |
| `category_id` | body | `string` | no | The category id of the item |
| `track_stock` | body | `boolean` | no | If true, the system tracks inventory for this item at all stores. Make sure you don't accidentally disable track stock. If you set `track_stock` to false then all inventory levels of this item are set to 0 |
| `sold_by_weight` | body | `boolean` | no | If true, a fractional quantity for this item can be specified at the time of a sale (for example 1.5) |
| `is_composite` | body | `boolean` | no | If true, the item contains a specified quantity of other items. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `use_production` | body | `boolean` | no | If true, the system tracks stock not only for its components but also for this item. This property can be set only for composite items. [Learn more](https://help.loyverse.com/help/how-work-production) |
| `components[]` | body | `array<object>` | no | The list of components for the item. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `components[]` | body | `array<object>` | no | The list of components for the item. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `components[]` | body | `array<object>` | no | The list of components for the item. [Learn more](https://help.loyverse.com/help/how-create-composite-item) |
| `primary_supplier_id` | body | `string` | no | — |
| `tax_ids[]` | body | `array<string>` | no | The list of tax ids applied to this item |
| `tax_ids[]` | body | `array<string>` | no | The list of tax ids applied to this item |
| `tax_ids[]` | body | `array<string>` | no | The list of tax ids applied to this item |
| `modifiers_ids[]` | body | `array<string>` | no | The list of modifiers ids applied to this item |
| `modifiers_ids[]` | body | `array<string>` | no | The list of modifiers ids applied to this item |
| `modifiers_ids[]` | body | `array<string>` | no | The list of modifiers ids applied to this item |
| `form` | body | `string` | no | The visual form of the item that is displayed on the POS |
| `color` | body | `string` | no | One of the predefined colors for the item that is displayed on the POS |
| `image_url` | body | `string` | no | — |
| `option1_name` | body | `string` | no | The name of the first option (for example "Size"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `option2_name` | body | `string` | no | The name of the first option (for example "Color"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `option3_name` | body | `string` | no | The name of the first option (for example "Material"). [Learn more](https://help.loyverse.com/help/how-use-variants-items) |
| `created_at` | body | `date` | no | The time when this resource was created (ISO 8601 format, e.g. 2020-03-25T19:55:23.077Z) |
| `updated_at` | body | `date` | no | The time when this resource was updated (ISO 8601 format, e.g. 2020-03-30T08:05:10.020Z) |
| `deleted_at` | body | `date` | no | The time when this resource was deleted (ISO 8601 format, e.g. 2020-04-02T23:45:20.050Z) |
| `variants[]` | body | `array<object>` | no | — |
| `variants[]` | body | `array<object>` | no | — |
| `variants[]` | body | `array<object>` | no | — |
