# Update Product with Sellty

## Endpoint

- **Method:** `POST`
- **Path:** `/seller/api/v-1-0/set-product`
- **Base URL:** `https://my.sellty.ru`
- **Official documentation:** [Update Product](https://my.sellty.ru/seller/docs/api-docs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vendor_code` | body | `string` | yes | Product SKU/vendor code to update. |
| `category_id` | body | `string` | no | Product category ID. |
| `price` | body | `string` | no | Product price. |
| `amount` | body | `number` | no | Available product quantity. |
| `amount_wait` | body | `number` | no | Expected product quantity. |
| `volume` | body | `string` | no | Product volume. |
| `weight` | body | `string` | no | Product weight. |
| `length` | body | `string` | no | Product length. |
| `width` | body | `string` | no | Product width. |
| `height` | body | `string` | no | Product height. |
| `status` | body | `boolean` | no | Product active status. |
