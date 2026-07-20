# Update Product with Botbaba

## Endpoint

- **Method:** `POST`
- **Path:** `/api/EditProduct`
- **Base URL:** `https://app.botbaba.io`
- **Official documentation:** [Update Product](https://app.botbaba.io/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Product identifier. |
| `botId` | body | `number` | yes | Bot identifier. |
| `productName` | body | `string` | yes | Product name. |
| `description` | body | `string` | no | Product description. |
| `sku` | body | `string` | no | Stock keeping unit. |
| `price` | body | `number` | no | Product price. |
| `displayPrice` | body | `number` | no | Display price. |
| `displayDiscountPer` | body | `number` | no | Display discount percentage. |
| `type` | body | `string` | no | Product type. |
| `image` | body | `string` | no | Image payload or URL. |
| `imageExtension` | body | `string` | no | Image file extension. |
| `foodType` | body | `string` | no | Food type. |
| `isSpicy` | body | `boolean` | no | Whether the product is spicy. |
| `isActive` | body | `boolean` | no | Whether the product is active. |
| `categories[]` | body | `array<number>` | no | Category identifiers. |
