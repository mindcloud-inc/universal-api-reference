# Create Product with Tiliter

Creates a product in the Tiliter Recognition API.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/:product_id`
- **Base URL:** `https://recognition.services.tiliter.com/v1/15`
- **Official documentation:** [Create Product](https://developer.tiliter.com/reference/create_product)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_id` | path | `string` | yes | — |
| `productId` | body | `string` | yes | Product ID in the request body. Must match Product ID Path. |
| `recognitionEnabled` | body | `boolean` | yes | — |
| `productName` | body | `string` | yes | — |
| `department` | body | `string` | yes | — |
| `productDescription` | body | `string` | no | — |
| `lookupCode` | body | `string` | no | — |
| `requiredAttributes[]` | body | `array<string>` | no | — |
| `requiredAttributes[]` | body | `array<string>` | no | — |
| `optionalAttributes[]` | body | `array<string>` | no | — |
| `optionalAttributes[]` | body | `array<string>` | no | — |
| `saleMethod` | body | `string` | no | — |
| `imageUrl` | body | `string` | no | — |
