# Bria Generate Image with CometAPI

Creates a Bria image in CometAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/bria/text-to-image`
- **Base URL:** `https://api.cometapi.com`
- **Official documentation:** [Bria Generate Image](https://apidoc.cometapi.com/api/image/bria/generate-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Text prompt for image generation. |
