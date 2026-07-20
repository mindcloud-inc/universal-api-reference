# Generate Image with Agent.ai

Creates an AI-generated image in Agent.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/generate_image`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Generate Image](https://docs.agent.ai/api-reference/use-ai/generate-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Prompt to generate an image from. |
| `model` | body | `string` | yes | Image generation model to use. |
| `model_style` | body | `string` | yes | Image style for the generation model. |
| `model_aspect_ratio` | body | `string` | yes | Image aspect ratio for the generation model. |
