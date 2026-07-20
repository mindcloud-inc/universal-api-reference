# Create Image Generation with CometAPI

Creates an image in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/images/generations`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Create Image Generation](https://www.cometapi.com/how-to-use-cometapi-a-beginners-guide/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Image generation model ID. |
| `prompt` | body | `string` | yes | Prompt describing the image to generate. |
