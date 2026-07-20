# Edit Image with Grok

Updates an image in Grok with prompt-based edits.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/edits`
- **Base URL:** `https://api.x.ai`
- **Official documentation:** [Edit Image](https://docs.x.ai/developers/rest-api-reference/inference/images#image-edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | xAI image editing model. |
| `prompt` | body | `string` | yes | Instructions describing the image edit. |
| `images[]` | body | `array<object>` | yes | Source images to edit. |
