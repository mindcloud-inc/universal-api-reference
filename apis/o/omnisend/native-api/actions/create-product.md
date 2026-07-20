# Create Product with Omnisend

Creates a new product in Omnisend.

## Endpoint

- **Method:** `POST`
- **Path:** `/v5/products`
- **Base URL:** `https://api.omnisend.com`
- **Official documentation:** [Create Product](https://api-docs.omnisend.com/reference/post_products)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `categoryIDs[]` | body | `array<string>` | no | — |
| `createdAt` | body | `date` | no | — |
| `currency` | body | `string` | no | — |
| `defaultImageUrl` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `id` | body | `string` | yes | — |
| `images[]` | body | `array<string>` | no | — |
| `status` | body | `string` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `title` | body | `string` | no | — |
| `type` | body | `string` | no | — |
| `updatedAt` | body | `date` | no | — |
| `url` | body | `string` | yes | — |
| `variants[]` | body | `array<object>` | no | — |
| `variants[].defaultImageUrl` | body | `string` | no | — |
| `variants[].description` | body | `string` | no | — |
| `variants[].id` | body | `string` | yes | — |
| `variants[].images[]` | body | `array<string>` | no | — |
| `variants[].price` | body | `number` | no | — |
| `variants[].sku` | body | `string` | no | — |
| `variants[].status` | body | `string` | yes | Required per verified runtime. Use one of: inStock, outOfStock, notAvailable. |
| `variants[].strikeThroughPrice` | body | `number` | no | — |
| `variants[].title` | body | `string` | no | — |
| `variants[].url` | body | `string` | yes | — |
| `vendor` | body | `string` | no | — |
