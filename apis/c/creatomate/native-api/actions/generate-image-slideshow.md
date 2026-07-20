# Generate Image Slideshow with Creatomate

Creates an image slideshow render in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Generate Image Slideshow](https://creatomate.com/docs/api/quick-start/generate-an-image-slideshow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUrls[]` | body | `array<string>` | yes | Ordered list of image URLs to include in the slideshow. |
| `imageDurationSeconds` | body | `number` | no | How long each image should stay on screen before the next one. |
| `includeTransitions` | body | `boolean` | no | Whether to add the documented transition animation between images. |
| `transitionType` | body | `string` | no | Creatomate transition type to apply between images. |
| `transitionDirection` | body | `string` | no | Direction used by the slide transition. |
| `includeZoomOut` | body | `boolean` | no | Whether to add the documented zoom-out effect to each image. |
