# Create Product Mapping with Tiliter

Creates a product mapping in the Tiliter Recognition API.

## Endpoint

- **Method:** `POST`
- **Path:** `/product_mappings/`
- **Base URL:** `https://recognition.services.tiliter.com/v1/15`
- **Official documentation:** [Create Product Mapping](https://developer.tiliter.com/reference/create_product_mapping)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `productId` | body | `string` | yes |
| `archetypeId` | body | `string` | yes |
