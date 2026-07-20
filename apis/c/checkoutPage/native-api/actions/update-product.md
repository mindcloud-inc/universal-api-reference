# Update Product with Checkout Page

Updates a product in Checkout Page.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/products/:productId`
- **Base URL:** `https://api.checkoutpage.com`
- **Official documentation:** [Update Product](https://checkoutpage.com/docs/api/v1/products/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | Unique identifier. Must be in BSON ObjectId format. |
| `title` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `price` | body | `object` | no | — |
| `sku` | body | `string` | no | — |
| `hasUnlimitedStock` | body | `boolean` | no | — |
| `stock` | body | `number` | no | — |
| `taxBehavior` | body | `string` | no | If Stripe Tax is enabled, determines the behaviour of Stripe Tax. Defaults to your Stripe Tax settings. |
| `taxCode` | body | `string` | no | — |
| `imageIds[]` | body | `array<string>` | no | Images for the product. Provide a list of image file IDs. Use the `/files/upload` API to add images. |
| `fileIds[]` | body | `array<string>` | no | Files for the product. Available to the customer after purchase. |
| `variantsRequired` | body | `boolean` | no | — |
| `variants[]` | body | `array<object>` | no | — |
