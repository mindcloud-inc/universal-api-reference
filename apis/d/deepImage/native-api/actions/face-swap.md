# Face Swap with DeepImage

Creates a face-swapped image in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Face Swap](https://documentation.deep-image.ai/common-usecases/face-swap)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the original image whose face should be replaced. |
| `background.generate.ip_image2` | body | `string` | yes | Public URL of the face image that will be swapped into the source image. |
| `background.generate.description` | body | `string` | no | Optional prompt used to creatively reimagine the swapped result. |
| `background.generate.strength` | body | `number` | no | Controls how strongly the result is reimagined during face swap. |
