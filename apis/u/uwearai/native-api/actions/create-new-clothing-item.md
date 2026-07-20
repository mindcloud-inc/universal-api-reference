# Create New Clothing Item with Uwear.ai

Creates a new clothing item in Uwear.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/clothing-item`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Create New Clothing Item](https://docs.dev.uwear.ai/operations/external_create_clothing_item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clothing_item_name` | body | `string` | yes | Human-readable clothing item name. |
| `description` | body | `string` | yes | Text description of the clothing item front view. |
| `description_back` | body | `string` | yes | Text description of the clothing item back view. |
| `external_clothing_item_back_url` | body | `string` | no | Optional publicly fetchable direct image URL for the clothing item back view. |
| `external_clothing_item_url` | body | `string` | yes | Publicly fetchable direct image URL for the clothing item front view. |
| `use_image_enhancement` | body | `boolean` | no | Enable Uwear image enhancement before processing. |
