# Update Product with GetResponse

Updates an existing product in a GetResponse shop.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shopId/products/:productId`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Update Product](https://apireference.getresponse.com/#operation/updateProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopId` | path | `string` | yes | The shop ID |
| `productId` | path | `string` | yes | The product ID |
| `name` | body | `string` | no | The product name |
| `type` | body | `string` | no | The product type |
| `url` | body | `string` | no | External URL for the product |
| `vendor` | body | `string` | no | The product vendor |
| `externalId` | body | `string` | no | External identifier for the product |
| `categories[]` | body | `array<object>` | no | Product categories collection |
| `variants[]` | body | `array<object>` | no | Product variants collection |
| `metaFields[]` | body | `array<object>` | no | Product meta fields collection |
| `variants[].name` | body | `string` | no | Variant name |
| `variants[].price` | body | `number` | no | Variant price |
| `variants[].priceTax` | body | `number` | no | Variant price including tax |
| `variants[].sku` | body | `string` | no | Variant SKU |
| `categories[].name` | body | `string` | no | Category name |
| `metaFields[].name` | body | `string` | no | Meta field name |
| `metaFields[].value` | body | `string` | no | Meta field value |
| `metaFields[].valueType` | body | `list<string>` | no | Meta field value type Accepted values: `integer`, `string`. |
| `variants[].images[]` | body | `array<object>` | no | Variant images collection |
| `variants[].metaFields[]` | body | `array<object>` | no | Variant meta fields collection |
| `variants[].taxes[]` | body | `array<object>` | no | Variant taxes collection |
| `variants[].images[].src` | body | `string` | no | Source URL for the variant image |
| `variants[].images[].position` | body | `number` | no | Position of the variant image |
| `variants[].metaFields[].name` | body | `string` | no | Variant meta field name |
| `variants[].metaFields[].value` | body | `string` | no | Variant meta field value |
| `variants[].metaFields[].valueType` | body | `list<string>` | no | Variant meta field value type Accepted values: `integer`, `string`. |
| `variants[].metaFields[].description` | body | `string` | no | Variant meta field description |
| `variants[].taxes[].name` | body | `string` | no | Variant tax name |
| `variants[].taxes[].rate` | body | `number` | no | Variant tax rate |
