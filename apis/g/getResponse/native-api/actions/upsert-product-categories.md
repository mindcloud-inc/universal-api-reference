# Upsert Product Categories with GetResponse

Creates or updates product categories for a GetResponse shop product.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shopId/products/:productId/categories`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Upsert Product Categories](https://apireference.getresponse.com/#operation/upsertProductCategories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopId` | path | `string` | yes | The shop ID |
| `productId` | path | `string` | yes | The product ID |
| `categories[]` | body | `array<object>` | yes | Categories to upsert |
| `categories[].categoryId` | body | `string` | yes | Category identifier |
| `categories[].isDefault` | body | `boolean` | no | Whether category is default |
