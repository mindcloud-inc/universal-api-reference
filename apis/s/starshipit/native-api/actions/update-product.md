# Update Product with Starshipit

## Endpoint

- **Method:** `PUT`
- **Path:** `/products/update`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Update Product](https://api-docs.starshipit.com/#9101a9d7-91b1-492c-b7ad-5f92f80bbfd7)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `number` | no |
| `product.id` | body | `number` | no |
| `product.sku` | body | `string` | no |
| `product.title` | body | `string` | no |
| `product.customs_description` | body | `string` | no |
| `product.description` | body | `string` | no |
| `product.country` | body | `string` | no |
| `product.weight` | body | `number` | no |
| `product.height` | body | `number` | no |
| `product.length` | body | `number` | no |
| `product.width` | body | `number` | no |
| `product.hs_code` | body | `string` | no |
| `product.color` | body | `string` | no |
| `product.size` | body | `string` | no |
| `product.barcode` | body | `string` | no |
| `product.bin_location` | body | `string` | no |
| `product.brand` | body | `string` | no |
| `product.usage` | body | `string` | no |
| `product.material` | body | `string` | no |
| `product.model` | body | `string` | no |
| `product.mid` | body | `string` | no |
| `product.price` | body | `number` | no |
| `product.dangerous_goods_type` | body | `string` | no |
