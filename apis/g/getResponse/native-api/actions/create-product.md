# Create Product with GetResponse

Creates a new product in a GetResponse shop.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shopId/products`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Create Product](https://apireference.getresponse.com/#operation/createProduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopId` | path | `string` | yes | The shop ID |
| `name` | body | `string` | yes | The product name |
| `variants[]` | body | `array<object>` | yes | Product variants collection |
| `type` | body | `string` | no | The product type |
| `url` | body | `string` | no | External URL for the product |
| `vendor` | body | `string` | no | The product vendor |
| `externalId` | body | `string` | no | External identifier for the product |
| `categories[]` | body | `array<object>` | no | Product categories collection |
| `metaFields[]` | body | `array<object>` | no | Product meta fields collection |
| `variants[].name` | body | `string` | yes | Variant name |
| `variants[].price` | body | `number` | yes | Variant price |
| `variants[].priceTax` | body | `number` | yes | Variant price including tax |
| `variants[].sku` | body | `string` | yes | Variant SKU |
| `categories[].name` | body | `string` | no | Category name |
| `metaFields[].name` | body | `string` | no | Meta field name |
| `metaFields[].value` | body | `string` | no | Meta field value |
| `metaFields[].valueType` | body | `list<string>` | no | Meta field value type Accepted values: `integer`, `string`. |
| `variants[].images[]` | body | `array<object>` | no | Variant images collection |
| `variants[].metaFields[]` | body | `array<object>` | no | Variant meta fields collection |
| `variants[].taxes[]` | body | `array<object>` | no | Variant taxes collection |
| `variants[].images[].src` | body | `string` | yes | Source URL for the variant image |
| `variants[].images[].position` | body | `number` | yes | Position of the variant image |
| `variants[].metaFields[].name` | body | `string` | no | Variant meta field name |
| `variants[].metaFields[].value` | body | `string` | no | Variant meta field value |
| `variants[].metaFields[].valueType` | body | `list<string>` | no | Variant meta field value type Accepted values: `integer`, `string`. |
| `variants[].metaFields[].description` | body | `string` | no | Variant meta field description |
| `variants[].taxes[].name` | body | `string` | no | Variant tax name |
| `variants[].taxes[].rate` | body | `number` | no | Variant tax rate |
