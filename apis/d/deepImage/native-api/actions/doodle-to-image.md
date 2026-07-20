# Doodle to Image with DeepImage

Creates an image from a doodle in DeepImage.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest_api/process`
- **Base URL:** `https://deep-image.ai`
- **Official documentation:** [Doodle to Image](https://documentation.deep-image.ai/common-usecases/ai-drawing-to-image-doodle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the sketch or doodle image to transform. |
| `background.generate.description` | body | `string` | yes | Prompt describing what the doodle should become. |
