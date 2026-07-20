# Remove Background with APImage

Removes the background from an image with APImage.

## Endpoint

- **Method:** `POST`
- **Path:** `https://app.apimage.org/api/v1/image-studio`
- **Base URL:** `https://apimage.org/api`
- **Official documentation:** [Remove Background](https://apimage.org/docs/api-reference#background-removal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input_image` | body | `string` | yes | Source image URL to process for background removal. |
| `prompt` | body | `string` | yes | Include a phrase like 'remove background' to trigger the background-removal flow. |
