# Generate Image with Imagior

Creates an image in Imagior from a template.

## Endpoint

- **Method:** `POST`
- **Path:** `/image/generate`
- **Base URL:** `https://api.imagior.com`
- **Official documentation:** [Generate Image](https://docs.imagior.com/api-reference/image-generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `string` | yes | The unique ID of the design template to use for image generation. |
