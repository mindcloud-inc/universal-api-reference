# Create Product with Sellty

## Endpoint

- **Method:** `POST`
- **Path:** `/seller/api/v-1-0/add-product`
- **Base URL:** `https://my.sellty.ru`
- **Official documentation:** [Create Product](https://my.sellty.ru/seller/docs/api-docs.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Product name. |
| `category_id` | body | `string` | no | Product category ID. |
| `vendor_code` | body | `string` | no | Product SKU/vendor code. |
| `price` | body | `number` | no | Product price. |
| `amount` | body | `number` | no | Available product quantity. |
| `amount_wait` | body | `number` | no | Expected product quantity. |
| `volume` | body | `string` | no | Product volume. |
| `weight` | body | `string` | no | Product weight. |
| `length` | body | `string` | no | Product length. |
| `width` | body | `string` | no | Product width. |
| `height` | body | `string` | no | Product height. |
| `description` | body | `string` | no | Product description. |
| `status` | body | `boolean` | no | Product active status. |
