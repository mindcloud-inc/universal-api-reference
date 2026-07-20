# Update Clothing Item with Uwear.ai

Updates an existing clothing item in Uwear.ai.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/clothing-item/:clothing_item_id`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Update Clothing Item](https://docs.dev.uwear.ai/operations/external_update_clothing_item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clothing_item_id` | path | `number` | yes | Clothing item ID. |
| `clothing_item_name` | body | `string` | no | Updated clothing item name. |
| `description` | body | `string` | no | Updated front-view description. |
| `description_back` | body | `string` | no | Updated back-view description. |
