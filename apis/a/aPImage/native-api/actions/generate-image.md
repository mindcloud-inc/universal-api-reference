# Generate Image with APImage

Generates or edits an image with APImage.

## Endpoint

- **Method:** `POST`
- **Path:** `https://app.apimage.org/api/v1/image-studio`
- **Base URL:** `https://apimage.org/api`
- **Official documentation:** [Generate Image](https://apimage.org/docs/api-reference#generate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | Describe the image you want APImage to generate. |
| `model` | body | `string` | yes | Choose the FLUX model to use for generation. |
