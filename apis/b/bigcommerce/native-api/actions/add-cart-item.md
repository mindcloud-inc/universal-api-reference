# Add Cart Item with BigCommerce

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/carts/:cartId/items`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`
- **Official documentation:** [Add Cart Item](https://developer.bigcommerce.com/docs/rest-management/carts/items#add-cart-line-items)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `custom_items[].list_price` | body | `string` | no |
| `custom_items[].name` | body | `string` | no |
| `custom_items[].quantity` | body | `number` | no |
| `line_items[].gift_wrapping` | body | `object` | no |
| `line_items[].gift_wrapping.wrap_details` | body | `string` | no |
| `line_items[].list_price` | body | `string` | no |
| `line_items[].name` | body | `string` | no |
| `line_items[].product_id` | body | `string` | no |
| `line_items[].variant_id` | body | `string` | no |
| `cartId` | path | `string` | yes |
| `custom_items[].sku` | body | `string` | no |
| `line_items[]` | body | `array` | no |
| `line_items[].gift_wrapping.wrap_together` | body | `string` | no |
| `line_items[].quantity` | body | `string` | no |
| `custom_items[]` | body | `array` | no |
| `gift_certificates[]` | body | `array` | no |
| `version` | body | `number` | no |
