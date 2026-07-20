# Generate character image with Vadootv

Creates a character image in Vadootv.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/generate_character_image`
- **Base URL:** `https://aiapi.vadoo.tv`
- **Official documentation:** [Generate character image](https://docs.vadoo.tv/docs/guide/ai-character/create-character-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | The AI character ID to use as a base. |
| `prompt` | body | `string` | yes | Description of the scene or pose to generate. |
| `ratio` | body | `list<string>` | yes | Output image ratio. Accepted values: `16:9`, `1:1`, `3:4`, `4:3`, `9:16`. |
