# Create Avatar with Uwear.ai

Creates an avatar generation in Uwear.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/generation-avatar`
- **Base URL:** `https://api.uwear.ai`
- **Official documentation:** [Create Avatar](https://docs.dev.uwear.ai/operations/external_avatar_generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `num_images` | body | `number` | yes | Number of avatar images to generate. |
| `prompt` | body | `string` | yes | Prompt describing the avatar to generate. |
