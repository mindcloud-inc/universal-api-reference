# Generate Image with DeepAI

Creates an AI-generated image in DeepAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/text2img`
- **Base URL:** `https://api.deepai.org/api`
- **Official documentation:** [Generate Image](https://api.deepai.org/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | The text prompt describing the image to generate. |
