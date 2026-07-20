# Create Product with SquareSpace

Creates a product in Squarespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/commerce/products`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Create Product](https://developers.squarespace.com/commerce-apis/products#create-product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Product description. |
| `isVisible` | body | `boolean` | no | Whether product is visible on storefront. |
| `name` | body | `string` | yes | Product name. |
| `storePageId` | body | `list<string>` | yes | Target store page ID where the product is created. |
| `tags[]` | body | `array<string>` | no | Product tags. |
| `type` | body | `list<string>` | yes | Product type (for example PHYSICAL). Accepted values: `GIFT_CARD`, `PHYSICAL`, `SERVICE`. |
| `variants[]` | body | `array<object>` | no | List of product variants. |
| `variants[].pricing.basePrice.currency` | body | `string` | no | Variant base price currency (ISO code). |
| `variants[].pricing.basePrice.value` | body | `string` | no | Variant base price amount. |
| `variants[].sku` | body | `string` | no | Variant SKU code. |
