# Create Generation with Uwear.ai

Creates a generation in Uwear.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/generation`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Create Generation](https://docs.dev.uwear.ai/operations/external_create_generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatar_id` | body | `number` | no | Optional avatar ID to use for the generation. |
| `camera` | body | `string` | no | Optional camera framing preset. |
| `clothing_item_id` | body | `number` | no | Existing clothing item ID to use for the generation. |
| `enhance_user_prompt` | body | `boolean` | no | Let Uwear enhance the prompt before generation. |
| `num_images` | body | `number` | yes | Number of images to generate. |
| `prompt` | body | `string` | yes | Prompt describing the generated fashion image. |
