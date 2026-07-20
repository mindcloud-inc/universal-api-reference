# Create Product Sample with Tiliter

Creates a product sample in the Tiliter Recognition API.

## Endpoint

- **Method:** `POST`
- **Path:** `/products/:product_id/samples`
- **Base URL:** `https://recognition.services.tiliter.com/v1/15`
- **Official documentation:** [Create Product Sample](https://developer.tiliter.com/reference/create_product_sample)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `product_id` | path | `string` | yes |
| `collectorEmail` | body | `string` | yes |
| `deviceId` | body | `string` | yes |
| `backgroundType` | body | `string` | yes |
| `weightGrams` | body | `number` | yes |
| `images[]` | body | `array<object>` | yes |
