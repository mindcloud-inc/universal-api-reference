# Generate Image with Open AI

Generates an image in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/images/generations`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Generate Image](https://developers.openai.com/api/reference/resources/images/methods/generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt describing the image to generate. |
| `model` | body | `list` | yes | Image generation model ID. |
