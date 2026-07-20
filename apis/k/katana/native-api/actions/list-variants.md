# List Variants with Katana

Lists variants in your Katana account.

## Endpoint

- **Method:** `GET`
- **Path:** `/variants`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [List Variants](https://developer.katanamrp.com/reference/list-all-variants)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | query | `array<number>` | no | Filters variants by an array of IDs |
| `product_id` | query | `number` | no | Filters variants by a product id |
| `material_id` | query | `number` | no | Filters variants by a material id |
| `sku[]` | query | `array<string>` | no | Filters variants by skus |
| `sales_price` | query | `number` | no | Filters variants by a sales price |
| `purchase_price` | query | `number` | no | Filters variants by a purchase price |
| `internal_barcode` | query | `string` | no | Filters variants by an internal barcode Maximum length: 40. |
| `registered_barcode` | query | `string` | no | Filters variants by a registered barcode Maximum length: 120. |
| `supplier_item_codes[]` | query | `array<string>` | no | Filters variants by supplier item codes. Returns the variants that match with any of the codes in the array. |
| `extend[]` | query | `array<string>` | no | Array of objects that need to be added to the response |
| `include_deleted` | query | `boolean` | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `include_archived` | query | `boolean` | no | Archived data is excluded from result set by default. Set to true to include it. |
| `created_at_min` | query | `string` | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `created_at_max` | query | `string` | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updated_at_min` | query | `string` | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updated_at_max` | query | `string` | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |
