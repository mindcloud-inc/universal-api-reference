# Replace Product with Omnisend

Replaces an existing product in Omnisend.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v5/products/:productID`
- **Base URL:** `https://api.omnisend.com`
- **Official documentation:** [Replace Product](https://api-docs.omnisend.com/reference/put_products-productid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | body | `string` | no | — |
| `id` | body | `string` | yes | — |
| `productID` | path | `string` | yes | Unique Omnisend product identifier. |
| `status` | body | `string` | no | — |
| `title` | body | `string` | no | — |
| `url` | body | `string` | yes | — |
| `variants[]` | body | `array<object>` | no | — |
| `variants[].defaultImageUrl` | body | `string` | no | — |
| `variants[].description` | body | `string` | no | — |
| `variants[].id` | body | `string` | yes | — |
| `variants[].images[]` | body | `array<string>` | no | — |
| `variants[].price` | body | `number` | no | — |
| `variants[].sku` | body | `string` | no | — |
| `variants[].status` | body | `string` | no | — |
| `variants[].strikeThroughPrice` | body | `number` | no | — |
| `variants[].title` | body | `string` | no | — |
| `variants[].url` | body | `string` | yes | — |
