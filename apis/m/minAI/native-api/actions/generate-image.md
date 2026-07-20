# Generate image with 1minAI

Creates an image from a text prompt in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Generate image](https://docs.1min.ai/docs/api/ai-for-image/image-generator/gpt-image-1-mini-image-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | — |
| `size` | body | `list` | no | Accepted values: `1024x1024`. |
| `quality` | body | `list` | no | Accepted values: `Auto`, `High`, `Low`, `Medium`. |
